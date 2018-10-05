---
title: Elemento de formas (PageContents_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Contém uma coleção de elementos de forma.
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397566"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="1de81-103">Elemento de formas (PageContents_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1de81-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1de81-104">Contém uma coleção de elementos de forma.</span><span class="sxs-lookup"><span data-stu-id="1de81-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1de81-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="1de81-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1de81-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1de81-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1de81-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="1de81-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1de81-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1de81-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1de81-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1de81-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1de81-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1de81-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1de81-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="1de81-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1de81-112">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="1de81-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1de81-113">Definição</span><span class="sxs-lookup"><span data-stu-id="1de81-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1de81-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1de81-114">Elements and attributes</span></span>

<span data-ttu-id="1de81-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1de81-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1de81-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1de81-116">Parent elements</span></span>

|<span data-ttu-id="1de81-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1de81-117">**Element**</span></span>|<span data-ttu-id="1de81-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1de81-118">**Type**</span></span>|<span data-ttu-id="1de81-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1de81-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1de81-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="1de81-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="1de81-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="1de81-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1de81-122">Especifica informações sobre as formas em um mestre em um desenho da Web.</span><span class="sxs-lookup"><span data-stu-id="1de81-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="1de81-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="1de81-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="1de81-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="1de81-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1de81-125">Especifica informações sobre as formas em um mestre em um desenho da Web.</span><span class="sxs-lookup"><span data-stu-id="1de81-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1de81-126">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1de81-126">Child elements</span></span>

|<span data-ttu-id="1de81-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1de81-127">**Element**</span></span>|<span data-ttu-id="1de81-128">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1de81-128">**Type**</span></span>|<span data-ttu-id="1de81-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1de81-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1de81-130">Shape</span><span class="sxs-lookup"><span data-stu-id="1de81-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1de81-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="1de81-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1de81-132">Contém os elementos que definem a uma forma em um **mestre**, **página**ou elemento de forma do grupo.</span><span class="sxs-lookup"><span data-stu-id="1de81-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1de81-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="1de81-133">Attributes</span></span>

<span data-ttu-id="1de81-134">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1de81-134">None.</span></span>
  

