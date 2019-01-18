---
title: Coleção Recordsets (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b935e05264497c7ad09ada4a8c50c775845857b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718760"
---
# <a name="recordsets-collection-dao"></a><span data-ttu-id="9dd6e-102">Coleção Recordsets (DAO)</span><span class="sxs-lookup"><span data-stu-id="9dd6e-102">Recordsets collection (DAO)</span></span>

<span data-ttu-id="9dd6e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9dd6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9dd6e-104">Uma coleção **Recordsets** contém todos os objetos **Recordset** abertos em um objeto **Connection** ou **Database**.</span><span class="sxs-lookup"><span data-stu-id="9dd6e-104">A **Recordsets** collection contains all open **Recordset** objects in a **Connection** or **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd6e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dd6e-105">Remarks</span></span>

<span data-ttu-id="9dd6e-106">Ao usar objetos DAO, você manipula dados praticamente usando objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9dd6e-106">When you use DAO objects, you manipulate data almost entirely using **Recordset** objects.</span></span>

<span data-ttu-id="9dd6e-107">Um novo objeto **Recordset** é automaticamente adicionado à coleção **Recordsets** quando você abre o objeto e é automaticamente removido quando você o fecha. **Recordset**</span><span class="sxs-lookup"><span data-stu-id="9dd6e-107">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the **Recordset** object, and is automatically removed when you close it.</span></span>

<span data-ttu-id="9dd6e-p101">Você pode criar quantas variáveis de objeto **Recordset** forem necessárias. Diferentes objetos **Recordset** podem acessar as mesmas tabelas, consultas e campos sem entrar em conflito.</span><span class="sxs-lookup"><span data-stu-id="9dd6e-p101">You can create as many **Recordset** object variables as needed. Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="9dd6e-110">Para se referir a um objeto **Recordset** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="9dd6e-110">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="9dd6e-111">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="9dd6e-111">**Recordsets**(0)</span></span>

- <span data-ttu-id="9dd6e-112">**Conjuntos de registros** ("nome")</span><span class="sxs-lookup"><span data-stu-id="9dd6e-112">**Recordsets**("name")</span></span>

- <span data-ttu-id="9dd6e-113">**Conjuntos de registros**\!\[nome\]</span><span class="sxs-lookup"><span data-stu-id="9dd6e-113">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="9dd6e-p102">[!OBSERVAçãO] É possível abrir um objeto **Recordset** a partir do mesmo banco de dados ou fonte de dados mais de uma vez criando nomes duplicados na coleção **Recordsets**. Você deve atribuir objetos **Recordsets** para variáveis de objetos e referenciá-los por nome de variável.</span><span class="sxs-lookup"><span data-stu-id="9dd6e-p102">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection. You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="9dd6e-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9dd6e-116">Example</span></span>

<span data-ttu-id="9dd6e-117">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9dd6e-117">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
