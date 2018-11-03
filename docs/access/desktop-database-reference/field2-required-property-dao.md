---
title: Propriedade Field2.Required (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf5e459773cd0fa0976704834b1b73467fc75294
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937404"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="81b57-102">Propriedade Field2.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="81b57-102">Field2.Required property (DAO)</span></span>


<span data-ttu-id="81b57-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="81b57-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="81b57-104">Define ou retorna um valor que indica se o objeto **Field2** requer ou não um valor não-Nulo .</span><span class="sxs-lookup"><span data-stu-id="81b57-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b57-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81b57-105">Syntax</span></span>

<span data-ttu-id="81b57-106">*expressão* . Necessário</span><span class="sxs-lookup"><span data-stu-id="81b57-106">*expression* .Required</span></span>

<span data-ttu-id="81b57-107">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="81b57-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="81b57-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="81b57-108">Remarks</span></span>

<span data-ttu-id="81b57-109">Para um objeto **Field2** ainda não acrescentado à coleção **Fields**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="81b57-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="81b57-110">A disponibilidade da propriedade **Required** depende do objeto que contém a coleção **[Fields](fields-collection-dao.md)**, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="81b57-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81b57-111">Se a coleção Fields pertencer a um</span><span class="sxs-lookup"><span data-stu-id="81b57-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="81b57-112">Então Required será</span><span class="sxs-lookup"><span data-stu-id="81b57-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81b57-113">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="81b57-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="81b57-114">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="81b57-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81b57-115">Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="81b57-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="81b57-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81b57-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81b57-117">Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="81b57-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="81b57-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81b57-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81b57-119">Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="81b57-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="81b57-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="81b57-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81b57-121">Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="81b57-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="81b57-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81b57-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="81b57-p101">Você pode usar a propriedade **Required** junto com as propriedades **AllowZeroLength**, **ValidateOnSet** ou **ValidationRule** para determinar a validade da configuração da propriedade **Value** para aquele objeto **Field2**. Se a propriedade **Required** for definida como **False**, o campo conterá valores **null** e valores que atendam às condições especificadas pelas configurações das propriedades **AllowZeroLength** e **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="81b57-p101">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="81b57-p102">[!OBSERVAçãO] Quando for possível definir essa propriedade para um objeto **Index** ou para um objeto **Field2**, defina-a para o objeto **Field2**. A validade da configuração da propriedade para um objeto **Field2** é verificada antes da configuração para um objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="81b57-p102">When you can set this property for either an **Index** object or a **Field2** object, set it for the **Field2** object. The validity of the property setting for a **Field2** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="81b57-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="81b57-127">Example</span></span>

<span data-ttu-id="81b57-p103">Este exemplo usa a propriedade **Required** para relatar quais campos de três tabelas diferentes devem conter dados para que um novo registro possa ser adicionado. O procedimento RequiredOutput é necessário para que este procedimento seja executado.</span><span class="sxs-lookup"><span data-stu-id="81b57-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

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
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

