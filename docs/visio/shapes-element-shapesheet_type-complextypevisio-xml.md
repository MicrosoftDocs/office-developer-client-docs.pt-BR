---
title: Elemento Shapes (ShapeSheet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contém uma coleção de elementos Shape.
ms.openlocfilehash: d4de4436079ec6290b52dd74bf3ee015c5b0d3f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348248"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="6b04c-103">Elemento Shapes (ShapeSheet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6b04c-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6b04c-104">Contém uma coleção de elementos Shape.</span><span class="sxs-lookup"><span data-stu-id="6b04c-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b04c-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="6b04c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b04c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6b04c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6b04c-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="6b04c-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6b04c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6b04c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6b04c-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6b04c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6b04c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6b04c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6b04c-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6b04c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6b04c-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="6b04c-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b04c-113">Definição</span><span class="sxs-lookup"><span data-stu-id="6b04c-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b04c-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6b04c-114">Elements and attributes</span></span>

<span data-ttu-id="6b04c-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6b04c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6b04c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6b04c-116">Parent elements</span></span>

|<span data-ttu-id="6b04c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6b04c-117">**Element**</span></span>|<span data-ttu-id="6b04c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6b04c-118">**Type**</span></span>|<span data-ttu-id="6b04c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6b04c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b04c-120">Forma</span><span class="sxs-lookup"><span data-stu-id="6b04c-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b04c-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6b04c-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b04c-122">Especifica uma coleção de propriedades associadas a uma forma.</span><span class="sxs-lookup"><span data-stu-id="6b04c-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6b04c-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6b04c-123">Child elements</span></span>

|<span data-ttu-id="6b04c-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6b04c-124">**Element**</span></span>|<span data-ttu-id="6b04c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6b04c-125">**Type**</span></span>|<span data-ttu-id="6b04c-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6b04c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b04c-127">Forma</span><span class="sxs-lookup"><span data-stu-id="6b04c-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b04c-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6b04c-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b04c-129">Contém elementos que definem uma forma em um elemento **Master**, **Page** ou group shape.</span><span class="sxs-lookup"><span data-stu-id="6b04c-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6b04c-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b04c-130">Attributes</span></span>

<span data-ttu-id="6b04c-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6b04c-131">None.</span></span>
  

