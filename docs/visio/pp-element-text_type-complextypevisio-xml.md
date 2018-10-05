---
title: elemento de PP (Text_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Especifica o início das propriedades de um parágrafo é executado. A execução é definida para o final do texto ou até que a próxima marca.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400094"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="a022b-104">elemento de PP (Text_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a022b-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a022b-105">Especifica o início das propriedades de um parágrafo é executado.</span><span class="sxs-lookup"><span data-stu-id="a022b-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="a022b-106">A execução é definida para o final do texto ou até que a próxima marca.</span><span class="sxs-lookup"><span data-stu-id="a022b-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a022b-107">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="a022b-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a022b-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a022b-108">**Element type**</span></span> <br/> |[<span data-ttu-id="a022b-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="a022b-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a022b-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a022b-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a022b-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a022b-111">**Schema file**</span></span> <br/> |<span data-ttu-id="a022b-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a022b-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a022b-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="a022b-113">**Document parts**</span></span> <br/> |<span data-ttu-id="a022b-114">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="a022b-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a022b-115">Definição</span><span class="sxs-lookup"><span data-stu-id="a022b-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a022b-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a022b-116">Elements and attributes</span></span>

<span data-ttu-id="a022b-117">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a022b-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a022b-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a022b-118">Parent elements</span></span>

|<span data-ttu-id="a022b-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a022b-119">**Element**</span></span>|<span data-ttu-id="a022b-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a022b-120">**Type**</span></span>|<span data-ttu-id="a022b-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a022b-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a022b-122">Text</span><span class="sxs-lookup"><span data-stu-id="a022b-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a022b-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="a022b-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a022b-124">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="a022b-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a022b-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a022b-125">Child elements</span></span>

<span data-ttu-id="a022b-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a022b-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a022b-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="a022b-127">Attributes</span></span>

|<span data-ttu-id="a022b-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a022b-128">**Attribute**</span></span>|<span data-ttu-id="a022b-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a022b-129">**Type**</span></span>|<span data-ttu-id="a022b-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a022b-130">**Required**</span></span>|<span data-ttu-id="a022b-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a022b-131">**Description**</span></span>|<span data-ttu-id="a022b-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a022b-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a022b-133">IX</span><span class="sxs-lookup"><span data-stu-id="a022b-133">IX</span></span>  <br/> |<span data-ttu-id="a022b-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a022b-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a022b-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a022b-135">required</span></span>  <br/> |<span data-ttu-id="a022b-136">O índice do elemento de **parágrafo** que especifica a formatação aplicada dessa execução.</span><span class="sxs-lookup"><span data-stu-id="a022b-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="a022b-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a022b-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

