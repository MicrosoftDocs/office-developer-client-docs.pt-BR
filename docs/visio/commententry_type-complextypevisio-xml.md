---
title: CommentEntry_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 5ee3c9f2aa8b0af91289ce1cd6bb2355adec3426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771528"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="5bf16-102">CommentEntry_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="5bf16-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5bf16-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="5bf16-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5bf16-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5bf16-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5bf16-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5bf16-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5bf16-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5bf16-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5bf16-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="5bf16-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5bf16-108">XSD: String</span><span class="sxs-lookup"><span data-stu-id="5bf16-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5bf16-109">Definição</span><span class="sxs-lookup"><span data-stu-id="5bf16-109">Definition</span></span>

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5bf16-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5bf16-110">Elements and attributes</span></span>

<span data-ttu-id="5bf16-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5bf16-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5bf16-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5bf16-112">Child elements</span></span>

<span data-ttu-id="5bf16-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5bf16-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5bf16-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="5bf16-114">Attributes</span></span>

|<span data-ttu-id="5bf16-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5bf16-115">**Attribute**</span></span>|<span data-ttu-id="5bf16-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5bf16-116">**Type**</span></span>|<span data-ttu-id="5bf16-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="5bf16-117">**Required**</span></span>|<span data-ttu-id="5bf16-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5bf16-118">**Description**</span></span>|<span data-ttu-id="5bf16-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="5bf16-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5bf16-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="5bf16-120">AuthorID</span></span>  <br/> |<span data-ttu-id="5bf16-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5bf16-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5bf16-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5bf16-122">required</span></span>  <br/> ||<span data-ttu-id="5bf16-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5bf16-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5bf16-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="5bf16-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="5bf16-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5bf16-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5bf16-126">opcional</span><span class="sxs-lookup"><span data-stu-id="5bf16-126">optional</span></span>  <br/> ||<span data-ttu-id="5bf16-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5bf16-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5bf16-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="5bf16-128">CommentID</span></span>  <br/> |<span data-ttu-id="5bf16-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5bf16-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5bf16-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5bf16-130">required</span></span>  <br/> ||<span data-ttu-id="5bf16-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5bf16-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5bf16-132">Date</span><span class="sxs-lookup"><span data-stu-id="5bf16-132">Date</span></span>  <br/> |<span data-ttu-id="5bf16-133">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="5bf16-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="5bf16-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5bf16-134">required</span></span>  <br/> ||<span data-ttu-id="5bf16-135">Valores do tipo xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="5bf16-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="5bf16-136">Concluído</span><span class="sxs-lookup"><span data-stu-id="5bf16-136">Done</span></span>  <br/> |<span data-ttu-id="5bf16-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf16-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5bf16-138">opcional</span><span class="sxs-lookup"><span data-stu-id="5bf16-138">optional</span></span>  <br/> ||<span data-ttu-id="5bf16-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5bf16-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5bf16-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="5bf16-140">EditDate</span></span>  <br/> |<span data-ttu-id="5bf16-141">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="5bf16-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="5bf16-142">opcional</span><span class="sxs-lookup"><span data-stu-id="5bf16-142">optional</span></span>  <br/> ||<span data-ttu-id="5bf16-143">Valores do tipo xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="5bf16-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="5bf16-144">PageID</span><span class="sxs-lookup"><span data-stu-id="5bf16-144">PageID</span></span>  <br/> |<span data-ttu-id="5bf16-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5bf16-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5bf16-146">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5bf16-146">required</span></span>  <br/> ||<span data-ttu-id="5bf16-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5bf16-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5bf16-148">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="5bf16-148">ShapeID</span></span>  <br/> |<span data-ttu-id="5bf16-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5bf16-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5bf16-150">opcional</span><span class="sxs-lookup"><span data-stu-id="5bf16-150">optional</span></span>  <br/> ||<span data-ttu-id="5bf16-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5bf16-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

