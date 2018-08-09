---
title: Elemento de texto (ShapeSheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contém o texto de uma forma.
ms.openlocfilehash: 636f349b0a93719cd157db563b238147af5584cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773105"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="67d80-103">Elemento de texto (ShapeSheet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="67d80-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="67d80-104">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="67d80-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67d80-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="67d80-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67d80-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="67d80-106">**Element type**</span></span> <br/> |[<span data-ttu-id="67d80-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="67d80-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="67d80-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="67d80-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="67d80-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="67d80-109">**Schema file**</span></span> <br/> |<span data-ttu-id="67d80-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="67d80-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="67d80-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="67d80-111">**Document parts**</span></span> <br/> |<span data-ttu-id="67d80-112">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="67d80-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67d80-113">Definição</span><span class="sxs-lookup"><span data-stu-id="67d80-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="67d80-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="67d80-114">Elements and attributes</span></span>

<span data-ttu-id="67d80-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="67d80-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="67d80-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="67d80-116">Parent elements</span></span>

|<span data-ttu-id="67d80-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="67d80-117">**Element**</span></span>|<span data-ttu-id="67d80-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67d80-118">**Type**</span></span>|<span data-ttu-id="67d80-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="67d80-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67d80-120">Shape</span><span class="sxs-lookup"><span data-stu-id="67d80-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67d80-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="67d80-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67d80-122">Contém os elementos que definem a uma forma em um **mestre**, **página**ou elemento de forma do grupo.</span><span class="sxs-lookup"><span data-stu-id="67d80-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67d80-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="67d80-123">Child elements</span></span>

|<span data-ttu-id="67d80-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="67d80-124">**Element**</span></span>|<span data-ttu-id="67d80-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67d80-125">**Type**</span></span>|<span data-ttu-id="67d80-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="67d80-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67d80-127">CP</span><span class="sxs-lookup"><span data-stu-id="67d80-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67d80-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="67d80-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67d80-129">Marca o início das propriedades de um caractere ou seja executado formatado de acordo com o elemento Char correspondente.</span><span class="sxs-lookup"><span data-stu-id="67d80-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="67d80-130">fld</span><span class="sxs-lookup"><span data-stu-id="67d80-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67d80-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="67d80-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67d80-132">Indica um ponto de inserção do campo de texto para o elemento do campo correspondente.</span><span class="sxs-lookup"><span data-stu-id="67d80-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="67d80-133">PP</span><span class="sxs-lookup"><span data-stu-id="67d80-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67d80-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="67d80-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67d80-135">Especifica o início das propriedades de um parágrafo é executado.</span><span class="sxs-lookup"><span data-stu-id="67d80-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="67d80-136">PA</span><span class="sxs-lookup"><span data-stu-id="67d80-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67d80-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="67d80-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67d80-138">Especifica o início de propriedades guias executar.</span><span class="sxs-lookup"><span data-stu-id="67d80-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="67d80-139">Atributos</span><span class="sxs-lookup"><span data-stu-id="67d80-139">Attributes</span></span>

<span data-ttu-id="67d80-140">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="67d80-140">None.</span></span>
  

