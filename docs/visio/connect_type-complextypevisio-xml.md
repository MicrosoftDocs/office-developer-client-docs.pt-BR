---
title: Connect_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9a321a3ff910afb183e1a697eaad9dfb51125524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771572"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="cab32-102">Connect_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="cab32-102">Connect_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cab32-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="cab32-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cab32-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cab32-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cab32-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cab32-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cab32-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cab32-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cab32-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="cab32-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cab32-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cab32-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cab32-109">Definição</span><span class="sxs-lookup"><span data-stu-id="cab32-109">Definition</span></span>

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cab32-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cab32-110">Elements and attributes</span></span>

<span data-ttu-id="cab32-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cab32-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cab32-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cab32-112">Child elements</span></span>

<span data-ttu-id="cab32-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="cab32-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cab32-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="cab32-114">Attributes</span></span>

|<span data-ttu-id="cab32-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cab32-115">**Attribute**</span></span>|<span data-ttu-id="cab32-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cab32-116">**Type**</span></span>|<span data-ttu-id="cab32-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="cab32-117">**Required**</span></span>|<span data-ttu-id="cab32-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cab32-118">**Description**</span></span>|<span data-ttu-id="cab32-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="cab32-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cab32-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="cab32-120">FromCell</span></span>  <br/> |<span data-ttu-id="cab32-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="cab32-121">xsd:string</span></span>  <br/> |<span data-ttu-id="cab32-122">opcional</span><span class="sxs-lookup"><span data-stu-id="cab32-122">optional</span></span>  <br/> ||<span data-ttu-id="cab32-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cab32-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cab32-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="cab32-124">FromPart</span></span>  <br/> |<span data-ttu-id="cab32-125">XSD:int</span><span class="sxs-lookup"><span data-stu-id="cab32-125">xsd:int</span></span>  <br/> |<span data-ttu-id="cab32-126">opcional</span><span class="sxs-lookup"><span data-stu-id="cab32-126">optional</span></span>  <br/> ||<span data-ttu-id="cab32-127">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="cab32-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="cab32-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="cab32-128">FromSheet</span></span>  <br/> |<span data-ttu-id="cab32-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cab32-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cab32-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cab32-130">required</span></span>  <br/> ||<span data-ttu-id="cab32-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cab32-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cab32-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="cab32-132">ToCell</span></span>  <br/> |<span data-ttu-id="cab32-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="cab32-133">xsd:string</span></span>  <br/> |<span data-ttu-id="cab32-134">opcional</span><span class="sxs-lookup"><span data-stu-id="cab32-134">optional</span></span>  <br/> ||<span data-ttu-id="cab32-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cab32-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cab32-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="cab32-136">ToPart</span></span>  <br/> |<span data-ttu-id="cab32-137">XSD:int</span><span class="sxs-lookup"><span data-stu-id="cab32-137">xsd:int</span></span>  <br/> |<span data-ttu-id="cab32-138">opcional</span><span class="sxs-lookup"><span data-stu-id="cab32-138">optional</span></span>  <br/> ||<span data-ttu-id="cab32-139">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="cab32-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="cab32-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="cab32-140">ToSheet</span></span>  <br/> |<span data-ttu-id="cab32-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cab32-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cab32-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cab32-142">required</span></span>  <br/> ||<span data-ttu-id="cab32-143">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cab32-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

