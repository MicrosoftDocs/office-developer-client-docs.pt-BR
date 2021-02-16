---
title: Elemento Shapes (PageContents_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Contém uma coleção de elementos Shape.
ms.openlocfilehash: 5d248dd2683a1ccc153d15477c888e1b13d24d0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542118"
---
# <a name="shapes-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="6f173-103">Elemento Shapes (PageContents_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="6f173-103">Shapes element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6f173-104">Contém uma coleção de elementos Shape.</span><span class="sxs-lookup"><span data-stu-id="6f173-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f173-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="6f173-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f173-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6f173-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6f173-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="6f173-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6f173-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6f173-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6f173-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6f173-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6f173-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6f173-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6f173-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6f173-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6f173-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="6f173-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6f173-113">Definição</span><span class="sxs-lookup"><span data-stu-id="6f173-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6f173-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6f173-114">Elements and attributes</span></span>

<span data-ttu-id="6f173-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6f173-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6f173-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6f173-116">Parent elements</span></span>

|<span data-ttu-id="6f173-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f173-117">**Element**</span></span>|<span data-ttu-id="6f173-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6f173-118">**Type**</span></span>|<span data-ttu-id="6f173-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6f173-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6f173-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="6f173-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="6f173-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="6f173-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6f173-122">Especifica informações sobre as formas em um mestre em um desenho da Web.</span><span class="sxs-lookup"><span data-stu-id="6f173-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="6f173-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="6f173-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="6f173-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="6f173-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6f173-125">Especifica informações sobre as formas em um mestre em um desenho da Web.</span><span class="sxs-lookup"><span data-stu-id="6f173-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6f173-126">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6f173-126">Child elements</span></span>

|<span data-ttu-id="6f173-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f173-127">**Element**</span></span>|<span data-ttu-id="6f173-128">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6f173-128">**Type**</span></span>|<span data-ttu-id="6f173-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6f173-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6f173-130">Forma</span><span class="sxs-lookup"><span data-stu-id="6f173-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6f173-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6f173-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6f173-132">Contém elementos que definem uma forma em um elemento **Master**, **Page** ou group shape.</span><span class="sxs-lookup"><span data-stu-id="6f173-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6f173-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f173-133">Attributes</span></span>

<span data-ttu-id="6f173-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6f173-134">None.</span></span>
  

