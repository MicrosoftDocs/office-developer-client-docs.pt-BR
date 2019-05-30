---
title: Elemento PublishSettings (VisioDocument_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Especifica as configurações que são usadas quando o diagrama é aberto usando os serviços do Visio no Microsoft SharePoint Server 2013.
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541355"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="ceca3-103">Elemento PublishSettings (VisioDocument_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="ceca3-103">PublishSettings element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ceca3-104">Especifica as configurações que são usadas quando o diagrama é aberto usando os serviços do Visio no Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ceca3-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ceca3-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="ceca3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ceca3-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ceca3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ceca3-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ceca3-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ceca3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ceca3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ceca3-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ceca3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ceca3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ceca3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ceca3-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="ceca3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ceca3-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="ceca3-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ceca3-113">Definição</span><span class="sxs-lookup"><span data-stu-id="ceca3-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ceca3-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ceca3-114">Elements and attributes</span></span>

<span data-ttu-id="ceca3-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ceca3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ceca3-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ceca3-116">Parent elements</span></span>

|<span data-ttu-id="ceca3-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ceca3-117">**Element**</span></span>|<span data-ttu-id="ceca3-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ceca3-118">**Type**</span></span>|<span data-ttu-id="ceca3-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ceca3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ceca3-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="ceca3-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="ceca3-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="ceca3-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ceca3-122">Especifica as propriedades de um desenho.</span><span class="sxs-lookup"><span data-stu-id="ceca3-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ceca3-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ceca3-123">Child elements</span></span>

|<span data-ttu-id="ceca3-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ceca3-124">**Element**</span></span>|<span data-ttu-id="ceca3-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ceca3-125">**Type**</span></span>|<span data-ttu-id="ceca3-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ceca3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ceca3-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="ceca3-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ceca3-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="ceca3-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ceca3-129">Especifica se uma página de desenho é visível no navegador usando os serviços do Visio.</span><span class="sxs-lookup"><span data-stu-id="ceca3-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="ceca3-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="ceca3-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ceca3-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="ceca3-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ceca3-132">Especifica se um Recordset é atualizável usando os serviços do Visio.</span><span class="sxs-lookup"><span data-stu-id="ceca3-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ceca3-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="ceca3-133">Attributes</span></span>

<span data-ttu-id="ceca3-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ceca3-134">None.</span></span>
  

