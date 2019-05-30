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
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="fbb2f-103">Elemento FaceNames (VisioDocument_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="fbb2f-103">FaceNames element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fbb2f-104">Contém uma coleção de elementos **FaceName**.</span><span class="sxs-lookup"><span data-stu-id="fbb2f-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fbb2f-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="fbb2f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbb2f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fbb2f-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="fbb2f-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fbb2f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fbb2f-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fbb2f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fbb2f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fbb2f-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fbb2f-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="fbb2f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fbb2f-113">Definição</span><span class="sxs-lookup"><span data-stu-id="fbb2f-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fbb2f-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fbb2f-114">Elements and attributes</span></span>

<span data-ttu-id="fbb2f-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fbb2f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fbb2f-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fbb2f-116">Parent elements</span></span>

|<span data-ttu-id="fbb2f-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-117">**Element**</span></span>|<span data-ttu-id="fbb2f-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-118">**Type**</span></span>|<span data-ttu-id="fbb2f-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fbb2f-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="fbb2f-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="fbb2f-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="fbb2f-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fbb2f-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="fbb2f-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fbb2f-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fbb2f-123">Child elements</span></span>

|<span data-ttu-id="fbb2f-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-124">**Element**</span></span>|<span data-ttu-id="fbb2f-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-125">**Type**</span></span>|<span data-ttu-id="fbb2f-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbb2f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fbb2f-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="fbb2f-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fbb2f-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="fbb2f-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fbb2f-129">Contém informações sobre uma fonte.</span><span class="sxs-lookup"><span data-stu-id="fbb2f-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fbb2f-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbb2f-130">Attributes</span></span>

<span data-ttu-id="fbb2f-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fbb2f-131">None.</span></span>
  

