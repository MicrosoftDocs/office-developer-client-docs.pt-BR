---
title: Elemento ColorEntry (Colors_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Contém uma entrada da tabela de cores.
ms.openlocfilehash: 934680b36428dd272d383ce421e86ae6d5c707cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771529"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a><span data-ttu-id="044f7-103">Elemento ColorEntry (Colors_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="044f7-103">ColorEntry element (Colors_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="044f7-104">Contém uma entrada da tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="044f7-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="044f7-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="044f7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="044f7-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="044f7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="044f7-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="044f7-107">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="044f7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="044f7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="044f7-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="044f7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="044f7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="044f7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="044f7-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="044f7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="044f7-112">Document</span><span class="sxs-lookup"><span data-stu-id="044f7-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="044f7-113">Definição</span><span class="sxs-lookup"><span data-stu-id="044f7-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="044f7-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="044f7-114">Elements and attributes</span></span>

<span data-ttu-id="044f7-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="044f7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="044f7-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="044f7-116">Parent elements</span></span>

|<span data-ttu-id="044f7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="044f7-117">**Element**</span></span>|<span data-ttu-id="044f7-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="044f7-118">**Type**</span></span>|<span data-ttu-id="044f7-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="044f7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="044f7-120">Cores</span><span class="sxs-lookup"><span data-stu-id="044f7-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="044f7-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="044f7-121">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="044f7-122">Contém a tabela de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="044f7-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="044f7-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="044f7-123">Child elements</span></span>

<span data-ttu-id="044f7-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="044f7-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="044f7-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="044f7-125">Attributes</span></span>

|<span data-ttu-id="044f7-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="044f7-126">**Attribute**</span></span>|<span data-ttu-id="044f7-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="044f7-127">**Type**</span></span>|<span data-ttu-id="044f7-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="044f7-128">**Required**</span></span>|<span data-ttu-id="044f7-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="044f7-129">**Description**</span></span>|<span data-ttu-id="044f7-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="044f7-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="044f7-131">IX</span><span class="sxs-lookup"><span data-stu-id="044f7-131">IX</span></span>  <br/> |<span data-ttu-id="044f7-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="044f7-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="044f7-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="044f7-133">required</span></span>  <br/> |<span data-ttu-id="044f7-134">O índice baseado em zero do elemento dentro de seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="044f7-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="044f7-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="044f7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="044f7-136">RGB</span><span class="sxs-lookup"><span data-stu-id="044f7-136">RGB</span></span>  <br/> |<span data-ttu-id="044f7-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="044f7-137">xsd:string</span></span>  <br/> |<span data-ttu-id="044f7-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="044f7-138">required</span></span>  <br/> |<span data-ttu-id="044f7-139">O valor hexadecimal da entrada da tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="044f7-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="044f7-140">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="044f7-140">Values of the xsd:string type.</span></span>  <br/> |
   

