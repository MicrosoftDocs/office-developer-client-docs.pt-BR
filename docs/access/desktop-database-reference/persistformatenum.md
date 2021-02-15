---
title: PersistFormatEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4954c09c3eff67bb6f55dfc9e49464ad58fad5e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287605"
---
# <a name="persistformatenum"></a><span data-ttu-id="62476-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="62476-102">PersistFormatEnum</span></span>

<span data-ttu-id="62476-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62476-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62476-104">Especifica o formato no qual se deve salvar um [Recorset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="62476-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62476-105">Constant</span><span class="sxs-lookup"><span data-stu-id="62476-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="62476-106">Valor</span><span class="sxs-lookup"><span data-stu-id="62476-106">Value</span></span></p></th>
<th><p><span data-ttu-id="62476-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="62476-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62476-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="62476-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="62476-109">0</span><span class="sxs-lookup"><span data-stu-id="62476-109">0</span></span></p></td>
<td><p><span data-ttu-id="62476-110">Indica o formato Microsoft Advanced Data TableGram (ADTG).</span><span class="sxs-lookup"><span data-stu-id="62476-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62476-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="62476-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="62476-112">1 </span><span class="sxs-lookup"><span data-stu-id="62476-112">1</span></span></p></td>
<td><p><span data-ttu-id="62476-p101">Indica que será usado o formato Extensible Markup Language (XML) do próprio ADO. Este valor é igual a adPersistXML e é incluído para compatibilidade reversa.</span><span class="sxs-lookup"><span data-stu-id="62476-p101">Indicates that ADO's own Extensible Markup Language (XML) format will be used. This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62476-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="62476-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="62476-116">1 </span><span class="sxs-lookup"><span data-stu-id="62476-116">1</span></span></p></td>
<td><p><span data-ttu-id="62476-117">Indica o formato Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="62476-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62476-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="62476-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="62476-119">2 </span><span class="sxs-lookup"><span data-stu-id="62476-119">2</span></span></p></td>
<td><p><span data-ttu-id="62476-120">Indica que o provedor manterá o <strong>Recorset</strong> usando seu próprio formato.</span><span class="sxs-lookup"><span data-stu-id="62476-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="62476-121">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="62476-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="62476-122">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="62476-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62476-123">Constant</span><span class="sxs-lookup"><span data-stu-id="62476-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62476-124">AdoEnums.PersistFormat.ADTG</span><span class="sxs-lookup"><span data-stu-id="62476-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62476-125">AdoEnums.PersistFormat.XML</span><span class="sxs-lookup"><span data-stu-id="62476-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

