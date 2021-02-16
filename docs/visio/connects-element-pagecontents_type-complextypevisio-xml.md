---
title: Elemento Connects (PageContents_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contém um elemento Connect para cada conexão entre duas formas em um desenho.
ms.openlocfilehash: d421068926a40a8f7c24a783388d06091700211f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538708"
---
# <a name="connects-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="8bb8a-103">Elemento Connects (PageContents_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="8bb8a-103">Connects element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8bb8a-104">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="8bb8a-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8bb8a-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="8bb8a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bb8a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8bb8a-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="8bb8a-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8bb8a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8bb8a-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8bb8a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8bb8a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8bb8a-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8bb8a-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="8bb8a-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8bb8a-113">Definição</span><span class="sxs-lookup"><span data-stu-id="8bb8a-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8bb8a-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8bb8a-114">Elements and attributes</span></span>

<span data-ttu-id="8bb8a-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8bb8a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8bb8a-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8bb8a-116">Parent elements</span></span>

|<span data-ttu-id="8bb8a-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-117">**Element**</span></span>|<span data-ttu-id="8bb8a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-118">**Type**</span></span>|<span data-ttu-id="8bb8a-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8bb8a-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="8bb8a-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="8bb8a-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="8bb8a-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8bb8a-122">Especifica as informações sobre as formas em uma página de desenho ou mestre de um desenho.</span><span class="sxs-lookup"><span data-stu-id="8bb8a-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="8bb8a-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="8bb8a-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="8bb8a-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="8bb8a-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8bb8a-125">Especifica as informações sobre as formas em uma página de desenho ou mestre de um desenho.</span><span class="sxs-lookup"><span data-stu-id="8bb8a-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8bb8a-126">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8bb8a-126">Child elements</span></span>

|<span data-ttu-id="8bb8a-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-127">**Element**</span></span>|<span data-ttu-id="8bb8a-128">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-128">**Type**</span></span>|<span data-ttu-id="8bb8a-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8bb8a-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8bb8a-130">Connect</span><span class="sxs-lookup"><span data-stu-id="8bb8a-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8bb8a-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="8bb8a-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8bb8a-132">Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.</span><span class="sxs-lookup"><span data-stu-id="8bb8a-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8bb8a-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="8bb8a-133">Attributes</span></span>

<span data-ttu-id="8bb8a-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8bb8a-134">None.</span></span>
  

