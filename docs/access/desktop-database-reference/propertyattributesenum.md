---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c929bcf5dc7f5267c2e7d3a8dac5ed6bfb55b20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302873"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="0e9b9-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="0e9b9-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="0e9b9-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e9b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e9b9-104">Especifica os atributos de um objeto [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0e9b9-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e9b9-105">Constant</span><span class="sxs-lookup"><span data-stu-id="0e9b9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0e9b9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="0e9b9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0e9b9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e9b9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e9b9-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="0e9b9-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9b9-109">0</span><span class="sxs-lookup"><span data-stu-id="0e9b9-109">0</span></span></p></td>
<td><p><span data-ttu-id="0e9b9-110">Indica que o provedor não oferece suporte para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="0e9b9-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e9b9-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="0e9b9-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9b9-112">1 </span><span class="sxs-lookup"><span data-stu-id="0e9b9-112">1</span></span></p></td>
<td><p><span data-ttu-id="0e9b9-113">Indica que o usuário deve especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="0e9b9-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e9b9-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="0e9b9-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9b9-115">2 </span><span class="sxs-lookup"><span data-stu-id="0e9b9-115">2</span></span></p></td>
<td><p><span data-ttu-id="0e9b9-116">Indica que o usuário não precisa especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="0e9b9-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e9b9-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="0e9b9-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9b9-118">512</span><span class="sxs-lookup"><span data-stu-id="0e9b9-118">512</span></span></p></td>
<td><p><span data-ttu-id="0e9b9-119">Indica que o usuário pode ler a propriedade.</span><span class="sxs-lookup"><span data-stu-id="0e9b9-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e9b9-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="0e9b9-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9b9-121">1024</span><span class="sxs-lookup"><span data-stu-id="0e9b9-121">1024</span></span></p></td>
<td><p><span data-ttu-id="0e9b9-122">Indica que o usuário pode definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="0e9b9-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0e9b9-123">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0e9b9-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="0e9b9-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0e9b9-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e9b9-125">Constant</span><span class="sxs-lookup"><span data-stu-id="0e9b9-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e9b9-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="0e9b9-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e9b9-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="0e9b9-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e9b9-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="0e9b9-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e9b9-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="0e9b9-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e9b9-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="0e9b9-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

