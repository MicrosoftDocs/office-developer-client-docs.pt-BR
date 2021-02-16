---
title: Elemento Text (ShapeSheet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contém o texto de uma forma.
ms.openlocfilehash: 4b03bc2539b80e49daae9d14f3e2ad07a51de9f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541922"
---
# <a name="text-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="028ca-103">Elemento Text (ShapeSheet_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="028ca-103">Text element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="028ca-104">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="028ca-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="028ca-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="028ca-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="028ca-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="028ca-106">**Element type**</span></span> <br/> |[<span data-ttu-id="028ca-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="028ca-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="028ca-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="028ca-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="028ca-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="028ca-109">**Schema file**</span></span> <br/> |<span data-ttu-id="028ca-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="028ca-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="028ca-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="028ca-111">**Document parts**</span></span> <br/> |<span data-ttu-id="028ca-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="028ca-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="028ca-113">Definição</span><span class="sxs-lookup"><span data-stu-id="028ca-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="028ca-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="028ca-114">Elements and attributes</span></span>

<span data-ttu-id="028ca-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="028ca-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="028ca-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="028ca-116">Parent elements</span></span>

|<span data-ttu-id="028ca-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="028ca-117">**Element**</span></span>|<span data-ttu-id="028ca-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="028ca-118">**Type**</span></span>|<span data-ttu-id="028ca-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="028ca-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="028ca-120">Forma</span><span class="sxs-lookup"><span data-stu-id="028ca-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="028ca-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="028ca-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="028ca-122">Contém elementos que definem uma forma em um elemento **Master**, **Page** ou group shape.</span><span class="sxs-lookup"><span data-stu-id="028ca-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="028ca-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="028ca-123">Child elements</span></span>

|<span data-ttu-id="028ca-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="028ca-124">**Element**</span></span>|<span data-ttu-id="028ca-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="028ca-125">**Type**</span></span>|<span data-ttu-id="028ca-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="028ca-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="028ca-127">cp</span><span class="sxs-lookup"><span data-stu-id="028ca-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="028ca-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="028ca-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="028ca-129">Marca o início de uma execução de propriedades de caracteres que é formatada de acordo com o elemento Char correspondente.</span><span class="sxs-lookup"><span data-stu-id="028ca-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="028ca-130">fld</span><span class="sxs-lookup"><span data-stu-id="028ca-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="028ca-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="028ca-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="028ca-132">Indica um ponto de inserção de campo de texto para o elemento Field correspondente.</span><span class="sxs-lookup"><span data-stu-id="028ca-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="028ca-133">pp</span><span class="sxs-lookup"><span data-stu-id="028ca-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="028ca-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="028ca-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="028ca-135">Especifica o início de uma série de propriedades de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="028ca-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="028ca-136">tp</span><span class="sxs-lookup"><span data-stu-id="028ca-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="028ca-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="028ca-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="028ca-138">Especifica o início de uma operação de propriedades de guias.</span><span class="sxs-lookup"><span data-stu-id="028ca-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="028ca-139">Atributos</span><span class="sxs-lookup"><span data-stu-id="028ca-139">Attributes</span></span>

<span data-ttu-id="028ca-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="028ca-140">None.</span></span>
  

