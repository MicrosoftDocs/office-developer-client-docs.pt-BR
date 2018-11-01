---
title: ResyncEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: d75ae42d5d3b63e1eea56153ef8e2dd2fb366a30
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870062"
---
# <a name="resyncenum"></a><span data-ttu-id="1e49e-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="1e49e-102">ResyncEnum</span></span>

<span data-ttu-id="1e49e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e49e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e49e-104">Especifica se os valores subjacentes são sobregravados por uma chamada para [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1e49e-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e49e-105">Constant</span><span class="sxs-lookup"><span data-stu-id="1e49e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1e49e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="1e49e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1e49e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e49e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e49e-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="1e49e-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="1e49e-109">2</span><span class="sxs-lookup"><span data-stu-id="1e49e-109">2</span></span></p></td>
<td><p><span data-ttu-id="1e49e-p101">Padrão. Sobregrava dados e as atualizações pendentes são canceladas.</span><span class="sxs-lookup"><span data-stu-id="1e49e-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e49e-112"><strong>adResyncUnderlyingValues</strong></span><span class="sxs-lookup"><span data-stu-id="1e49e-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="1e49e-113">1</span><span class="sxs-lookup"><span data-stu-id="1e49e-113">1</span></span></p></td>
<td><p><span data-ttu-id="1e49e-114">Não sobregrava os dados e as atualizações pendentes não são canceladas.</span><span class="sxs-lookup"><span data-stu-id="1e49e-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1e49e-115">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1e49e-115">ADO/WFC equivalent</span></span>

<span data-ttu-id="1e49e-116">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1e49e-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e49e-117">Constante</span><span class="sxs-lookup"><span data-stu-id="1e49e-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e49e-118">AdoEnums.Resync.ALLVALUES</span><span class="sxs-lookup"><span data-stu-id="1e49e-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e49e-119">AdoEnums.Resync.UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="1e49e-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

