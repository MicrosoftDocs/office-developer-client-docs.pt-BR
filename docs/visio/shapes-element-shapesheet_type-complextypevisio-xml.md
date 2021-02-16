---
title: Elemento Shapes (ShapeSheet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contém uma coleção de elementos Shape.
ms.openlocfilehash: e9f45d1f61b83339274d24aea2c0473adf282bac
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542097"
---
# <a name="shapes-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="aab5b-103">Elemento Shapes (ShapeSheet_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="aab5b-103">Shapes element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="aab5b-104">Contém uma coleção de elementos Shape.</span><span class="sxs-lookup"><span data-stu-id="aab5b-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aab5b-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="aab5b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aab5b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="aab5b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="aab5b-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="aab5b-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="aab5b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aab5b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="aab5b-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="aab5b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="aab5b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="aab5b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="aab5b-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="aab5b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="aab5b-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="aab5b-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aab5b-113">Definição</span><span class="sxs-lookup"><span data-stu-id="aab5b-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aab5b-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="aab5b-114">Elements and attributes</span></span>

<span data-ttu-id="aab5b-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="aab5b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="aab5b-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="aab5b-116">Parent elements</span></span>

|<span data-ttu-id="aab5b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aab5b-117">**Element**</span></span>|<span data-ttu-id="aab5b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aab5b-118">**Type**</span></span>|<span data-ttu-id="aab5b-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aab5b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aab5b-120">Forma</span><span class="sxs-lookup"><span data-stu-id="aab5b-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aab5b-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="aab5b-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aab5b-122">Especifica uma coleção de propriedades associadas a uma forma.</span><span class="sxs-lookup"><span data-stu-id="aab5b-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="aab5b-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="aab5b-123">Child elements</span></span>

|<span data-ttu-id="aab5b-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aab5b-124">**Element**</span></span>|<span data-ttu-id="aab5b-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aab5b-125">**Type**</span></span>|<span data-ttu-id="aab5b-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aab5b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aab5b-127">Forma</span><span class="sxs-lookup"><span data-stu-id="aab5b-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aab5b-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="aab5b-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aab5b-129">Contém elementos que definem uma forma em um elemento **Master**, **Page** ou group shape.</span><span class="sxs-lookup"><span data-stu-id="aab5b-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="aab5b-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="aab5b-130">Attributes</span></span>

<span data-ttu-id="aab5b-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="aab5b-131">None.</span></span>
  

