---
title: elemento FLD (Text_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Indica um ponto de inserção de campo de texto para o elemento Field correspondente.
ms.openlocfilehash: a7303697a9471dab68f5b1cf851f60d51650a84e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346211"
---
# <a name="fld-element-texttype-complextype-visio-xml"></a><span data-ttu-id="6afa0-103">elemento FLD (Text_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6afa0-103">fld element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6afa0-104">Indica um ponto de inserção de campo de texto para o elemento **Field** correspondente.</span><span class="sxs-lookup"><span data-stu-id="6afa0-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6afa0-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="6afa0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6afa0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6afa0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6afa0-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="6afa0-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6afa0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6afa0-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6afa0-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6afa0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6afa0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6afa0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6afa0-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6afa0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6afa0-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="6afa0-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6afa0-113">Definição</span><span class="sxs-lookup"><span data-stu-id="6afa0-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6afa0-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6afa0-114">Elements and attributes</span></span>

<span data-ttu-id="6afa0-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6afa0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6afa0-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6afa0-116">Parent elements</span></span>

|<span data-ttu-id="6afa0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6afa0-117">**Element**</span></span>|<span data-ttu-id="6afa0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6afa0-118">**Type**</span></span>|<span data-ttu-id="6afa0-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6afa0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6afa0-120">Text</span><span class="sxs-lookup"><span data-stu-id="6afa0-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6afa0-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="6afa0-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6afa0-122">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="6afa0-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6afa0-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6afa0-123">Child elements</span></span>

<span data-ttu-id="6afa0-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6afa0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6afa0-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="6afa0-125">Attributes</span></span>

|<span data-ttu-id="6afa0-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6afa0-126">**Attribute**</span></span>|<span data-ttu-id="6afa0-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6afa0-127">**Type**</span></span>|<span data-ttu-id="6afa0-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="6afa0-128">**Required**</span></span>|<span data-ttu-id="6afa0-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6afa0-129">**Description**</span></span>|<span data-ttu-id="6afa0-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="6afa0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6afa0-131">IX</span><span class="sxs-lookup"><span data-stu-id="6afa0-131">IX</span></span>  <br/> |<span data-ttu-id="6afa0-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6afa0-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6afa0-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="6afa0-133">required</span></span>  <br/> |<span data-ttu-id="6afa0-134">O índices baseado em zero do elemento no seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="6afa0-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="6afa0-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6afa0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

