---
title: Elemento PublishSettings (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Especifica as configurações que são usadas quando o diagrama é aberto usando os serviços do Visio no Microsoft SharePoint Server 2013.
ms.openlocfilehash: f2554facc47de23104f65b26ae19cfc71821bd37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772623"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="24161-103">Elemento PublishSettings (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="24161-103">PublishSettings element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="24161-104">Especifica as configurações que são usadas quando o diagrama é aberto usando os serviços do Visio no Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="24161-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24161-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="24161-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24161-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="24161-106">**Element type**</span></span> <br/> |[<span data-ttu-id="24161-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="24161-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="24161-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="24161-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="24161-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="24161-109">**Schema file**</span></span> <br/> |<span data-ttu-id="24161-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="24161-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="24161-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="24161-111">**Document parts**</span></span> <br/> |<span data-ttu-id="24161-112">Document</span><span class="sxs-lookup"><span data-stu-id="24161-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="24161-113">Definição</span><span class="sxs-lookup"><span data-stu-id="24161-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="24161-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="24161-114">Elements and attributes</span></span>

<span data-ttu-id="24161-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="24161-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="24161-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="24161-116">Parent elements</span></span>

|<span data-ttu-id="24161-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="24161-117">**Element**</span></span>|<span data-ttu-id="24161-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="24161-118">**Type**</span></span>|<span data-ttu-id="24161-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="24161-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="24161-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="24161-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="24161-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="24161-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24161-122">Especifica as propriedades de um desenho.</span><span class="sxs-lookup"><span data-stu-id="24161-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="24161-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="24161-123">Child elements</span></span>

|<span data-ttu-id="24161-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="24161-124">**Element**</span></span>|<span data-ttu-id="24161-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="24161-125">**Type**</span></span>|<span data-ttu-id="24161-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="24161-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="24161-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="24161-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24161-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="24161-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24161-129">Especifica se uma página de desenho é exibida no navegador usando os serviços do Visio.</span><span class="sxs-lookup"><span data-stu-id="24161-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="24161-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="24161-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="24161-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="24161-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="24161-132">Especifica se um conjunto de registros é atualizável usando os serviços do Visio.</span><span class="sxs-lookup"><span data-stu-id="24161-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="24161-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="24161-133">Attributes</span></span>

<span data-ttu-id="24161-134">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="24161-134">None.</span></span>
  

