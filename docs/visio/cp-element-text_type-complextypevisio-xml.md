---
title: Elemento cp (Text_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marca o início de uma execução de propriedades de caracteres que é formatada de acordo com o elemento Char correspondente. A execução é definida para o final do texto ou até a próxima marcação.
ms.openlocfilehash: 70f7d3f8333ff0f2c109862455fbd8cc3b340bf4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540557"
---
# <a name="cp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="738f2-104">Elemento cp (Text_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="738f2-104">cp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="738f2-105">Marca o início de uma execução de propriedades de caracteres que é formatada de acordo com o elemento Char correspondente.</span><span class="sxs-lookup"><span data-stu-id="738f2-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="738f2-106">A execução é definida para o final do texto ou até a próxima marcação.</span><span class="sxs-lookup"><span data-stu-id="738f2-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="738f2-107">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="738f2-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="738f2-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="738f2-108">**Element type**</span></span> <br/> |[<span data-ttu-id="738f2-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="738f2-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="738f2-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="738f2-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="738f2-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="738f2-111">**Schema file**</span></span> <br/> |<span data-ttu-id="738f2-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="738f2-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="738f2-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="738f2-113">**Document parts**</span></span> <br/> |<span data-ttu-id="738f2-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="738f2-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="738f2-115">Definição</span><span class="sxs-lookup"><span data-stu-id="738f2-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="738f2-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="738f2-116">Elements and attributes</span></span>

<span data-ttu-id="738f2-117">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="738f2-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="738f2-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="738f2-118">Parent elements</span></span>

|<span data-ttu-id="738f2-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="738f2-119">**Element**</span></span>|<span data-ttu-id="738f2-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="738f2-120">**Type**</span></span>|<span data-ttu-id="738f2-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="738f2-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="738f2-122">Text</span><span class="sxs-lookup"><span data-stu-id="738f2-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="738f2-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="738f2-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="738f2-124">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="738f2-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="738f2-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="738f2-125">Child elements</span></span>

<span data-ttu-id="738f2-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="738f2-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="738f2-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="738f2-127">Attributes</span></span>

|<span data-ttu-id="738f2-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="738f2-128">**Attribute**</span></span>|<span data-ttu-id="738f2-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="738f2-129">**Type**</span></span>|<span data-ttu-id="738f2-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="738f2-130">**Required**</span></span>|<span data-ttu-id="738f2-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="738f2-131">**Description**</span></span>|<span data-ttu-id="738f2-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="738f2-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="738f2-133">IX</span><span class="sxs-lookup"><span data-stu-id="738f2-133">IX</span></span>  <br/> |<span data-ttu-id="738f2-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="738f2-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="738f2-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="738f2-135">required</span></span>  <br/> |<span data-ttu-id="738f2-136">O índice do elemento Char que essa execução de propriedade representa.</span><span class="sxs-lookup"><span data-stu-id="738f2-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="738f2-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="738f2-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

