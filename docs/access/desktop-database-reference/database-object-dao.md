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
ms.openlocfilehash: 265edf6b5d426b87d718c66e9886b7a4877120de
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918846"
---
# <a name="database-object-dao"></a><span data-ttu-id="8c537-102">Objeto de banco de dados (DAO)</span><span class="sxs-lookup"><span data-stu-id="8c537-102">Database object (DAO)</span></span>

<span data-ttu-id="8c537-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c537-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c537-104">Um objeto **Database** representa um banco de dados aberto.</span><span class="sxs-lookup"><span data-stu-id="8c537-104">A **Database** object represents an open database.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c537-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c537-105">Remarks</span></span>

<span data-ttu-id="8c537-p101">Você usa o objeto **Database** e seus métodos e propriedades para manipular um banco de dados aberto. Em qualquer tipo de banco de dados, você pode:</span><span class="sxs-lookup"><span data-stu-id="8c537-p101">You use the **Database** object and its methods and properties to manipulate an open database. In any type of database, you can:</span></span>

  - <span data-ttu-id="8c537-108">Usar o método **Execute** para executar uma consulta ação.</span><span class="sxs-lookup"><span data-stu-id="8c537-108">Use the **Execute** method to run an action query.</span></span>

  - <span data-ttu-id="8c537-109">Definir a propriedade **Connect** para estabelecer uma conexão com uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="8c537-109">Set the **Connect** property to establish a connection to an ODBC data source.</span></span>

  - <span data-ttu-id="8c537-110">Definir a propriedade **QueryTimeout** para limitar a duração do tempo para aguardar a execução de uma consulta na fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="8c537-110">Set the **QueryTimeout** property to limit the length of time to wait for a query to execute against an ODBC data source.</span></span>

  - <span data-ttu-id="8c537-111">Usar a propriedade **RecordsAffected** para determinar quantos registros foram alterados por uma consulta ação.</span><span class="sxs-lookup"><span data-stu-id="8c537-111">Use the **RecordsAffected** property to determine how many records were changed by an action query.</span></span>

  - <span data-ttu-id="8c537-112">Usar o método **OpenRecordset** para executar uma consulta seleção e criar um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8c537-112">Use the **OpenRecordset** method to execute a select query and create a **Recordset** object.</span></span>

  - <span data-ttu-id="8c537-113">Usar a propriedade **Version** para determinar qual versão de um mecanismo de banco de dados criou o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8c537-113">Use the **Version** property to determine which version of a database engine created the database.</span></span>

<span data-ttu-id="8c537-p102">Com um banco de dados do mecanismo do Microsoft Access, você também pode usar outros métodos, propriedades e coleções para manipular um objeto **Database**, bem como criar, modificar ou obter informações sobre suas tabelas, consultas e relações. Por exemplo, você pode:</span><span class="sxs-lookup"><span data-stu-id="8c537-p102">With a Microsoft Access database engine database, you can also use other methods, properties, and collections to manipulate a **Database** object, as well as create, modify, or get information about its tables, queries, and relationships. For example, you can:</span></span>

  - <span data-ttu-id="8c537-116">Usar os métodos **CreateTableDef** e **CreateRelation** para criar tabelas e relações, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8c537-116">Use the **CreateTableDef** and **CreateRelation** methods to create tables and relations, respectively.</span></span>

  - <span data-ttu-id="8c537-117">Usar o método **CreateProperty** para definir novas propriedades **Database**.</span><span class="sxs-lookup"><span data-stu-id="8c537-117">Use the **CreateProperty** method to define new **Database** properties.</span></span>

  - <span data-ttu-id="8c537-118">Usar o método **CreateQueryDef** para criar uma definição de consulta persistente ou temporária.</span><span class="sxs-lookup"><span data-stu-id="8c537-118">Use the **CreateQueryDef** method to create a persistent or temporary query definition.</span></span>

  - <span data-ttu-id="8c537-119">Usar os métodos **MakeReplica**, **Synchronize** e **PopulatePartial** para criar e sincronizar total ou parcialmente as réplicas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8c537-119">Use **MakeReplica**, **Synchronize**, and **PopulatePartial** methods to create and synchronize full or partial replicas of your database.</span></span>

  - <span data-ttu-id="8c537-120">Definir a propriedade **CollatingOrder** para estabelecer a ordem alfabética de classificação para os campos baseados em caracteres, em diferentes idiomas.</span><span class="sxs-lookup"><span data-stu-id="8c537-120">Set the **CollatingOrder** property to establish the alphabetic sorting order for character-based fields in different languages.</span></span>

<span data-ttu-id="8c537-121">Você usa o método **CreateDatabase** para criar um objeto **Database** persistente que é automaticamente acrescentado à coleção **Databases** e salvo, posteriormente, no disco.</span><span class="sxs-lookup"><span data-stu-id="8c537-121">You use the **CreateDatabase** method to create a persistent **Database** object that is automatically appended to the **Databases** collection, thereby saving it to disk.</span></span>

<span data-ttu-id="8c537-122">Você não precisa especificar o objeto **DBEngine** ao utilizar o método **OpenDatabase**.</span><span class="sxs-lookup"><span data-stu-id="8c537-122">You don't need to specify the **DBEngine** object when you use the **OpenDatabase** method.</span></span>

<span data-ttu-id="8c537-p103">Abrir um banco de dados com tabelas vinculadas não estabelece automaticamente os links para os arquivos externos especificados. Você deve fazer referência aos objetos **TableDef** ou **Field** da tabela ou abrir um objeto **Recordset**. Se você não puder estabelecer links com essas tabelas, ocorrerá um erro interceptável. Talvez seja necessário ter permissão de acesso ao banco de dados ou outro usuário pode ter aberto o banco de dados de forma exclusiva. Nesses casos, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="8c537-p103">Opening a database with linked tables doesn't automatically establish links to the specified external files. You must either reference the table's **TableDef** or **Field** objects or open a **Recordset** object. If you can't establish links to these tables, a trappable error occurs. You may also need permission to access the database, or another user might have the database opened exclusively. In these cases, trappable errors occur.</span></span>

<span data-ttu-id="8c537-p104">Quando um procedimento que declara um objeto **Database** é executado, os objetos **Database** locais são fechados junto com qualquer objeto **Recordset** aberto. Quaisquer atualizações pendentes são perdidas e quaisquer transações pendentes são revertidas, mas não ocorre nenhum erro interceptável. Você deve concluir explicitamente as transações ou as edições pendentes e fechar os objetos **Recordset** e **Database** antes de sair dos procedimentos que declaram essas variáveis de objeto localmente.</span><span class="sxs-lookup"><span data-stu-id="8c537-p104">When a procedure that declares a **Database** object has executed, local **Database** objects are closed along with any open **Recordset** objects. Any pending updates are lost and any pending transactions are rolled back, but no trappable error occurs. You should explicitly complete any pending transactions or edits and close **Recordset** objects and **Database** objects before exiting procedures that declare these object variables locally.</span></span>

<span data-ttu-id="8c537-p105">Quando você usa um dos métodos de transação (**BeginTrans**, **CommitTrans** ou **Rollback**) no objeto **Workspace**, essas transações são aplicadas a todos os bancos de dados abertos no **Workspace** a partir do qual o objeto **Database** foi aberto. Se você quiser usar transações independentes, deverá primeiro abrir um objeto **Workspace** adicional e, em seguida, abrir outro objeto **Database** naquele objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="8c537-p105">When you use one of the transaction methods (**BeginTrans**, **CommitTrans**, or **Rollback**) on the **Workspace** object, these transactions apply to all databases opened on the **Workspace** from which the **Database** object was opened. If you want to use independent transactions, you must first open an additional **Workspace** object, and then open another **Database** object in that **Workspace** object.</span></span>


> [!NOTE]
> <span data-ttu-id="8c537-p106">[!OBSERVAçãO] Você pode abrir a mesma fonte de dados ou banco de dados mais de uma vez, criando nomes duplicados na coleção **Databases**. Você deve atribuir objetos **Database** a variáveis de objeto e referir-se a eles pelo nome da variável.</span><span class="sxs-lookup"><span data-stu-id="8c537-p106">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>



## <a name="example"></a><span data-ttu-id="8c537-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8c537-135">Example</span></span>

<span data-ttu-id="8c537-p107">Este exemplo cria um novo objeto **Database** e abre um objeto **Database** existente no objeto **Workspace** padrão. Em seguida, ele enumera a coleção **Database** e a coleção **Properties** de cada objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="8c537-p107">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

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

<span data-ttu-id="8c537-138">Este exemplo usa o **CreateDatabase** para criar um objeto **Database** novo e criptografado.</span><span class="sxs-lookup"><span data-stu-id="8c537-138">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
