---
title: Elemento MasterContents ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Especifica informações sobre as formas em um mestre em um desenho.
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385463"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="36d40-103">Elemento MasterContents ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="36d40-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="36d40-104">Especifica informações sobre as formas em um mestre em um desenho.</span><span class="sxs-lookup"><span data-stu-id="36d40-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="36d40-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="36d40-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36d40-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="36d40-106">**Element type**</span></span> <br/> |[<span data-ttu-id="36d40-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="36d40-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="36d40-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="36d40-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="36d40-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="36d40-109">**Schema file**</span></span> <br/> |<span data-ttu-id="36d40-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="36d40-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="36d40-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="36d40-111">**Document parts**</span></span> <br/> |<span data-ttu-id="36d40-112">. XML de # mestre</span><span class="sxs-lookup"><span data-stu-id="36d40-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36d40-113">Definição</span><span class="sxs-lookup"><span data-stu-id="36d40-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="36d40-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="36d40-114">Elements and attributes</span></span>

<span data-ttu-id="36d40-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="36d40-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="36d40-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="36d40-116">Parent elements</span></span>

<span data-ttu-id="36d40-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="36d40-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36d40-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="36d40-118">Child elements</span></span>

|<span data-ttu-id="36d40-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="36d40-119">**Element**</span></span>|<span data-ttu-id="36d40-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="36d40-120">**Type**</span></span>|<span data-ttu-id="36d40-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36d40-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="36d40-122">Connects</span><span class="sxs-lookup"><span data-stu-id="36d40-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36d40-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="36d40-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="36d40-124">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="36d40-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="36d40-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="36d40-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36d40-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="36d40-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="36d40-127">Contém uma coleção de elementos de **forma** .</span><span class="sxs-lookup"><span data-stu-id="36d40-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="36d40-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="36d40-128">Attributes</span></span>

<span data-ttu-id="36d40-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="36d40-129">None.</span></span>
  

