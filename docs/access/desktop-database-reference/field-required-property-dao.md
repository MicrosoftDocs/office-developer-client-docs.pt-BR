---
title: Propriedade Field.Required (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6fbf95e02c9945558d70fff35f12a73ce0dee45e
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937313"
---
# <a name="fieldrequired-property-dao"></a><span data-ttu-id="fc1e2-102">Propriedade Field.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="fc1e2-102">Field.Required property (DAO)</span></span>


<span data-ttu-id="fc1e2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc1e2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc1e2-104">Define ou retorna um valor que indica se um objeto **[Field](field-object-dao.md)** requer um valor não Null.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc1e2-105">Syntax</span></span>

<span data-ttu-id="fc1e2-106">*expressão* . Necessário</span><span class="sxs-lookup"><span data-stu-id="fc1e2-106">*expression* .Required</span></span>

<span data-ttu-id="fc1e2-107">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="fc1e2-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc1e2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc1e2-108">Remarks</span></span>

<span data-ttu-id="fc1e2-109">Para um **Field** ainda não acrescentado à coleção **Fields**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-109">For a **Field** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="fc1e2-110">A disponibilidade da propriedade **Required** depende do objeto que contém a coleção [Fields](fields-collection-dao.md), como exibido na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-110">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc1e2-111">Se a coleção Fields pertencer a um</span><span class="sxs-lookup"><span data-stu-id="fc1e2-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="fc1e2-112">Então Required será</span><span class="sxs-lookup"><span data-stu-id="fc1e2-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc1e2-113">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="fc1e2-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc1e2-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="fc1e2-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc1e2-115">Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="fc1e2-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc1e2-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc1e2-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc1e2-117">Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="fc1e2-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc1e2-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc1e2-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc1e2-119">Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="fc1e2-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc1e2-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="fc1e2-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc1e2-121">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="fc1e2-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc1e2-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fc1e2-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc1e2-p101">Use a propriedade **Required** junto com a propriedade **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** ou a propriedade **[ValidationRule](field-validationrule-property-dao.md)** para determinar a validade da definição da propriedade **[Value](field-value-property-dao.md)** desse objeto **Field**. Se a propriedade **Required** for definida como **False**, o campo pode conter os valores **null** assim como os valores que atendem as condições especificadas pelas definições das propriedades **AllowZeroLength** e **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-p101">You can use the **Required** property along with the **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to determine the validity of the **[Value](field-value-property-dao.md)** property setting for that **Field** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="fc1e2-p102">[!OBSERVAçãO] Quando definir essa propriedade para um objeto **Index** ou um objeto **Field**, defina-a para o objeto **Field**. A validade da definição da propriedade para um objeto **Field** é verificada antes da validade do objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-p102">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object. The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="fc1e2-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fc1e2-127">Example</span></span>

<span data-ttu-id="fc1e2-p103">Este exemplo usa a propriedade **Required** para relatar quais campos de três tabelas diferentes devem conter dados para que um novo registro possa ser adicionado. O procedimento RequiredOutput é necessário para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="fc1e2-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

