---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a570171386a1ff00e1740e42cf914683ad5eb03
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871525"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="0e0e5-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="0e0e5-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="0e0e5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e0e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e0e5-104">Especifica se [Parameter](parameter-object-ado.md) representa um parâmetro de entrada, de saída, ou ambos, ou o valor de retorno de um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="0e0e5-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e0e5-105">Constant</span><span class="sxs-lookup"><span data-stu-id="0e0e5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0e0e5-106">Valor</span><span class="sxs-lookup"><span data-stu-id="0e0e5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0e0e5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e0e5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e0e5-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="0e0e5-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="0e0e5-109">1</span><span class="sxs-lookup"><span data-stu-id="0e0e5-109">1</span></span></p></td>
<td><p><span data-ttu-id="0e0e5-p101">Padrão. Indica que o parâmetro representa um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="0e0e5-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e0e5-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="0e0e5-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="0e0e5-113">3</span><span class="sxs-lookup"><span data-stu-id="0e0e5-113">3</span></span></p></td>
<td><p><span data-ttu-id="0e0e5-114">Indica que o parâmetro representa um parâmetro de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="0e0e5-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e0e5-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="0e0e5-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="0e0e5-116">2</span><span class="sxs-lookup"><span data-stu-id="0e0e5-116">2</span></span></p></td>
<td><p><span data-ttu-id="0e0e5-117">Indica que o parâmetro representa um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="0e0e5-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e0e5-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="0e0e5-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="0e0e5-119">4</span><span class="sxs-lookup"><span data-stu-id="0e0e5-119">4</span></span></p></td>
<td><p><span data-ttu-id="0e0e5-120">Indica que o parâmetro representa um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0e0e5-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e0e5-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="0e0e5-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="0e0e5-122">0</span><span class="sxs-lookup"><span data-stu-id="0e0e5-122">0</span></span></p></td>
<td><p><span data-ttu-id="0e0e5-123">Indica que a direção do parâmetro é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="0e0e5-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0e0e5-124">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0e0e5-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="0e0e5-125">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0e0e5-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e0e5-126">Constante</span><span class="sxs-lookup"><span data-stu-id="0e0e5-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e0e5-127">AdoEnums.ParameterDirection.INPUT</span><span class="sxs-lookup"><span data-stu-id="0e0e5-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e0e5-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e0e5-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e0e5-129">AdoEnums.ParameterDirection.OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e0e5-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e0e5-130">AdoEnums.ParameterDirection.RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="0e0e5-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e0e5-131">AdoEnums.ParameterDirection.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="0e0e5-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

