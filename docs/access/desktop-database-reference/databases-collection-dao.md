---
title: Coleção Databases (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbaa0fe7aaa50c8aec582e2f03cd2849268816b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715547"
---
# <a name="databases-collection-dao"></a>Coleção Databases (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Uma coleção **Databases** contém todos os objetos **Database** abertos que foram abertos ou criados em um objeto **Workspace**.

## <a name="remarks"></a>Comentários

Quando você abre um objeto **Database** existente ou cria um novo a partir de um **Workspace**, ele é automaticamente acrescentado à coleção **Databases**. Quando você fecha um objeto **Database** com o método **[Close](connection-close-method-dao.md)**, ele é removido da coleção **Databases** mas não excluído do disco. Você deve fechar todos os objetos **Recordset** antes de fechar um objeto **Database**.

Em um espaço de trabalho do Microsoft Access, a configuração da propriedade **Name** de um banco de dados é uma sequência de caracteres que especifica o caminho do arquivo de banco de dados.

Para fazer referência a um objeto **Database** em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:

- **Databases**(0)

- **Bancos de dados** ("*nome*")

- **Bancos de dados**\!\[*nome*\]

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
 
 Set wrkAcc = CreateWorkspace("AccWorkspace", "admin", _ 
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
