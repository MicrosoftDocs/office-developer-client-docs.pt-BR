---
title: Elemento ColorEntry (Colors_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Contém uma entrada de tabela de cor.
ms.openlocfilehash: 14ef92069ce8d963ce4a0770324843321804c5cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358083"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a><span data-ttu-id="229e6-103">Elemento ColorEntry (Colors_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="229e6-103">ColorEntry element (Colors_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="229e6-104">Contém uma entrada de tabela de cor.</span><span class="sxs-lookup"><span data-stu-id="229e6-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="229e6-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="229e6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="229e6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="229e6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="229e6-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="229e6-107">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="229e6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="229e6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="229e6-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="229e6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="229e6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="229e6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="229e6-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="229e6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="229e6-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="229e6-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="229e6-113">Definição</span><span class="sxs-lookup"><span data-stu-id="229e6-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="229e6-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="229e6-114">Elements and attributes</span></span>

<span data-ttu-id="229e6-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="229e6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="229e6-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="229e6-116">Parent elements</span></span>

|<span data-ttu-id="229e6-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="229e6-117">**Element**</span></span>|<span data-ttu-id="229e6-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="229e6-118">**Type**</span></span>|<span data-ttu-id="229e6-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="229e6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="229e6-120">Colors</span><span class="sxs-lookup"><span data-stu-id="229e6-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="229e6-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="229e6-121">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="229e6-122">Contém a tabela de cor do documento.</span><span class="sxs-lookup"><span data-stu-id="229e6-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="229e6-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="229e6-123">Child elements</span></span>

<span data-ttu-id="229e6-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="229e6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="229e6-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="229e6-125">Attributes</span></span>

|<span data-ttu-id="229e6-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="229e6-126">**Attribute**</span></span>|<span data-ttu-id="229e6-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="229e6-127">**Type**</span></span>|<span data-ttu-id="229e6-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="229e6-128">**Required**</span></span>|<span data-ttu-id="229e6-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="229e6-129">**Description**</span></span>|<span data-ttu-id="229e6-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="229e6-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="229e6-131">IX</span><span class="sxs-lookup"><span data-stu-id="229e6-131">IX</span></span>  <br/> |<span data-ttu-id="229e6-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="229e6-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="229e6-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="229e6-133">required</span></span>  <br/> |<span data-ttu-id="229e6-134">O índices baseado em zero do elemento no seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="229e6-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="229e6-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="229e6-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="229e6-136">RGB</span><span class="sxs-lookup"><span data-stu-id="229e6-136">RGB</span></span>  <br/> |<span data-ttu-id="229e6-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="229e6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="229e6-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="229e6-138">required</span></span>  <br/> |<span data-ttu-id="229e6-139">O valor hexadecimal da entrada da tabela de cor.</span><span class="sxs-lookup"><span data-stu-id="229e6-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="229e6-140">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="229e6-140">Values of the xsd:string type.</span></span>  <br/> |
   

