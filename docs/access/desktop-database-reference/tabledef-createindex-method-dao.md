---
title: Método TableDef.CreateIndex (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: baa82b659cc2260d4a003c644b2d03d6c897fd21
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706230"
---
# <a name="tabledefcreateindex-method-dao"></a><span data-ttu-id="5054d-102">Método TableDef.CreateIndex (DAO)</span><span class="sxs-lookup"><span data-stu-id="5054d-102">TableDef.CreateIndex method (DAO)</span></span>

<span data-ttu-id="5054d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5054d-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="5054d-p101">Cria um novo objeto **[Index](index-object-dao.md)** (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="5054d-p101">Creates a new **[Index](index-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="5054d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5054d-106">Syntax</span></span>

<span data-ttu-id="5054d-107">*expressão* . CreateIndex (***nome***)</span><span class="sxs-lookup"><span data-stu-id="5054d-107">*expression* .CreateIndex(***Name***)</span></span>

<span data-ttu-id="5054d-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="5054d-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5054d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5054d-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5054d-110">Nome</span><span class="sxs-lookup"><span data-stu-id="5054d-110">Name</span></span></p></th>
<th><p><span data-ttu-id="5054d-111">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="5054d-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5054d-112">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5054d-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="5054d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="5054d-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5054d-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="5054d-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="5054d-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="5054d-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="5054d-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="5054d-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="5054d-p102">Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Index</strong>. Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="5054d-p102">A <strong>String</strong> that uniquely names the new <strong>Index</strong> object. See the <strong>Name</strong> property for details on valid <strong>Index</strong> names.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="5054d-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5054d-119">Return value</span></span>

<span data-ttu-id="5054d-120">Index</span><span class="sxs-lookup"><span data-stu-id="5054d-120">Index</span></span>

## <a name="remarks"></a><span data-ttu-id="5054d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5054d-121">Remarks</span></span>

<span data-ttu-id="5054d-122">Você pode usar o método **CreateIndex** para criar um novo objeto **Index** para um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="5054d-122">You can use the **CreateIndex** method to create a new **Index** object for a **TableDef** object.</span></span> <span data-ttu-id="5054d-123">Se você omitir a parte do nome opcional quando você usa **CreateIndex**, você pode usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade **Name** , antes de você acrescentar o novo objeto a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="5054d-123">If you omit the optional name part when you use **CreateIndex**, you can use an appropriate assignment statement to set or reset the **Name** property before you append the new object to a collection.</span></span> <span data-ttu-id="5054d-124">Depois de acrescentar o objeto, você pode ou não conseguir definir sua propriedade **Name**, dependendo do tipo de objeto que contém a coleção **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="5054d-124">After you append the object, you may or may not be able to set its **Name** property, depending on the type of object that contains the **Indexes** collection.</span></span> <span data-ttu-id="5054d-125">Consulte o tópico da propriedade **Name** para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="5054d-125">See the **Name** property topic for more details.</span></span>

<span data-ttu-id="5054d-126">Se name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="5054d-126">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="5054d-127">Para remover um objeto **Index** de uma coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção.</span><span class="sxs-lookup"><span data-stu-id="5054d-127">To remove an **Index** object from a collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="5054d-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5054d-128">Example</span></span>

<span data-ttu-id="5054d-p104">Este exemplo usa o método **CreateIndex** para criar dois novos objetos **Index** e, em seguida, acrescenta-os à coleção **Indexes** do objeto **TableDef** Employees. Em seguida, é enumerada a coleção Indexes do objeto **TableDef**, a coleção **Fields** dos novos objetos **Index** e a coleção Properties dos novos objetos **Index**. A função CreateIndexOutput é exigida para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="5054d-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the Indexes collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
