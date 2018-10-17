---
title: CommentEntry_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384791"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="feec5-102">CommentEntry_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="feec5-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="feec5-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="feec5-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="feec5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="feec5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="feec5-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="feec5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="feec5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="feec5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="feec5-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="feec5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="feec5-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="feec5-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="feec5-109">Definição</span><span class="sxs-lookup"><span data-stu-id="feec5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="feec5-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="feec5-110">Elements and attributes</span></span>

<span data-ttu-id="feec5-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="feec5-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="feec5-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="feec5-112">Child elements</span></span>

<span data-ttu-id="feec5-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="feec5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="feec5-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="feec5-114">Attributes</span></span>

|<span data-ttu-id="feec5-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="feec5-115">**Attribute**</span></span>|<span data-ttu-id="feec5-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="feec5-116">**Type**</span></span>|<span data-ttu-id="feec5-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="feec5-117">**Required**</span></span>|<span data-ttu-id="feec5-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="feec5-118">**Description**</span></span>|<span data-ttu-id="feec5-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="feec5-119">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="feec5-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="feec5-120">AuthorID</span></span>  <br/> |<span data-ttu-id="feec5-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="feec5-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="feec5-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="feec5-122">required</span></span>  <br/> ||<span data-ttu-id="feec5-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="feec5-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="feec5-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="feec5-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="feec5-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="feec5-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="feec5-126">opcional</span><span class="sxs-lookup"><span data-stu-id="feec5-126">optional</span></span>  <br/> ||<span data-ttu-id="feec5-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="feec5-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="feec5-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="feec5-128">CommentID</span></span>  <br/> |<span data-ttu-id="feec5-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="feec5-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="feec5-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="feec5-130">required</span></span>  <br/> ||<span data-ttu-id="feec5-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="feec5-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="feec5-132">Data</span><span class="sxs-lookup"><span data-stu-id="feec5-132">Date</span></span>  <br/> |<span data-ttu-id="feec5-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="feec5-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="feec5-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="feec5-134">required</span></span>  <br/> ||<span data-ttu-id="feec5-135">Valores do tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="feec5-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="feec5-136">Concluído</span><span class="sxs-lookup"><span data-stu-id="feec5-136">Done</span></span>  <br/> |<span data-ttu-id="feec5-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="feec5-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="feec5-138">opcional</span><span class="sxs-lookup"><span data-stu-id="feec5-138">optional</span></span>  <br/> ||<span data-ttu-id="feec5-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="feec5-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="feec5-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="feec5-140">EditDate Property</span></span>  <br/> |<span data-ttu-id="feec5-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="feec5-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="feec5-142">opcional</span><span class="sxs-lookup"><span data-stu-id="feec5-142">optional</span></span>  <br/> ||<span data-ttu-id="feec5-143">Valores do tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="feec5-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="feec5-144">PageID</span><span class="sxs-lookup"><span data-stu-id="feec5-144">expression  . PageID</span></span>  <br/> |<span data-ttu-id="feec5-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="feec5-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="feec5-146">obrigatório</span><span class="sxs-lookup"><span data-stu-id="feec5-146">required</span></span>  <br/> ||<span data-ttu-id="feec5-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="feec5-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="feec5-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="feec5-148">ShapeId</span></span>  <br/> |<span data-ttu-id="feec5-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="feec5-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="feec5-150">opcional</span><span class="sxs-lookup"><span data-stu-id="feec5-150">optional</span></span>  <br/> ||<span data-ttu-id="feec5-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="feec5-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

