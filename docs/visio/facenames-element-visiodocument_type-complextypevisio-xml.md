---
title: Elemento FaceNames (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Contém uma coleção de elementos de FaceName.
ms.openlocfilehash: 5d6f2ffbf54dd04e744e85909fbc8a6bd4a387a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386814"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="7aceb-103">Elemento FaceNames (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7aceb-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7aceb-104">Contém uma coleção de elementos de **FaceName** .</span><span class="sxs-lookup"><span data-stu-id="7aceb-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7aceb-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="7aceb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7aceb-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7aceb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7aceb-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="7aceb-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7aceb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7aceb-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7aceb-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7aceb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7aceb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7aceb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7aceb-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="7aceb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7aceb-112">Document</span><span class="sxs-lookup"><span data-stu-id="7aceb-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7aceb-113">Definição</span><span class="sxs-lookup"><span data-stu-id="7aceb-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7aceb-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7aceb-114">Elements and attributes</span></span>

<span data-ttu-id="7aceb-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7aceb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7aceb-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7aceb-116">Parent elements</span></span>

|<span data-ttu-id="7aceb-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7aceb-117">**Element**</span></span>|<span data-ttu-id="7aceb-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7aceb-118">**Type**</span></span>|<span data-ttu-id="7aceb-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7aceb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7aceb-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="7aceb-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="7aceb-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="7aceb-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7aceb-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="7aceb-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7aceb-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7aceb-123">Child elements</span></span>

|<span data-ttu-id="7aceb-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7aceb-124">**Element**</span></span>|<span data-ttu-id="7aceb-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7aceb-125">**Type**</span></span>|<span data-ttu-id="7aceb-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7aceb-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7aceb-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="7aceb-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7aceb-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="7aceb-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7aceb-129">Contém informações sobre uma fonte.</span><span class="sxs-lookup"><span data-stu-id="7aceb-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7aceb-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="7aceb-130">Attributes</span></span>

<span data-ttu-id="7aceb-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7aceb-131">None.</span></span>
  

