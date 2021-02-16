---
title: Elemento PageContents (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Especifica as informações sobre as formas em uma página de desenho ou mestre de um desenho.
ms.openlocfilehash: 23ff6c74007adc5764007e34c1b2ac92c522b121
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537994"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="c1e88-103">Elemento PageContents (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="c1e88-103">PageContents element (Visio XML)</span></span>

<span data-ttu-id="c1e88-104">Especifica as informações sobre as formas em uma página de desenho ou mestre de um desenho.</span><span class="sxs-lookup"><span data-stu-id="c1e88-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1e88-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="c1e88-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1e88-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c1e88-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c1e88-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c1e88-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c1e88-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c1e88-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c1e88-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c1e88-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c1e88-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c1e88-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c1e88-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="c1e88-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c1e88-112">page#.xml</span><span class="sxs-lookup"><span data-stu-id="c1e88-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1e88-113">Definição</span><span class="sxs-lookup"><span data-stu-id="c1e88-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c1e88-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c1e88-114">Elements and attributes</span></span>

<span data-ttu-id="c1e88-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c1e88-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c1e88-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c1e88-116">Parent elements</span></span>

<span data-ttu-id="c1e88-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1e88-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1e88-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c1e88-118">Child elements</span></span>

|<span data-ttu-id="c1e88-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1e88-119">**Element**</span></span>|<span data-ttu-id="c1e88-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c1e88-120">**Type**</span></span>|<span data-ttu-id="c1e88-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c1e88-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1e88-122">Connects</span><span class="sxs-lookup"><span data-stu-id="c1e88-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1e88-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="c1e88-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1e88-124">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="c1e88-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="c1e88-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="c1e88-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1e88-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="c1e88-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1e88-127">Especifica uma coleção de formas.</span><span class="sxs-lookup"><span data-stu-id="c1e88-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c1e88-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1e88-128">Attributes</span></span>

<span data-ttu-id="c1e88-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1e88-129">None.</span></span>
  

