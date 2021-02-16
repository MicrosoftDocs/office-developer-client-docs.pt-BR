---
title: elemento fld (Text_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Indica um ponto de inserção de campo de texto para o elemento Field correspondente.
ms.openlocfilehash: efacb7ed11968dec5d5c2f62b0ca3e3bcd8580c0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539611"
---
# <a name="fld-element-text_type-complextype-visio-xml"></a><span data-ttu-id="af5c9-103">elemento fld (Text_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="af5c9-103">fld element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="af5c9-104">Indica um ponto de inserção de campo de texto para o elemento **Field** correspondente.</span><span class="sxs-lookup"><span data-stu-id="af5c9-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="af5c9-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="af5c9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af5c9-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="af5c9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="af5c9-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="af5c9-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="af5c9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="af5c9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="af5c9-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="af5c9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="af5c9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="af5c9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="af5c9-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="af5c9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="af5c9-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="af5c9-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="af5c9-113">Definição</span><span class="sxs-lookup"><span data-stu-id="af5c9-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="af5c9-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="af5c9-114">Elements and attributes</span></span>

<span data-ttu-id="af5c9-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="af5c9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="af5c9-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="af5c9-116">Parent elements</span></span>

|<span data-ttu-id="af5c9-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="af5c9-117">**Element**</span></span>|<span data-ttu-id="af5c9-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="af5c9-118">**Type**</span></span>|<span data-ttu-id="af5c9-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="af5c9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="af5c9-120">Text</span><span class="sxs-lookup"><span data-stu-id="af5c9-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af5c9-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="af5c9-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="af5c9-122">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="af5c9-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="af5c9-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="af5c9-123">Child elements</span></span>

<span data-ttu-id="af5c9-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="af5c9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af5c9-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="af5c9-125">Attributes</span></span>

|<span data-ttu-id="af5c9-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="af5c9-126">**Attribute**</span></span>|<span data-ttu-id="af5c9-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="af5c9-127">**Type**</span></span>|<span data-ttu-id="af5c9-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="af5c9-128">**Required**</span></span>|<span data-ttu-id="af5c9-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="af5c9-129">**Description**</span></span>|<span data-ttu-id="af5c9-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="af5c9-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="af5c9-131">IX</span><span class="sxs-lookup"><span data-stu-id="af5c9-131">IX</span></span>  <br/> |<span data-ttu-id="af5c9-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="af5c9-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af5c9-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="af5c9-133">required</span></span>  <br/> |<span data-ttu-id="af5c9-134">O índices baseado em zero do elemento no seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="af5c9-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="af5c9-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="af5c9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

