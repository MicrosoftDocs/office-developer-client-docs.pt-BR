---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ae3f65b42032e9a5d8f905516de080a9c575e5b
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863625"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="3a1fe-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="3a1fe-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="3a1fe-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a1fe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3a1fe-104">Especifica se [Parameter](parameter-object-ado.md) representa um parâmetro de entrada, de saída, ou ambos, ou o valor de retorno de um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="3a1fe-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a1fe-105">Constant</span><span class="sxs-lookup"><span data-stu-id="3a1fe-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3a1fe-106">Valor</span><span class="sxs-lookup"><span data-stu-id="3a1fe-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3a1fe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a1fe-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a1fe-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="3a1fe-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="3a1fe-109">1</span><span class="sxs-lookup"><span data-stu-id="3a1fe-109">1</span></span></p></td>
<td><p><span data-ttu-id="3a1fe-p101">Padrão. Indica que o parâmetro representa um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="3a1fe-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a1fe-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="3a1fe-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="3a1fe-113">3</span><span class="sxs-lookup"><span data-stu-id="3a1fe-113">3</span></span></p></td>
<td><p><span data-ttu-id="3a1fe-114">Indica que o parâmetro representa um parâmetro de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="3a1fe-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a1fe-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="3a1fe-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="3a1fe-116">2</span><span class="sxs-lookup"><span data-stu-id="3a1fe-116">2</span></span></p></td>
<td><p><span data-ttu-id="3a1fe-117">Indica que o parâmetro representa um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="3a1fe-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a1fe-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="3a1fe-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="3a1fe-119">4</span><span class="sxs-lookup"><span data-stu-id="3a1fe-119">4</span></span></p></td>
<td><p><span data-ttu-id="3a1fe-120">Indica que o parâmetro representa um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3a1fe-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a1fe-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="3a1fe-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="3a1fe-122">0</span><span class="sxs-lookup"><span data-stu-id="3a1fe-122">0</span></span></p></td>
<td><p><span data-ttu-id="3a1fe-123">Indica que a direção do parâmetro é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="3a1fe-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3a1fe-124">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="3a1fe-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="3a1fe-125">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="3a1fe-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a1fe-126">Constante</span><span class="sxs-lookup"><span data-stu-id="3a1fe-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a1fe-127">AdoEnums.ParameterDirection.INPUT</span><span class="sxs-lookup"><span data-stu-id="3a1fe-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a1fe-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a1fe-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a1fe-129">AdoEnums.ParameterDirection.OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a1fe-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a1fe-130">AdoEnums.ParameterDirection.RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="3a1fe-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a1fe-131">AdoEnums.ParameterDirection.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="3a1fe-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

