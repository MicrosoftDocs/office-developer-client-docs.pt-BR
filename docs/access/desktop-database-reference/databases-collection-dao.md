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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294642"
---
# <a name="databases-collection-dao"></a><span data-ttu-id="b6c3c-102">Coleção Databases (DAO)</span><span class="sxs-lookup"><span data-stu-id="b6c3c-102">Databases collection (DAO)</span></span>

<span data-ttu-id="b6c3c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6c3c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6c3c-104">Uma coleção **Databases** contém todos os objetos **Database** abertos ou criados em um objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-104">A **Databases** collection contains all open **Database** objects opened or created in a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6c3c-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6c3c-105">Remarks</span></span>

<span data-ttu-id="b6c3c-p101">Quando você abre um objeto **Database** existente ou cria um novo a partir de um **Workspace**, ele é automaticamente acrescentado à coleção **Databases**. Quando você fecha um objeto **Database** com o método **[Close](connection-close-method-dao.md)**, ele é removido da coleção **Databases** mas não excluído do disco. Você deve fechar todos os objetos **Recordset** antes de fechar um objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-p101">When you open an existing **Database** object or create a new one from a **Workspace**, it is automatically appended to the **Databases** collection. When you close a **Database** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Databases** collection but not deleted from disk. You should close all open **Recordset** objects before closing a **Database** object.</span></span>

<span data-ttu-id="b6c3c-109">Em um espaço de trabalho do Microsoft Access, a configuração da propriedade **Name** de um banco de dados é uma sequência de caracteres que especifica o caminho do arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-109">In a Microsoft Access workspace, the **Name** property setting of a database is a string that specifies the path of the database file.</span></span>

<span data-ttu-id="b6c3c-110">Para fazer referência a um objeto **Database** em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:</span><span class="sxs-lookup"><span data-stu-id="b6c3c-110">To refer to a **Database** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="b6c3c-111">**Bancos de** dados (0)</span><span class="sxs-lookup"><span data-stu-id="b6c3c-111">**Databases**(0)</span></span>

- <span data-ttu-id="b6c3c-112">**Bancos de** dados ("*nome*")</span><span class="sxs-lookup"><span data-stu-id="b6c3c-112">**Databases**("*name*")</span></span>

- <span data-ttu-id="b6c3c-113">**Bancos de dados** \! \[ *name*\]</span><span class="sxs-lookup"><span data-stu-id="b6c3c-113">**Databases**\!\[*name*\]</span></span>

> [!NOTE]
> <span data-ttu-id="b6c3c-p102">Você pode abrir a mesma fonte de dados ou o mesmo banco de dados mais de uma vez, criando nomes duplicados na coleção **Databases**. Você deve atribuir objetos **Database** a variáveis de objeto e fazer referência a eles por nome de variável.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-p102">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="b6c3c-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b6c3c-116">Example</span></span>

<span data-ttu-id="b6c3c-p103">Este exemplo cria um novo objeto **Database** e abre um objeto **Database** existente no objeto **Workspace** padrão. Em seguida, ele enumera a coleção **Database** e a coleção **Properties** de cada objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-p103">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

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

<span data-ttu-id="b6c3c-119">Este exemplo usa o **CreateDatabase** para criar um objeto **Database** novo e criptografado.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-119">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
