---
title: Elemento MasterContents (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Especifica informações sobre as formas de um mestre em um desenho.
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341353"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="956e6-103">Elemento MasterContents (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="956e6-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="956e6-104">Especifica informações sobre as formas de um mestre em um desenho.</span><span class="sxs-lookup"><span data-stu-id="956e6-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="956e6-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="956e6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="956e6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="956e6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="956e6-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="956e6-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="956e6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="956e6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="956e6-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="956e6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="956e6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="956e6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="956e6-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="956e6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="956e6-112">Master #. xml</span><span class="sxs-lookup"><span data-stu-id="956e6-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="956e6-113">Definição</span><span class="sxs-lookup"><span data-stu-id="956e6-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="956e6-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="956e6-114">Elements and attributes</span></span>

<span data-ttu-id="956e6-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="956e6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="956e6-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="956e6-116">Parent elements</span></span>

<span data-ttu-id="956e6-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="956e6-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="956e6-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="956e6-118">Child elements</span></span>

|<span data-ttu-id="956e6-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="956e6-119">**Element**</span></span>|<span data-ttu-id="956e6-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="956e6-120">**Type**</span></span>|<span data-ttu-id="956e6-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="956e6-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="956e6-122">Connects</span><span class="sxs-lookup"><span data-stu-id="956e6-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="956e6-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="956e6-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="956e6-124">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="956e6-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="956e6-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="956e6-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="956e6-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="956e6-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="956e6-127">Contém uma coleção de elementos **Shape** .</span><span class="sxs-lookup"><span data-stu-id="956e6-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="956e6-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="956e6-128">Attributes</span></span>

<span data-ttu-id="956e6-129">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="956e6-129">None.</span></span>
  

