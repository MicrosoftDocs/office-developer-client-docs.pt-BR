---
title: Elemento PageContents ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Especifica as informações sobre as formas em uma página mestra ou desenho de um desenho.
ms.openlocfilehash: 0ca705081ad42d799a0155b26eb42ff0b64cd7d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772443"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="faf02-103">Elemento PageContents ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="faf02-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="faf02-104">Especifica as informações sobre as formas em uma página mestra ou desenho de um desenho.</span><span class="sxs-lookup"><span data-stu-id="faf02-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="faf02-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="faf02-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="faf02-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="faf02-106">**Element type**</span></span> <br/> |[<span data-ttu-id="faf02-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="faf02-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="faf02-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="faf02-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="faf02-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="faf02-109">**Schema file**</span></span> <br/> |<span data-ttu-id="faf02-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="faf02-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="faf02-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="faf02-111">**Document parts**</span></span> <br/> |<span data-ttu-id="faf02-112">página # XML</span><span class="sxs-lookup"><span data-stu-id="faf02-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="faf02-113">Definição</span><span class="sxs-lookup"><span data-stu-id="faf02-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="faf02-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="faf02-114">Elements and attributes</span></span>

<span data-ttu-id="faf02-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="faf02-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="faf02-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="faf02-116">Parent elements</span></span>

<span data-ttu-id="faf02-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="faf02-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="faf02-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="faf02-118">Child elements</span></span>

|<span data-ttu-id="faf02-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="faf02-119">**Element**</span></span>|<span data-ttu-id="faf02-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="faf02-120">**Type**</span></span>|<span data-ttu-id="faf02-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="faf02-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="faf02-122">Connects</span><span class="sxs-lookup"><span data-stu-id="faf02-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="faf02-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="faf02-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="faf02-124">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="faf02-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="faf02-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="faf02-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="faf02-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="faf02-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="faf02-127">Especifica um conjunto de formas.</span><span class="sxs-lookup"><span data-stu-id="faf02-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="faf02-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="faf02-128">Attributes</span></span>

<span data-ttu-id="faf02-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="faf02-129">None.</span></span>
  

