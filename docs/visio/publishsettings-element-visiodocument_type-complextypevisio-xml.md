---
title: Elemento PublishSettings (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Especifica as configurações que são usadas quando o diagrama é aberto usando os serviços do Visio no Microsoft SharePoint Server 2013.
ms.openlocfilehash: 7e926021180d0f32c5e8754fd856081908f4925d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345455"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="20255-103">Elemento PublishSettings (VisioDocument_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="20255-103">PublishSettings element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="20255-104">Especifica as configurações que são usadas quando o diagrama é aberto usando os serviços do Visio no Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20255-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20255-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="20255-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20255-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="20255-106">**Element type**</span></span> <br/> |[<span data-ttu-id="20255-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="20255-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="20255-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="20255-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="20255-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="20255-109">**Schema file**</span></span> <br/> |<span data-ttu-id="20255-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="20255-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="20255-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="20255-111">**Document parts**</span></span> <br/> |<span data-ttu-id="20255-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="20255-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="20255-113">Definição</span><span class="sxs-lookup"><span data-stu-id="20255-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="20255-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="20255-114">Elements and attributes</span></span>

<span data-ttu-id="20255-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="20255-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="20255-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="20255-116">Parent elements</span></span>

|<span data-ttu-id="20255-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="20255-117">**Element**</span></span>|<span data-ttu-id="20255-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="20255-118">**Type**</span></span>|<span data-ttu-id="20255-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20255-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="20255-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="20255-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="20255-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="20255-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20255-122">Especifica as propriedades de um desenho.</span><span class="sxs-lookup"><span data-stu-id="20255-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="20255-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="20255-123">Child elements</span></span>

|<span data-ttu-id="20255-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="20255-124">**Element**</span></span>|<span data-ttu-id="20255-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="20255-125">**Type**</span></span>|<span data-ttu-id="20255-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20255-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="20255-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="20255-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="20255-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="20255-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20255-129">Especifica se uma página de desenho é visível no navegador usando os serviços do Visio.</span><span class="sxs-lookup"><span data-stu-id="20255-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="20255-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="20255-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="20255-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="20255-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20255-132">Especifica se um Recordset é atualizável usando os serviços do Visio.</span><span class="sxs-lookup"><span data-stu-id="20255-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="20255-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="20255-133">Attributes</span></span>

<span data-ttu-id="20255-134">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="20255-134">None.</span></span>
  

