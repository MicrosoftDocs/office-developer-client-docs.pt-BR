---
title: Objeto de banco de dados (DAO)
TOCTitle: Database Object
ms:assetid: 6cf2ddf8-3957-a15e-5eeb-85f81c1e415e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195520(v=office.15)
ms:contentKeyID: 48545482
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm0
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 22754d966e3e45e08a9db79e509617b378f88633
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462955"
---
# <a name="database-object-dao"></a>Objeto de banco de dados (DAO)

**Aplica-se a**: Access 2013 | Office 2013

Um objeto **Database** representa um banco de dados aberto.

## <a name="remarks"></a>Comentários

Você usa o objeto **Database** e seus métodos e propriedades para manipular um banco de dados aberto. Em qualquer tipo de banco de dados, você pode:

  - Usar o método **Execute** para executar uma consulta ação.

  - Definir a propriedade **Connect** para estabelecer uma conexão com uma fonte de dados ODBC.

  - Definir a propriedade **QueryTimeout** para limitar a duração do tempo para aguardar a execução de uma consulta na fonte de dados ODBC.

  - Usar a propriedade **RecordsAffected** para determinar quantos registros foram alterados por uma consulta ação.

  - Usar o método **OpenRecordset** para executar uma consulta seleção e criar um objeto **Recordset**.

  - Usar a propriedade **Version** para determinar qual versão de um mecanismo de banco de dados criou o banco de dados.

Com um banco de dados do mecanismo do Microsoft Access, você também pode usar outros métodos, propriedades e coleções para manipular um objeto **Database**, bem como criar, modificar ou obter informações sobre suas tabelas, consultas e relações. Por exemplo, você pode:

  - Usar os métodos **CreateTableDef** e **CreateRelation** para criar tabelas e relações, respectivamente.

  - Usar o método **CreateProperty** para definir novas propriedades **Database**.

  - Usar o método **CreateQueryDef** para criar uma definição de consulta persistente ou temporária.

  - Usar os métodos **MakeReplica**, **Synchronize** e **PopulatePartial** para criar e sincronizar total ou parcialmente as réplicas do banco de dados.

  - Definir a propriedade **CollatingOrder** para estabelecer a ordem alfabética de classificação para os campos baseados em caracteres, em diferentes idiomas.

Você usa o método **CreateDatabase** para criar um objeto **Database** persistente que é automaticamente acrescentado à coleção **Databases** e salvo, posteriormente, no disco.

Você não precisa especificar o objeto **DBEngine** ao utilizar o método **OpenDatabase**.

Abrir um banco de dados com tabelas vinculadas não estabelece automaticamente os links para os arquivos externos especificados. Você deve fazer referência aos objetos **TableDef** ou **Field** da tabela ou abrir um objeto **Recordset**. Se você não puder estabelecer links com essas tabelas, ocorrerá um erro interceptável. Talvez seja necessário ter permissão de acesso ao banco de dados ou outro usuário pode ter aberto o banco de dados de forma exclusiva. Nesses casos, ocorrerá um erro interceptável.

Quando um procedimento que declara um objeto **Database** é executado, os objetos **Database** locais são fechados junto com qualquer objeto **Recordset** aberto. Quaisquer atualizações pendentes são perdidas e quaisquer transações pendentes são revertidas, mas não ocorre nenhum erro interceptável. Você deve concluir explicitamente as transações ou as edições pendentes e fechar os objetos **Recordset** e **Database** antes de sair dos procedimentos que declaram essas variáveis de objeto localmente.

Quando você usa um dos métodos de transação (**BeginTrans**, **CommitTrans** ou **Rollback**) no objeto **Workspace**, essas transações são aplicadas a todos os bancos de dados abertos no **Workspace** a partir do qual o objeto **Database** foi aberto. Se você quiser usar transações independentes, deverá primeiro abrir um objeto **Workspace** adicional e, em seguida, abrir outro objeto **Database** naquele objeto **Workspace**.


> [!NOTE]
> [!OBSERVAçãO] Você pode abrir a mesma fonte de dados ou banco de dados mais de uma vez, criando nomes duplicados na coleção **Databases**. Você deve atribuir objetos **Database** a variáveis de objeto e referir-se a eles pelo nome da variável.



## <a name="example"></a>Exemplo

Este exemplo cria um novo objeto **Database** e abre um objeto **Database** existente no objeto **Workspace** padrão. Em seguida, ele enumera a coleção **Database** e a coleção **Properties** de cada objeto **Database**.

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccessWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

Este exemplo usa o **CreateDatabase** para criar um objeto **Database** novo e criptografado.

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
