---
title: Propriedade Index.IgnoreNulls (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e7fd7b98b246f4fda24426d9376cc5edc2553b8e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870307"
---
# <a name="indexignorenulls-property-dao"></a><span data-ttu-id="7bc19-102">Propriedade Index.IgnoreNulls (DAO)</span><span class="sxs-lookup"><span data-stu-id="7bc19-102">Index.IgnoreNulls Property (DAO)</span></span>


<span data-ttu-id="7bc19-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bc19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bc19-104">Define ou retorna um valor que indica se os registros com valores Null nos campos de índice têm entradas de índice (somente nos espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="7bc19-104">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bc19-105">Syntax</span></span>

<span data-ttu-id="7bc19-106">*expressão* . IgnoreNulls</span><span class="sxs-lookup"><span data-stu-id="7bc19-106">*expression* .IgnoreNulls</span></span>

<span data-ttu-id="7bc19-107">*expressão* Uma variável que representa um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="7bc19-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bc19-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bc19-108">Remarks</span></span>

<span data-ttu-id="7bc19-109">Essa propriedade é leitura/gravação para um novo objeto **[Index](index-object-dao.md)** ainda não acrescentado a uma coleção e somente leitura para um objeto **Index** existente em uma coleção **[Indexes](indexes-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7bc19-109">This property is read/write for a new **[Index](index-object-dao.md)** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection.</span></span>

<span data-ttu-id="7bc19-p101">Para acelerar o processo de pesquisa dos registros, defina um índice para um campo. Se você permitir entradas **null** em um campo indexado e esperar que muitas das entradas sejam **null**, defina a propriedade **IgnoreNulls** do objeto **Index** como **True** para reduzir a quantidade de espaço usada pelo índice.</span><span class="sxs-lookup"><span data-stu-id="7bc19-p101">To speed up the process of searching for records, you can define an index for a field. If you allow **null** entries in an indexed field and expect many of the entries to be **null**, you can set the **IgnoreNulls** property for the **Index** object to **True** to reduce the amount of storage space that the index uses.</span></span>

<span data-ttu-id="7bc19-112">A definição da propriedade **IgnoreNulls** e a definição da propriedade **[Required](field-required-property-dao.md)** em conjunto determinam se o registro com o valor de índice **null** terá uma entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="7bc19-112">The **IgnoreNulls** property setting and the **[Required](field-required-property-dao.md)** property setting together determine whether a record with a **null** index value has an index entry.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bc19-113">Se IgnoreNulls for</span><span class="sxs-lookup"><span data-stu-id="7bc19-113">If IgnoreNulls is</span></span></p></th>
<th><p><span data-ttu-id="7bc19-114">e Required for</span><span class="sxs-lookup"><span data-stu-id="7bc19-114">And Required is</span></span></p></th>
<th><p><span data-ttu-id="7bc19-115">Então</span><span class="sxs-lookup"><span data-stu-id="7bc19-115">Then</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bc19-116">True</span><span class="sxs-lookup"><span data-stu-id="7bc19-116">True</span></span></p></td>
<td><p><span data-ttu-id="7bc19-117">False</span><span class="sxs-lookup"><span data-stu-id="7bc19-117">False</span></span></p></td>
<td><p><span data-ttu-id="7bc19-118">Um valor nulo é permitido no campo de índice; nenhuma entrada de índice foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="7bc19-118">A null value is allowed in the index field; no index entry added.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bc19-119">False</span><span class="sxs-lookup"><span data-stu-id="7bc19-119">False</span></span></p></td>
<td><p><span data-ttu-id="7bc19-120">False</span><span class="sxs-lookup"><span data-stu-id="7bc19-120">False</span></span></p></td>
<td><p><span data-ttu-id="7bc19-121">Um valor nulo é permitido no campo de índice; entrada de índice adicionada.</span><span class="sxs-lookup"><span data-stu-id="7bc19-121">A null value is allowed in the index field; index entry added.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bc19-122">True or False</span><span class="sxs-lookup"><span data-stu-id="7bc19-122">True or False</span></span></p></td>
<td><p><span data-ttu-id="7bc19-123">True</span><span class="sxs-lookup"><span data-stu-id="7bc19-123">True</span></span></p></td>
<td><p><span data-ttu-id="7bc19-124">Um valor nulo não é permitido no campo de índice; nenhuma entrada de índice foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="7bc19-124">A null value isn't allowed in the index field; no index entry added.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="7bc19-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7bc19-125">Example</span></span>

<span data-ttu-id="7bc19-126">Este exemplo define a propriedade **IgnoreNulls** de um novo **Index** como **True** ou **False** com base na entrada do usuário e depois demonstra o efeito em um **Recordset** com um registro cujo campo de chave contém um valor **Null**.</span><span class="sxs-lookup"><span data-stu-id="7bc19-126">This example sets the **IgnoreNulls** property of a new **Index** to **True** or **False** based on user input, and then demonstrates the effect on a **Recordset** with a record whose key field contains a **Null** value.</span></span>

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
