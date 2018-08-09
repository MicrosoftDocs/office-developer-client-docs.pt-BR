---
title: Conecta o elemento (PageContents_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contém um elemento Connect para cada conexão entre duas formas em um desenho.
ms.openlocfilehash: 93930a8f21f9d250bf24d821b0eeb4036f6fe187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771591"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="abd57-103">Conecta o elemento (PageContents_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="abd57-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="abd57-104">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="abd57-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="abd57-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="abd57-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abd57-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="abd57-106">**Element type**</span></span> <br/> |[<span data-ttu-id="abd57-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="abd57-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="abd57-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="abd57-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="abd57-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="abd57-109">**Schema file**</span></span> <br/> |<span data-ttu-id="abd57-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="abd57-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="abd57-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="abd57-111">**Document parts**</span></span> <br/> |<span data-ttu-id="abd57-112">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="abd57-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="abd57-113">Definição</span><span class="sxs-lookup"><span data-stu-id="abd57-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="abd57-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="abd57-114">Elements and attributes</span></span>

<span data-ttu-id="abd57-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="abd57-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="abd57-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="abd57-116">Parent elements</span></span>

|<span data-ttu-id="abd57-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="abd57-117">**Element**</span></span>|<span data-ttu-id="abd57-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="abd57-118">**Type**</span></span>|<span data-ttu-id="abd57-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="abd57-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="abd57-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="abd57-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="abd57-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="abd57-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="abd57-122">Especifica as informações sobre as formas em uma página mestra ou desenho de um desenho.</span><span class="sxs-lookup"><span data-stu-id="abd57-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="abd57-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="abd57-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="abd57-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="abd57-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="abd57-125">Especifica as informações sobre as formas em uma página mestra ou desenho de um desenho.</span><span class="sxs-lookup"><span data-stu-id="abd57-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="abd57-126">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="abd57-126">Child elements</span></span>

|<span data-ttu-id="abd57-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="abd57-127">**Element**</span></span>|<span data-ttu-id="abd57-128">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="abd57-128">**Type**</span></span>|<span data-ttu-id="abd57-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="abd57-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="abd57-130">Connect</span><span class="sxs-lookup"><span data-stu-id="abd57-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="abd57-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="abd57-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="abd57-132">
			Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.
</span><span class="sxs-lookup"><span data-stu-id="abd57-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="abd57-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="abd57-133">Attributes</span></span>

<span data-ttu-id="abd57-134">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="abd57-134">None.</span></span>
  

