---
title: elemento PA (Text_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Especifica o início de propriedades guias executar. A execução é definida para o final do texto ou até que a próxima marca.
ms.openlocfilehash: 9b98374af4ffbf2eaeaea61dcb1dbb49214f01b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773165"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="5b028-104">elemento PA (Text_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="5b028-104">tp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5b028-105">Especifica o início de propriedades guias executar.</span><span class="sxs-lookup"><span data-stu-id="5b028-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="5b028-106">A execução é definida para o final do texto ou até que a próxima marca.</span><span class="sxs-lookup"><span data-stu-id="5b028-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b028-107">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="5b028-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b028-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5b028-108">**Element type**</span></span> <br/> |[<span data-ttu-id="5b028-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="5b028-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5b028-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b028-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5b028-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5b028-111">**Schema file**</span></span> <br/> |<span data-ttu-id="5b028-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5b028-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5b028-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="5b028-113">**Document parts**</span></span> <br/> |<span data-ttu-id="5b028-114">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="5b028-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b028-115">Definição</span><span class="sxs-lookup"><span data-stu-id="5b028-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b028-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5b028-116">Elements and attributes</span></span>

<span data-ttu-id="5b028-117">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5b028-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5b028-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5b028-118">Parent elements</span></span>

|<span data-ttu-id="5b028-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5b028-119">**Element**</span></span>|<span data-ttu-id="5b028-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5b028-120">**Type**</span></span>|<span data-ttu-id="5b028-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5b028-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b028-122">Text</span><span class="sxs-lookup"><span data-stu-id="5b028-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b028-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="5b028-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b028-124">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="5b028-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5b028-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5b028-125">Child elements</span></span>

<span data-ttu-id="5b028-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5b028-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b028-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b028-127">Attributes</span></span>

|<span data-ttu-id="5b028-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5b028-128">**Attribute**</span></span>|<span data-ttu-id="5b028-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5b028-129">**Type**</span></span>|<span data-ttu-id="5b028-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="5b028-130">**Required**</span></span>|<span data-ttu-id="5b028-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5b028-131">**Description**</span></span>|<span data-ttu-id="5b028-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="5b028-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5b028-133">IX</span><span class="sxs-lookup"><span data-stu-id="5b028-133">IX</span></span>  <br/> |<span data-ttu-id="5b028-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5b028-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5b028-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5b028-135">required</span></span>  <br/> |<span data-ttu-id="5b028-136">O índice baseado em zero do elemento dentro de seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="5b028-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="5b028-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5b028-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

