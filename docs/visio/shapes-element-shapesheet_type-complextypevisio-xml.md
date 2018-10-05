---
title: Elemento de formas (ShapeSheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contém uma coleção de elementos de forma.
ms.openlocfilehash: d4de4436079ec6290b52dd74bf3ee015c5b0d3f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392092"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="dcb49-103">Elemento de formas (ShapeSheet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="dcb49-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="dcb49-104">Contém uma coleção de elementos de forma.</span><span class="sxs-lookup"><span data-stu-id="dcb49-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dcb49-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="dcb49-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcb49-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="dcb49-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dcb49-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="dcb49-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dcb49-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dcb49-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dcb49-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dcb49-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dcb49-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="dcb49-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dcb49-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="dcb49-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dcb49-112">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="dcb49-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dcb49-113">Definição</span><span class="sxs-lookup"><span data-stu-id="dcb49-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dcb49-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="dcb49-114">Elements and attributes</span></span>

<span data-ttu-id="dcb49-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="dcb49-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dcb49-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="dcb49-116">Parent elements</span></span>

|<span data-ttu-id="dcb49-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dcb49-117">**Element**</span></span>|<span data-ttu-id="dcb49-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dcb49-118">**Type**</span></span>|<span data-ttu-id="dcb49-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dcb49-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dcb49-120">Shape</span><span class="sxs-lookup"><span data-stu-id="dcb49-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dcb49-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="dcb49-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dcb49-122">Especifica um conjunto de propriedades associadas a uma forma.</span><span class="sxs-lookup"><span data-stu-id="dcb49-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dcb49-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="dcb49-123">Child elements</span></span>

|<span data-ttu-id="dcb49-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dcb49-124">**Element**</span></span>|<span data-ttu-id="dcb49-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dcb49-125">**Type**</span></span>|<span data-ttu-id="dcb49-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dcb49-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dcb49-127">Shape</span><span class="sxs-lookup"><span data-stu-id="dcb49-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dcb49-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="dcb49-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dcb49-129">Contém os elementos que definem a uma forma em um **mestre**, **página**ou elemento de forma do grupo.</span><span class="sxs-lookup"><span data-stu-id="dcb49-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="dcb49-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="dcb49-130">Attributes</span></span>

<span data-ttu-id="dcb49-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="dcb49-131">None.</span></span>
  

