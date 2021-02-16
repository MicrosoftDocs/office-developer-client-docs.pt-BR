---
title: Elemento pp (Text_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Especifica o início de uma série de propriedades de parágrafo. A execução é definida para o final do texto ou até a próxima marcação.
ms.openlocfilehash: 695958c77f730abed03f50d6ad9c71f4de76dd63
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537735"
---
# <a name="pp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="6a9fd-104">Elemento pp (Text_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="6a9fd-104">pp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6a9fd-105">Especifica o início de uma série de propriedades de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="6a9fd-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="6a9fd-106">A execução é definida para o final do texto ou até a próxima marcação.</span><span class="sxs-lookup"><span data-stu-id="6a9fd-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a9fd-107">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="6a9fd-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a9fd-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-108">**Element type**</span></span> <br/> |[<span data-ttu-id="6a9fd-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="6a9fd-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6a9fd-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6a9fd-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-111">**Schema file**</span></span> <br/> |<span data-ttu-id="6a9fd-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6a9fd-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6a9fd-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-113">**Document parts**</span></span> <br/> |<span data-ttu-id="6a9fd-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="6a9fd-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6a9fd-115">Definição</span><span class="sxs-lookup"><span data-stu-id="6a9fd-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6a9fd-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6a9fd-116">Elements and attributes</span></span>

<span data-ttu-id="6a9fd-117">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6a9fd-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6a9fd-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6a9fd-118">Parent elements</span></span>

|<span data-ttu-id="6a9fd-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-119">**Element**</span></span>|<span data-ttu-id="6a9fd-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-120">**Type**</span></span>|<span data-ttu-id="6a9fd-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6a9fd-122">Text</span><span class="sxs-lookup"><span data-stu-id="6a9fd-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6a9fd-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="6a9fd-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6a9fd-124">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="6a9fd-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6a9fd-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6a9fd-125">Child elements</span></span>

<span data-ttu-id="6a9fd-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6a9fd-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a9fd-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a9fd-127">Attributes</span></span>

|<span data-ttu-id="6a9fd-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-128">**Attribute**</span></span>|<span data-ttu-id="6a9fd-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-129">**Type**</span></span>|<span data-ttu-id="6a9fd-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-130">**Required**</span></span>|<span data-ttu-id="6a9fd-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-131">**Description**</span></span>|<span data-ttu-id="6a9fd-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="6a9fd-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6a9fd-133">IX</span><span class="sxs-lookup"><span data-stu-id="6a9fd-133">IX</span></span>  <br/> |<span data-ttu-id="6a9fd-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6a9fd-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6a9fd-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="6a9fd-135">required</span></span>  <br/> |<span data-ttu-id="6a9fd-136">O índice do **elemento Para** que especifica a formatação aplicada a essa executar.</span><span class="sxs-lookup"><span data-stu-id="6a9fd-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="6a9fd-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6a9fd-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

