---
title: Elemento PageContents ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Especifica as informações sobre as formas em uma página mestra ou desenho de um desenho.
ms.openlocfilehash: aec860f4135e15f18436dba50986b0ad0e6ee9e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396565"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="f0e78-103">Elemento PageContents ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f0e78-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="f0e78-104">Especifica as informações sobre as formas em uma página mestra ou desenho de um desenho.</span><span class="sxs-lookup"><span data-stu-id="f0e78-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0e78-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="f0e78-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0e78-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f0e78-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f0e78-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="f0e78-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f0e78-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f0e78-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f0e78-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f0e78-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f0e78-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f0e78-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f0e78-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="f0e78-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f0e78-112">página # XML</span><span class="sxs-lookup"><span data-stu-id="f0e78-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f0e78-113">Definição</span><span class="sxs-lookup"><span data-stu-id="f0e78-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f0e78-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f0e78-114">Elements and attributes</span></span>

<span data-ttu-id="f0e78-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f0e78-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f0e78-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f0e78-116">Parent elements</span></span>

<span data-ttu-id="f0e78-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f0e78-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0e78-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f0e78-118">Child elements</span></span>

|<span data-ttu-id="f0e78-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f0e78-119">**Element**</span></span>|<span data-ttu-id="f0e78-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0e78-120">**Type**</span></span>|<span data-ttu-id="f0e78-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f0e78-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f0e78-122">Connects</span><span class="sxs-lookup"><span data-stu-id="f0e78-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f0e78-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="f0e78-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f0e78-124">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="f0e78-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="f0e78-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="f0e78-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f0e78-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="f0e78-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f0e78-127">Especifica um conjunto de formas.</span><span class="sxs-lookup"><span data-stu-id="f0e78-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f0e78-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0e78-128">Attributes</span></span>

<span data-ttu-id="f0e78-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f0e78-129">None.</span></span>
  

