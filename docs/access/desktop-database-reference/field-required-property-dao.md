---
title: Propriedade Field.Required (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25ba678f759fefa460dd505cded6e05b3e96fdf5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928351"
---
# <a name="fieldrequired-property-dao"></a><span data-ttu-id="c92bc-102">Propriedade Field.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="c92bc-102">Field.Required property (DAO)</span></span>


<span data-ttu-id="c92bc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c92bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c92bc-104">Define ou retorna um valor que indica se um objeto **[Field](field-object-dao.md)** requer um valor não Null.</span><span class="sxs-lookup"><span data-stu-id="c92bc-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c92bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c92bc-105">Syntax</span></span>

<span data-ttu-id="c92bc-106">*expressão* . Necessário</span><span class="sxs-lookup"><span data-stu-id="c92bc-106">*expression* .Required</span></span>

<span data-ttu-id="c92bc-107">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="c92bc-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c92bc-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c92bc-108">Remarks</span></span>

<span data-ttu-id="c92bc-109">Para um **Field** ainda não acrescentado à coleção **Fields**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c92bc-109">For a **Field** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="c92bc-110">A disponibilidade da propriedade **Required** depende do objeto que contém a coleção [Fields](fields-collection-dao.md), como exibido na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c92bc-110">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c92bc-111">Se a coleção Fields pertencer a um</span><span class="sxs-lookup"><span data-stu-id="c92bc-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="c92bc-112">Então Required será</span><span class="sxs-lookup"><span data-stu-id="c92bc-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c92bc-113">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="c92bc-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c92bc-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="c92bc-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c92bc-115">Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="c92bc-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c92bc-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c92bc-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c92bc-117">Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="c92bc-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c92bc-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c92bc-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c92bc-119">Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="c92bc-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c92bc-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="c92bc-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c92bc-121">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="c92bc-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c92bc-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c92bc-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c92bc-p101">Use a propriedade **Required** junto com a propriedade **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** ou a propriedade **[ValidationRule](field-validationrule-property-dao.md)** para determinar a validade da definição da propriedade **[Value](field-value-property-dao.md)** desse objeto **Field**. Se a propriedade **Required** for definida como **False**, o campo pode conter os valores **null** assim como os valores que atendem as condições especificadas pelas definições das propriedades **AllowZeroLength** e **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="c92bc-p101">You can use the **Required** property along with the **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to determine the validity of the **[Value](field-value-property-dao.md)** property setting for that **Field** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c92bc-p102">[!OBSERVAçãO] Quando definir essa propriedade para um objeto <STRONG>Index</STRONG> ou um objeto <STRONG>Field</STRONG>, defina-a para o objeto <STRONG>Field</STRONG>. A validade da definição da propriedade para um objeto <STRONG>Field</STRONG> é verificada antes da validade do objeto <STRONG>Index</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c92bc-p102">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object. The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



## <a name="example"></a><span data-ttu-id="c92bc-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c92bc-127">Example</span></span>

<span data-ttu-id="c92bc-p103">Este exemplo usa a propriedade **Required** para relatar quais campos de três tabelas diferentes devem conter dados para que um novo registro possa ser adicionado. O procedimento RequiredOutput é necessário para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="c92bc-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

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

