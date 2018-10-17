---
title: Elemento Data2 (ShapeSheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e823797e-dde9-6ee7-b5e4-9e57cef90b08
description: Contém um valor arbitrário de cadeia de caracteres usado para fornecer informações adicionais sobre uma forma.
ms.openlocfilehash: ebd70fc0f83bd7cbf0bd6465c5e06276675a8022
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401710"
---
# <a name="data2-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="5e7c1-103">Elemento Data2 (ShapeSheet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="5e7c1-103">Data2 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5e7c1-104">Contém um valor arbitrário de cadeia de caracteres usado para fornecer informações adicionais sobre uma forma.</span><span class="sxs-lookup"><span data-stu-id="5e7c1-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5e7c1-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="5e7c1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e7c1-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5e7c1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5e7c1-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="5e7c1-107">DataType</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5e7c1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5e7c1-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5e7c1-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5e7c1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5e7c1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5e7c1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5e7c1-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="5e7c1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5e7c1-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="5e7c1-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5e7c1-113">Definição</span><span class="sxs-lookup"><span data-stu-id="5e7c1-113">Definition</span></span>

```XML
< xs:element name="Data2" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5e7c1-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5e7c1-114">Elements and attributes</span></span>

<span data-ttu-id="5e7c1-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5e7c1-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5e7c1-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5e7c1-116">Parent elements</span></span>

|<span data-ttu-id="5e7c1-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5e7c1-117">**Element**</span></span>|<span data-ttu-id="5e7c1-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5e7c1-118">**Type**</span></span>|<span data-ttu-id="5e7c1-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5e7c1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5e7c1-120">Forma</span><span class="sxs-lookup"><span data-stu-id="5e7c1-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5e7c1-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="5e7c1-121">ShapeSheet_Type complexType</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5e7c1-122">Contém elementos que definem uma forma em um elemento **Master**, **Page** ou group shape.</span><span class="sxs-lookup"><span data-stu-id="5e7c1-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5e7c1-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5e7c1-123">Child elements</span></span>

<span data-ttu-id="5e7c1-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5e7c1-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e7c1-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e7c1-125">Attributes</span></span>

<span data-ttu-id="5e7c1-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5e7c1-126">None.</span></span>
  

