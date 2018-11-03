---
title: Os limites de um Recordset
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c5b0f03e135f4e00b3ca9d6be7417bfe0e5047e6
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946577"
---
# <a name="limits-of-a-recordset"></a><span data-ttu-id="ae57f-102">Limites de um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="ae57f-102">Limits of a Recordset</span></span>


<span data-ttu-id="ae57f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae57f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae57f-p101">Use as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você ultrapassou os limites de um objeto **Recordset** ao se mover de um registro para outro. Pense nas propriedades **BOF** e **EOF** como registros "fantasmas" que são posicionados no início e no final de cada **Recordset**. Desenvolver o **Recordset** a partir de [Examinando dados](chapter-3-examining-data.md) daria a seguinte aparência ao objeto:</span><span class="sxs-lookup"><span data-stu-id="ae57f-p101">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record. Think of **BOF** and **EOF** as "phantom" records that are positioned at the beginning and end of the **Recordset**. Building on the sample **Recordset** from [Examining Data](chapter-3-examining-data.md), it would now look like this:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae57f-107">ProductID</span><span class="sxs-lookup"><span data-stu-id="ae57f-107">ProductID</span></span></p></th>
<th><p><span data-ttu-id="ae57f-108">ProductName</span><span class="sxs-lookup"><span data-stu-id="ae57f-108">ProductName</span></span></p></th>
<th><p><span data-ttu-id="ae57f-109">UnitPrice</span><span class="sxs-lookup"><span data-stu-id="ae57f-109">UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae57f-110">BOF</span><span class="sxs-lookup"><span data-stu-id="ae57f-110">BOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae57f-111">7</span><span class="sxs-lookup"><span data-stu-id="ae57f-111">7</span></span></p></td>
<td><p><span data-ttu-id="ae57f-112">Pêras secas orgânicas do Tio Bob</span><span class="sxs-lookup"><span data-stu-id="ae57f-112">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="ae57f-113">30.0000</span><span class="sxs-lookup"><span data-stu-id="ae57f-113">30.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae57f-114">14</span><span class="sxs-lookup"><span data-stu-id="ae57f-114">14</span></span></p></td>
<td><p><span data-ttu-id="ae57f-115">Tofu</span><span class="sxs-lookup"><span data-stu-id="ae57f-115">Tofu</span></span></p></td>
<td><p><span data-ttu-id="ae57f-116">23.2500</span><span class="sxs-lookup"><span data-stu-id="ae57f-116">23.2500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae57f-117">28</span><span class="sxs-lookup"><span data-stu-id="ae57f-117">28</span></span></p></td>
<td><p><span data-ttu-id="ae57f-118">Chucrute Rssle</span><span class="sxs-lookup"><span data-stu-id="ae57f-118">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="ae57f-119">45.6000</span><span class="sxs-lookup"><span data-stu-id="ae57f-119">45.6000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae57f-120">51</span><span class="sxs-lookup"><span data-stu-id="ae57f-120">51</span></span></p></td>
<td><p><span data-ttu-id="ae57f-121">Maçãs secas Manjimup</span><span class="sxs-lookup"><span data-stu-id="ae57f-121">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="ae57f-122">53.0000</span><span class="sxs-lookup"><span data-stu-id="ae57f-122">53.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae57f-123">74</span><span class="sxs-lookup"><span data-stu-id="ae57f-123">74</span></span></p></td>
<td><p><span data-ttu-id="ae57f-124">Tofu longa vida</span><span class="sxs-lookup"><span data-stu-id="ae57f-124">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="ae57f-125">10.0000</span><span class="sxs-lookup"><span data-stu-id="ae57f-125">10.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae57f-126">EOF</span><span class="sxs-lookup"><span data-stu-id="ae57f-126">EOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae57f-127">A propriedade **BOF** retorna **Verdadeiro** (-1) se a posição do registro atual for antes do primeiro registro e **Falso** (0) se a posição for no primeiro registro ou após ele.</span><span class="sxs-lookup"><span data-stu-id="ae57f-127">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="ae57f-128">A propriedade **EOF** retornará **True** se a posição do registro atual estiver depois do último registro e **Falso** se a posição atual do registro estiver no ou antes do último registro.</span><span class="sxs-lookup"><span data-stu-id="ae57f-128">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="ae57f-129">Se a propriedade **BOF** ou **EOF** for **True**, não haverá registro atual, conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="ae57f-129">If either the **BOF** or **EOF** property is **True**, there is no current record, as shown in the following code:</span></span>

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

<span data-ttu-id="ae57f-130">Se você abrir um objeto **Recordset** que não contenha registros, as propriedades **BOF** e **EOF** serão definidas como **True** e o valor da configuração da propriedade **RecordCount** do objeto **Recordset** dependerá do tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="ae57f-130">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type.</span></span> <span data-ttu-id="ae57f-131">-1 será retornado para cursores dinâmicos (**CursorType** = **adOpenDynamic**) e 0 será retornado para outros cursores.</span><span class="sxs-lookup"><span data-stu-id="ae57f-131">-1 will be returned for dynamic cursors (**CursorType** = **adOpenDynamic**) and 0 will be returned for other cursors.</span></span>

<span data-ttu-id="ae57f-132">Ao abrir um objeto **Recordset** que contenha pelo menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** serão **False**.</span><span class="sxs-lookup"><span data-stu-id="ae57f-132">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="ae57f-p103">Se você excluir o último registro do objeto **Recordset**, o cursor será deixado em estado indeterminado. As propriedades **BOF** e **EOF** podem permanecer como **False** até que seja feita uma tentativa de reposicionamento do registro atual, de acordo com o provedor.</span><span class="sxs-lookup"><span data-stu-id="ae57f-p103">If you delete the last remaining record in the **Recordset** object, the cursor is left in an indeterminate state. The **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record, depending upon the provider.</span></span>

