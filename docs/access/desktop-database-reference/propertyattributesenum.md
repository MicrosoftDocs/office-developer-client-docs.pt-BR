---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f01efcc98ed12858712c28f080fb066d3dc1b41
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463245"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="3fff1-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="3fff1-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="3fff1-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fff1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3fff1-104">Especifica os atributos de um objeto [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3fff1-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fff1-105">Constant</span><span class="sxs-lookup"><span data-stu-id="3fff1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3fff1-106">Valor</span><span class="sxs-lookup"><span data-stu-id="3fff1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3fff1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fff1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fff1-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="3fff1-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="3fff1-109">0</span><span class="sxs-lookup"><span data-stu-id="3fff1-109">0</span></span></p></td>
<td><p><span data-ttu-id="3fff1-110">Indica que o provedor não oferece suporte para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="3fff1-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fff1-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="3fff1-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="3fff1-112">1</span><span class="sxs-lookup"><span data-stu-id="3fff1-112">1</span></span></p></td>
<td><p><span data-ttu-id="3fff1-113">Indica que o usuário deve especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="3fff1-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fff1-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="3fff1-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="3fff1-115">2</span><span class="sxs-lookup"><span data-stu-id="3fff1-115">2</span></span></p></td>
<td><p><span data-ttu-id="3fff1-116">Indica que o usuário não precisa especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="3fff1-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fff1-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="3fff1-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="3fff1-118">512</span><span class="sxs-lookup"><span data-stu-id="3fff1-118">512</span></span></p></td>
<td><p><span data-ttu-id="3fff1-119">Indica que o usuário pode ler a propriedade.</span><span class="sxs-lookup"><span data-stu-id="3fff1-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fff1-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="3fff1-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="3fff1-121">1024</span><span class="sxs-lookup"><span data-stu-id="3fff1-121">1024</span></span></p></td>
<td><p><span data-ttu-id="3fff1-122">Indica que o usuário pode definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="3fff1-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3fff1-123">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="3fff1-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="3fff1-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="3fff1-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fff1-125">Constante</span><span class="sxs-lookup"><span data-stu-id="3fff1-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fff1-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="3fff1-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fff1-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="3fff1-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fff1-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="3fff1-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fff1-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="3fff1-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fff1-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="3fff1-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

