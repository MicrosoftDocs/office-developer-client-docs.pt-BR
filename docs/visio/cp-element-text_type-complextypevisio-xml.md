---
title: Elemento cp (Text_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marca o início de uma execução de propriedades de caracteres que é formatada de acordo com o elemento Char correspondente. A execução é definida para o final do texto ou até a próxima marcação.
ms.openlocfilehash: eb7fd30c2314e159dc3649e87cd63bd4090ba283
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388193"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="8db39-104">Elemento cp (Text_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8db39-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8db39-105">Marca o início de uma execução de propriedades de caracteres que é formatada de acordo com o elemento Char correspondente.</span><span class="sxs-lookup"><span data-stu-id="8db39-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="8db39-106">A execução é definida para o final do texto ou até a próxima marcação.</span><span class="sxs-lookup"><span data-stu-id="8db39-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8db39-107">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="8db39-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8db39-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8db39-108">**Element type**</span></span> <br/> |[<span data-ttu-id="8db39-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="8db39-109">cp_Type complexType</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8db39-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8db39-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8db39-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8db39-111">**Schema file**</span></span> <br/> |<span data-ttu-id="8db39-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8db39-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8db39-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="8db39-113">**Document parts**</span></span> <br/> |<span data-ttu-id="8db39-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="8db39-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8db39-115">Definição</span><span class="sxs-lookup"><span data-stu-id="8db39-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8db39-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8db39-116">Elements and attributes</span></span>

<span data-ttu-id="8db39-117">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8db39-117">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8db39-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8db39-118">Parent elements</span></span>

|<span data-ttu-id="8db39-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8db39-119">**Element**</span></span>|<span data-ttu-id="8db39-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8db39-120">**Type**</span></span>|<span data-ttu-id="8db39-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8db39-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8db39-122">Text</span><span class="sxs-lookup"><span data-stu-id="8db39-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8db39-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="8db39-123">textType</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8db39-124">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="8db39-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8db39-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8db39-125">Child elements</span></span>

<span data-ttu-id="8db39-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8db39-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8db39-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="8db39-127">Attributes</span></span>

|<span data-ttu-id="8db39-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8db39-128">**Attribute**</span></span>|<span data-ttu-id="8db39-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8db39-129">**Type**</span></span>|<span data-ttu-id="8db39-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8db39-130">**Required**</span></span>|<span data-ttu-id="8db39-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8db39-131">**Description**</span></span>|<span data-ttu-id="8db39-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8db39-132">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8db39-133">IX</span><span class="sxs-lookup"><span data-stu-id="8db39-133">IX</span></span>  <br/> |<span data-ttu-id="8db39-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8db39-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8db39-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8db39-135">required</span></span>  <br/> |<span data-ttu-id="8db39-136">O índice do elemento Char que essa execução de propriedade representa.</span><span class="sxs-lookup"><span data-stu-id="8db39-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="8db39-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8db39-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

