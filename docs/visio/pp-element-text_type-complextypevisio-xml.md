---
title: elemento PP (Text_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Especifica o início de uma execução de propriedades de parágrafo. A execução é definida para o final do texto ou até a próxima marcação.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356074"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="a19f8-104">elemento PP (Text_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a19f8-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a19f8-105">Especifica o início de uma execução de propriedades de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="a19f8-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="a19f8-106">A execução é definida para o final do texto ou até a próxima marcação.</span><span class="sxs-lookup"><span data-stu-id="a19f8-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a19f8-107">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="a19f8-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a19f8-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a19f8-108">**Element type**</span></span> <br/> |[<span data-ttu-id="a19f8-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="a19f8-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a19f8-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a19f8-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a19f8-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a19f8-111">**Schema file**</span></span> <br/> |<span data-ttu-id="a19f8-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a19f8-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a19f8-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="a19f8-113">**Document parts**</span></span> <br/> |<span data-ttu-id="a19f8-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="a19f8-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a19f8-115">Definição</span><span class="sxs-lookup"><span data-stu-id="a19f8-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a19f8-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a19f8-116">Elements and attributes</span></span>

<span data-ttu-id="a19f8-117">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a19f8-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a19f8-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a19f8-118">Parent elements</span></span>

|<span data-ttu-id="a19f8-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a19f8-119">**Element**</span></span>|<span data-ttu-id="a19f8-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a19f8-120">**Type**</span></span>|<span data-ttu-id="a19f8-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a19f8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a19f8-122">Text</span><span class="sxs-lookup"><span data-stu-id="a19f8-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a19f8-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="a19f8-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a19f8-124">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="a19f8-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a19f8-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a19f8-125">Child elements</span></span>

<span data-ttu-id="a19f8-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a19f8-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a19f8-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="a19f8-127">Attributes</span></span>

|<span data-ttu-id="a19f8-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a19f8-128">**Attribute**</span></span>|<span data-ttu-id="a19f8-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a19f8-129">**Type**</span></span>|<span data-ttu-id="a19f8-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a19f8-130">**Required**</span></span>|<span data-ttu-id="a19f8-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a19f8-131">**Description**</span></span>|<span data-ttu-id="a19f8-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a19f8-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a19f8-133">IX</span><span class="sxs-lookup"><span data-stu-id="a19f8-133">IX</span></span>  <br/> |<span data-ttu-id="a19f8-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a19f8-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a19f8-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a19f8-135">required</span></span>  <br/> |<span data-ttu-id="a19f8-136">O índice do elemento **para** que especifica a formatação aplicada a esta execução.</span><span class="sxs-lookup"><span data-stu-id="a19f8-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="a19f8-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a19f8-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

