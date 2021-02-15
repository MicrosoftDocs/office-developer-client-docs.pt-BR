---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281898"
---
# <a name="adcprop_asyncthreadpriority_enum"></a><span data-ttu-id="2906a-102">ADCPROP \_ ASYNCTHREADPRIORITY \_ ENUM</span><span class="sxs-lookup"><span data-stu-id="2906a-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="2906a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2906a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2906a-104">Para um objeto do [Recordset](recordset-object-ado.md) RDS, especifica a prioridade de execução do encadeamento assíncrono que recupera os dados.</span><span class="sxs-lookup"><span data-stu-id="2906a-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="2906a-105">Use essas constantes com o **Recordset** da propriedade dinâmica "**Prioridade de Encadeamento em Segundo Plano**" , que referenciada no Índice de Propriedades Dinâmicas ADO e documentada no [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span><span class="sxs-lookup"><span data-stu-id="2906a-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2906a-106">Constant</span><span class="sxs-lookup"><span data-stu-id="2906a-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="2906a-107">Valor</span><span class="sxs-lookup"><span data-stu-id="2906a-107">Value</span></span></p></th>
<th><p><span data-ttu-id="2906a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2906a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2906a-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="2906a-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="2906a-110">4 </span><span class="sxs-lookup"><span data-stu-id="2906a-110">4</span></span></p></td>
<td><p><span data-ttu-id="2906a-111">Define a prioridade entre normal e mais alta.</span><span class="sxs-lookup"><span data-stu-id="2906a-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2906a-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="2906a-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="2906a-113">2 </span><span class="sxs-lookup"><span data-stu-id="2906a-113">2</span></span></p></td>
<td><p><span data-ttu-id="2906a-114">Define a prioridade entre mais baixa e normal.</span><span class="sxs-lookup"><span data-stu-id="2906a-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2906a-115"><strong>adPriorityHighest</strong></span><span class="sxs-lookup"><span data-stu-id="2906a-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="2906a-116">5 </span><span class="sxs-lookup"><span data-stu-id="2906a-116">5</span></span></p></td>
<td><p><span data-ttu-id="2906a-117">Define a prioridade para o valor mais alto possível.</span><span class="sxs-lookup"><span data-stu-id="2906a-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2906a-118"><strong>AdPriorityLowest</strong></span><span class="sxs-lookup"><span data-stu-id="2906a-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="2906a-119">1 </span><span class="sxs-lookup"><span data-stu-id="2906a-119">1</span></span></p></td>
<td><p><span data-ttu-id="2906a-120">Define a prioridade para o valor mais baixo possível.</span><span class="sxs-lookup"><span data-stu-id="2906a-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2906a-121"><strong>adPriorityNormal</strong></span><span class="sxs-lookup"><span data-stu-id="2906a-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="2906a-122">3 </span><span class="sxs-lookup"><span data-stu-id="2906a-122">3</span></span></p></td>
<td><p><span data-ttu-id="2906a-123">Define a prioridade como normal.</span><span class="sxs-lookup"><span data-stu-id="2906a-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="2906a-124">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2906a-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="2906a-125">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2906a-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2906a-126">Constant</span><span class="sxs-lookup"><span data-stu-id="2906a-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2906a-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span><span class="sxs-lookup"><span data-stu-id="2906a-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2906a-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="2906a-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2906a-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span><span class="sxs-lookup"><span data-stu-id="2906a-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2906a-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span><span class="sxs-lookup"><span data-stu-id="2906a-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2906a-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span><span class="sxs-lookup"><span data-stu-id="2906a-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

