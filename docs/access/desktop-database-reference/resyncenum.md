---
title: ResyncEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 837bc16435ea574bd9d8e2e5e21ae50a4e852ee6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861075"
---
# <a name="resyncenum"></a><span data-ttu-id="5a851-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="5a851-102">ResyncEnum</span></span>

<span data-ttu-id="5a851-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a851-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5a851-104">Especifica se os valores subjacentes são sobregravados por uma chamada para [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5a851-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a851-105">Constant</span><span class="sxs-lookup"><span data-stu-id="5a851-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5a851-106">Valor</span><span class="sxs-lookup"><span data-stu-id="5a851-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5a851-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a851-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a851-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="5a851-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="5a851-109">2</span><span class="sxs-lookup"><span data-stu-id="5a851-109">2</span></span></p></td>
<td><p><span data-ttu-id="5a851-p101">Padrão. Sobregrava dados e as atualizações pendentes são canceladas.</span><span class="sxs-lookup"><span data-stu-id="5a851-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a851-112"><strong>adResyncUnderlyingValues</strong></span><span class="sxs-lookup"><span data-stu-id="5a851-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="5a851-113">1</span><span class="sxs-lookup"><span data-stu-id="5a851-113">1</span></span></p></td>
<td><p><span data-ttu-id="5a851-114">Não sobregrava os dados e as atualizações pendentes não são canceladas.</span><span class="sxs-lookup"><span data-stu-id="5a851-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="5a851-115">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="5a851-115">ADO/WFC equivalent</span></span>

<span data-ttu-id="5a851-116">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="5a851-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a851-117">Constante</span><span class="sxs-lookup"><span data-stu-id="5a851-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a851-118">AdoEnums.Resync.ALLVALUES</span><span class="sxs-lookup"><span data-stu-id="5a851-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a851-119">AdoEnums.Resync.UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="5a851-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

