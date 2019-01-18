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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717262"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="2f254-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="2f254-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="2f254-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f254-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f254-104">Especifica os atributos de um objeto [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2f254-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f254-105">Constant</span><span class="sxs-lookup"><span data-stu-id="2f254-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2f254-106">Valor</span><span class="sxs-lookup"><span data-stu-id="2f254-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2f254-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f254-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f254-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="2f254-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="2f254-109">0</span><span class="sxs-lookup"><span data-stu-id="2f254-109">0</span></span></p></td>
<td><p><span data-ttu-id="2f254-110">Indica que o provedor não oferece suporte para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="2f254-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f254-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="2f254-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="2f254-112">1</span><span class="sxs-lookup"><span data-stu-id="2f254-112">1</span></span></p></td>
<td><p><span data-ttu-id="2f254-113">Indica que o usuário deve especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="2f254-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f254-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="2f254-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="2f254-115">2</span><span class="sxs-lookup"><span data-stu-id="2f254-115">2</span></span></p></td>
<td><p><span data-ttu-id="2f254-116">Indica que o usuário não precisa especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="2f254-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f254-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="2f254-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="2f254-118">512</span><span class="sxs-lookup"><span data-stu-id="2f254-118">512</span></span></p></td>
<td><p><span data-ttu-id="2f254-119">Indica que o usuário pode ler a propriedade.</span><span class="sxs-lookup"><span data-stu-id="2f254-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f254-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="2f254-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="2f254-121">1024</span><span class="sxs-lookup"><span data-stu-id="2f254-121">1024</span></span></p></td>
<td><p><span data-ttu-id="2f254-122">Indica que o usuário pode definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="2f254-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2f254-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2f254-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="2f254-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2f254-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f254-125">Constante</span><span class="sxs-lookup"><span data-stu-id="2f254-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f254-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="2f254-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f254-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="2f254-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f254-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="2f254-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f254-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="2f254-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f254-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="2f254-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

