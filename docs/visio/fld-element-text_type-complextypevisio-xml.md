---
title: elemento FLD (Text_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Indica um ponto de inserção do campo de texto para o elemento do campo correspondente.
ms.openlocfilehash: a7303697a9471dab68f5b1cf851f60d51650a84e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383321"
---
# <a name="fld-element-texttype-complextype-visio-xml"></a><span data-ttu-id="dbd24-103">elemento FLD (Text_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="dbd24-103">fld element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="dbd24-104">Indica um ponto de inserção do campo de texto para o elemento do **campo** correspondente.</span><span class="sxs-lookup"><span data-stu-id="dbd24-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="dbd24-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="dbd24-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dbd24-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="dbd24-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dbd24-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="dbd24-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dbd24-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dbd24-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dbd24-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dbd24-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dbd24-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="dbd24-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dbd24-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="dbd24-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dbd24-112">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="dbd24-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dbd24-113">Definição</span><span class="sxs-lookup"><span data-stu-id="dbd24-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dbd24-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="dbd24-114">Elements and attributes</span></span>

<span data-ttu-id="dbd24-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="dbd24-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dbd24-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="dbd24-116">Parent elements</span></span>

|<span data-ttu-id="dbd24-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dbd24-117">**Element**</span></span>|<span data-ttu-id="dbd24-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dbd24-118">**Type**</span></span>|<span data-ttu-id="dbd24-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dbd24-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dbd24-120">Text</span><span class="sxs-lookup"><span data-stu-id="dbd24-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dbd24-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="dbd24-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dbd24-122">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="dbd24-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dbd24-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="dbd24-123">Child elements</span></span>

<span data-ttu-id="dbd24-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="dbd24-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dbd24-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="dbd24-125">Attributes</span></span>

|<span data-ttu-id="dbd24-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="dbd24-126">**Attribute**</span></span>|<span data-ttu-id="dbd24-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dbd24-127">**Type**</span></span>|<span data-ttu-id="dbd24-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="dbd24-128">**Required**</span></span>|<span data-ttu-id="dbd24-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dbd24-129">**Description**</span></span>|<span data-ttu-id="dbd24-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="dbd24-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dbd24-131">IX</span><span class="sxs-lookup"><span data-stu-id="dbd24-131">IX</span></span>  <br/> |<span data-ttu-id="dbd24-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dbd24-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dbd24-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="dbd24-133">required</span></span>  <br/> |<span data-ttu-id="dbd24-134">O índice baseado em zero do elemento dentro de seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="dbd24-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="dbd24-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dbd24-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

