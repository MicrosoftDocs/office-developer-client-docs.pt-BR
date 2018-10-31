---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2567d07ad33670fcd68be4513d7a409ffdcd599c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864043"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="ae8c5-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="ae8c5-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="ae8c5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae8c5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ae8c5-104">Especifica os atributos de um objeto [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ae8c5-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae8c5-105">Constant</span><span class="sxs-lookup"><span data-stu-id="ae8c5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ae8c5-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ae8c5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ae8c5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae8c5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae8c5-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="ae8c5-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="ae8c5-109">0</span><span class="sxs-lookup"><span data-stu-id="ae8c5-109">0</span></span></p></td>
<td><p><span data-ttu-id="ae8c5-110">Indica que o provedor não oferece suporte para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="ae8c5-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae8c5-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="ae8c5-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="ae8c5-112">1</span><span class="sxs-lookup"><span data-stu-id="ae8c5-112">1</span></span></p></td>
<td><p><span data-ttu-id="ae8c5-113">Indica que o usuário deve especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="ae8c5-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae8c5-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="ae8c5-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="ae8c5-115">2</span><span class="sxs-lookup"><span data-stu-id="ae8c5-115">2</span></span></p></td>
<td><p><span data-ttu-id="ae8c5-116">Indica que o usuário não precisa especificar um valor para essa propriedade antes de a fonte de dados ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="ae8c5-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae8c5-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="ae8c5-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="ae8c5-118">512</span><span class="sxs-lookup"><span data-stu-id="ae8c5-118">512</span></span></p></td>
<td><p><span data-ttu-id="ae8c5-119">Indica que o usuário pode ler a propriedade.</span><span class="sxs-lookup"><span data-stu-id="ae8c5-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae8c5-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="ae8c5-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="ae8c5-121">1024</span><span class="sxs-lookup"><span data-stu-id="ae8c5-121">1024</span></span></p></td>
<td><p><span data-ttu-id="ae8c5-122">Indica que o usuário pode definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="ae8c5-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ae8c5-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ae8c5-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="ae8c5-124">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ae8c5-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae8c5-125">Constante</span><span class="sxs-lookup"><span data-stu-id="ae8c5-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae8c5-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ae8c5-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae8c5-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="ae8c5-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae8c5-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="ae8c5-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae8c5-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="ae8c5-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae8c5-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="ae8c5-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

