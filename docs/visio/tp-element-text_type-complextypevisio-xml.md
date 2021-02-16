---
title: Elemento tp (Text_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Especifica o início de uma operação de propriedades de guias. A execução é definida para o final do texto ou até a próxima marcação.
ms.openlocfilehash: dad7a3de715473a75c601c1e391c9d51fc1cab85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542972"
---
# <a name="tp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="e7aca-104">Elemento tp (Text_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="e7aca-104">tp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="e7aca-105">Especifica o início de uma operação de propriedades de guias.</span><span class="sxs-lookup"><span data-stu-id="e7aca-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="e7aca-106">A execução é definida para o final do texto ou até a próxima marcação.</span><span class="sxs-lookup"><span data-stu-id="e7aca-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7aca-107">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="e7aca-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7aca-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e7aca-108">**Element type**</span></span> <br/> |[<span data-ttu-id="e7aca-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="e7aca-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e7aca-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e7aca-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e7aca-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e7aca-111">**Schema file**</span></span> <br/> |<span data-ttu-id="e7aca-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e7aca-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e7aca-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="e7aca-113">**Document parts**</span></span> <br/> |<span data-ttu-id="e7aca-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="e7aca-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e7aca-115">Definição</span><span class="sxs-lookup"><span data-stu-id="e7aca-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e7aca-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="e7aca-116">Elements and attributes</span></span>

<span data-ttu-id="e7aca-117">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="e7aca-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e7aca-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e7aca-118">Parent elements</span></span>

|<span data-ttu-id="e7aca-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e7aca-119">**Element**</span></span>|<span data-ttu-id="e7aca-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e7aca-120">**Type**</span></span>|<span data-ttu-id="e7aca-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e7aca-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e7aca-122">Text</span><span class="sxs-lookup"><span data-stu-id="e7aca-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e7aca-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="e7aca-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e7aca-124">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="e7aca-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e7aca-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e7aca-125">Child elements</span></span>

<span data-ttu-id="e7aca-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e7aca-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7aca-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="e7aca-127">Attributes</span></span>

|<span data-ttu-id="e7aca-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e7aca-128">**Attribute**</span></span>|<span data-ttu-id="e7aca-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e7aca-129">**Type**</span></span>|<span data-ttu-id="e7aca-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="e7aca-130">**Required**</span></span>|<span data-ttu-id="e7aca-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e7aca-131">**Description**</span></span>|<span data-ttu-id="e7aca-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="e7aca-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e7aca-133">IX</span><span class="sxs-lookup"><span data-stu-id="e7aca-133">IX</span></span>  <br/> |<span data-ttu-id="e7aca-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e7aca-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e7aca-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="e7aca-135">required</span></span>  <br/> |<span data-ttu-id="e7aca-136">O índices baseado em zero do elemento no seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="e7aca-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="e7aca-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e7aca-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

