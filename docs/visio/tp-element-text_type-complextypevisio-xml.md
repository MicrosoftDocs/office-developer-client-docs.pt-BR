---
title: elemento TP (Text_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Especifica o início de uma propriedade de guias executada. A execução é definida para o final do texto ou até a próxima marcação.
ms.openlocfilehash: 3f27ea0babefa0ea69cbbc361031c57602649107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307697"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="9e6d0-104">elemento TP (Text_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9e6d0-104">tp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9e6d0-105">Especifica o início de uma propriedade de guias executada.</span><span class="sxs-lookup"><span data-stu-id="9e6d0-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="9e6d0-106">A execução é definida para o final do texto ou até a próxima marcação.</span><span class="sxs-lookup"><span data-stu-id="9e6d0-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e6d0-107">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="9e6d0-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e6d0-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-108">**Element type**</span></span> <br/> |[<span data-ttu-id="9e6d0-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="9e6d0-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9e6d0-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9e6d0-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-111">**Schema file**</span></span> <br/> |<span data-ttu-id="9e6d0-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9e6d0-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9e6d0-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-113">**Document parts**</span></span> <br/> |<span data-ttu-id="9e6d0-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="9e6d0-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9e6d0-115">Definição</span><span class="sxs-lookup"><span data-stu-id="9e6d0-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9e6d0-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9e6d0-116">Elements and attributes</span></span>

<span data-ttu-id="9e6d0-117">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9e6d0-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9e6d0-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9e6d0-118">Parent elements</span></span>

|<span data-ttu-id="9e6d0-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-119">**Element**</span></span>|<span data-ttu-id="9e6d0-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-120">**Type**</span></span>|<span data-ttu-id="9e6d0-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9e6d0-122">Text</span><span class="sxs-lookup"><span data-stu-id="9e6d0-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9e6d0-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="9e6d0-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9e6d0-124">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="9e6d0-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9e6d0-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9e6d0-125">Child elements</span></span>

<span data-ttu-id="9e6d0-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9e6d0-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e6d0-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="9e6d0-127">Attributes</span></span>

|<span data-ttu-id="9e6d0-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-128">**Attribute**</span></span>|<span data-ttu-id="9e6d0-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-129">**Type**</span></span>|<span data-ttu-id="9e6d0-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-130">**Required**</span></span>|<span data-ttu-id="9e6d0-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-131">**Description**</span></span>|<span data-ttu-id="9e6d0-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9e6d0-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9e6d0-133">IX</span><span class="sxs-lookup"><span data-stu-id="9e6d0-133">IX</span></span>  <br/> |<span data-ttu-id="9e6d0-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9e6d0-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9e6d0-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9e6d0-135">required</span></span>  <br/> |<span data-ttu-id="9e6d0-136">O índices baseado em zero do elemento no seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="9e6d0-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="9e6d0-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9e6d0-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

