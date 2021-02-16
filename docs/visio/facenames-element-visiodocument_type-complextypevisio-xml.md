---
title: Elemento FaceNames (VisioDocument_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Contém uma coleção de elementos FaceName.
ms.openlocfilehash: ce18847fdd46a0c703a0df5e8d8c7a877f864d35
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539710"
---
# <a name="facenames-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="3fad7-103">Elemento FaceNames (VisioDocument_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="3fad7-103">FaceNames element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="3fad7-104">Contém uma coleção de elementos **FaceName**.</span><span class="sxs-lookup"><span data-stu-id="3fad7-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3fad7-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="3fad7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fad7-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3fad7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3fad7-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="3fad7-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3fad7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3fad7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3fad7-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3fad7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3fad7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3fad7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3fad7-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="3fad7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3fad7-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="3fad7-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3fad7-113">Definição</span><span class="sxs-lookup"><span data-stu-id="3fad7-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3fad7-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3fad7-114">Elements and attributes</span></span>

<span data-ttu-id="3fad7-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3fad7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3fad7-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3fad7-116">Parent elements</span></span>

|<span data-ttu-id="3fad7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3fad7-117">**Element**</span></span>|<span data-ttu-id="3fad7-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3fad7-118">**Type**</span></span>|<span data-ttu-id="3fad7-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3fad7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3fad7-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="3fad7-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="3fad7-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="3fad7-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3fad7-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="3fad7-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3fad7-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3fad7-123">Child elements</span></span>

|<span data-ttu-id="3fad7-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3fad7-124">**Element**</span></span>|<span data-ttu-id="3fad7-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3fad7-125">**Type**</span></span>|<span data-ttu-id="3fad7-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3fad7-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3fad7-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="3fad7-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3fad7-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="3fad7-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3fad7-129">Contém informações sobre uma fonte.</span><span class="sxs-lookup"><span data-stu-id="3fad7-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3fad7-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="3fad7-130">Attributes</span></span>

<span data-ttu-id="3fad7-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3fad7-131">None.</span></span>
  

