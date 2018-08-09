---
title: elemento CP (Text_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marca o início das propriedades de um caractere ou seja executado formatado de acordo com o elemento Char correspondente. A execução é definida para o final do texto ou até que a próxima marca.
ms.openlocfilehash: 16e5bb94afeb860220c6cb49a9b98e36e45d76cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771630"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="d04ff-104">elemento CP (Text_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d04ff-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d04ff-105">Marca o início das propriedades de um caractere ou seja executado formatado de acordo com o elemento Char correspondente.</span><span class="sxs-lookup"><span data-stu-id="d04ff-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="d04ff-106">A execução é definida para o final do texto ou até que a próxima marca.</span><span class="sxs-lookup"><span data-stu-id="d04ff-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d04ff-107">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="d04ff-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d04ff-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="d04ff-108">**Element type**</span></span> <br/> |[<span data-ttu-id="d04ff-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="d04ff-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d04ff-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d04ff-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d04ff-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d04ff-111">**Schema file**</span></span> <br/> |<span data-ttu-id="d04ff-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d04ff-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d04ff-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="d04ff-113">**Document parts**</span></span> <br/> |<span data-ttu-id="d04ff-114">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="d04ff-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d04ff-115">Definição</span><span class="sxs-lookup"><span data-stu-id="d04ff-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d04ff-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d04ff-116">Elements and attributes</span></span>

<span data-ttu-id="d04ff-117">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d04ff-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d04ff-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d04ff-118">Parent elements</span></span>

|<span data-ttu-id="d04ff-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d04ff-119">**Element**</span></span>|<span data-ttu-id="d04ff-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d04ff-120">**Type**</span></span>|<span data-ttu-id="d04ff-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d04ff-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d04ff-122">Text</span><span class="sxs-lookup"><span data-stu-id="d04ff-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d04ff-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="d04ff-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d04ff-124">Contém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="d04ff-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d04ff-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d04ff-125">Child elements</span></span>

<span data-ttu-id="d04ff-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d04ff-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d04ff-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="d04ff-127">Attributes</span></span>

|<span data-ttu-id="d04ff-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d04ff-128">**Attribute**</span></span>|<span data-ttu-id="d04ff-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d04ff-129">**Type**</span></span>|<span data-ttu-id="d04ff-130">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d04ff-130">**Required**</span></span>|<span data-ttu-id="d04ff-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d04ff-131">**Description**</span></span>|<span data-ttu-id="d04ff-132">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d04ff-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d04ff-133">IX</span><span class="sxs-lookup"><span data-stu-id="d04ff-133">IX</span></span>  <br/> |<span data-ttu-id="d04ff-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d04ff-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d04ff-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="d04ff-135">required</span></span>  <br/> |<span data-ttu-id="d04ff-136">O índice do elemento de Char que representa essa propriedade executar.</span><span class="sxs-lookup"><span data-stu-id="d04ff-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="d04ff-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d04ff-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

