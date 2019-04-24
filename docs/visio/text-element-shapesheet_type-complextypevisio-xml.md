---
title: Elemento de texto (ShapeSheet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contém o texto de uma forma.
ms.openlocfilehash: f2c809d7db895a3635a5898d83d4583cd38f1249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332343"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="93340-103">Elemento de texto (ShapeSheet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="93340-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="93340-104">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="93340-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93340-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="93340-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93340-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="93340-106">**Element type**</span></span> <br/> |[<span data-ttu-id="93340-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="93340-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="93340-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="93340-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="93340-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="93340-109">**Schema file**</span></span> <br/> |<span data-ttu-id="93340-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="93340-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="93340-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="93340-111">**Document parts**</span></span> <br/> |<span data-ttu-id="93340-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="93340-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="93340-113">Definição</span><span class="sxs-lookup"><span data-stu-id="93340-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="93340-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="93340-114">Elements and attributes</span></span>

<span data-ttu-id="93340-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="93340-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="93340-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="93340-116">Parent elements</span></span>

|<span data-ttu-id="93340-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="93340-117">**Element**</span></span>|<span data-ttu-id="93340-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="93340-118">**Type**</span></span>|<span data-ttu-id="93340-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="93340-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="93340-120">Forma</span><span class="sxs-lookup"><span data-stu-id="93340-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93340-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="93340-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93340-122">Contém elementos que definem uma forma em um elemento **Master**, **Page** ou group shape.</span><span class="sxs-lookup"><span data-stu-id="93340-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="93340-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="93340-123">Child elements</span></span>

|<span data-ttu-id="93340-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="93340-124">**Element**</span></span>|<span data-ttu-id="93340-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="93340-125">**Type**</span></span>|<span data-ttu-id="93340-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="93340-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="93340-127">CP</span><span class="sxs-lookup"><span data-stu-id="93340-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93340-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="93340-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93340-129">Marca o início de uma execução de propriedades de caracteres que é formatada de acordo com o elemento Char correspondente.</span><span class="sxs-lookup"><span data-stu-id="93340-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="93340-130">FLD</span><span class="sxs-lookup"><span data-stu-id="93340-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93340-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="93340-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93340-132">Indica um ponto de inserção de campo de texto para o elemento Field correspondente.</span><span class="sxs-lookup"><span data-stu-id="93340-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="93340-133">páginas</span><span class="sxs-lookup"><span data-stu-id="93340-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93340-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="93340-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93340-135">Especifica o início de uma execução de propriedades de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="93340-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="93340-136">par</span><span class="sxs-lookup"><span data-stu-id="93340-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93340-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="93340-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93340-138">Especifica o início de uma propriedade de guias executada.</span><span class="sxs-lookup"><span data-stu-id="93340-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="93340-139">Atributos</span><span class="sxs-lookup"><span data-stu-id="93340-139">Attributes</span></span>

<span data-ttu-id="93340-140">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="93340-140">None.</span></span>
  

