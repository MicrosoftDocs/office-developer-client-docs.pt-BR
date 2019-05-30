---
title: CommentEntry_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 840f660d72acbda052d4729846d8a26686d82b2a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540123"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="7d69b-102">CommentEntry_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="7d69b-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7d69b-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="7d69b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d69b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7d69b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7d69b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7d69b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7d69b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7d69b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7d69b-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="7d69b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7d69b-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7d69b-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7d69b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="7d69b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7d69b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7d69b-110">Elements and attributes</span></span>

<span data-ttu-id="7d69b-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7d69b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7d69b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7d69b-112">Child elements</span></span>

<span data-ttu-id="7d69b-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7d69b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d69b-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d69b-114">Attributes</span></span>

|<span data-ttu-id="7d69b-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7d69b-115">**Attribute**</span></span>|<span data-ttu-id="7d69b-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d69b-116">**Type**</span></span>|<span data-ttu-id="7d69b-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7d69b-117">**Required**</span></span>|<span data-ttu-id="7d69b-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7d69b-118">**Description**</span></span>|<span data-ttu-id="7d69b-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7d69b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7d69b-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="7d69b-120">AuthorID</span></span>  <br/> |<span data-ttu-id="7d69b-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7d69b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d69b-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7d69b-122">required</span></span>  <br/> ||<span data-ttu-id="7d69b-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7d69b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7d69b-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="7d69b-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="7d69b-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7d69b-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d69b-126">opcional</span><span class="sxs-lookup"><span data-stu-id="7d69b-126">optional</span></span>  <br/> ||<span data-ttu-id="7d69b-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7d69b-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7d69b-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="7d69b-128">CommentID</span></span>  <br/> |<span data-ttu-id="7d69b-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7d69b-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d69b-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7d69b-130">required</span></span>  <br/> ||<span data-ttu-id="7d69b-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7d69b-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7d69b-132">Data</span><span class="sxs-lookup"><span data-stu-id="7d69b-132">Date</span></span>  <br/> |<span data-ttu-id="7d69b-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="7d69b-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="7d69b-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7d69b-134">required</span></span>  <br/> ||<span data-ttu-id="7d69b-135">Valores do tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="7d69b-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="7d69b-136">Done</span><span class="sxs-lookup"><span data-stu-id="7d69b-136">Done</span></span>  <br/> |<span data-ttu-id="7d69b-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7d69b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7d69b-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7d69b-138">optional</span></span>  <br/> ||<span data-ttu-id="7d69b-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="7d69b-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7d69b-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="7d69b-140">EditDate</span></span>  <br/> |<span data-ttu-id="7d69b-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="7d69b-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="7d69b-142">opcional</span><span class="sxs-lookup"><span data-stu-id="7d69b-142">optional</span></span>  <br/> ||<span data-ttu-id="7d69b-143">Valores do tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="7d69b-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="7d69b-144">PageID</span><span class="sxs-lookup"><span data-stu-id="7d69b-144">PageID</span></span>  <br/> |<span data-ttu-id="7d69b-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7d69b-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d69b-146">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7d69b-146">required</span></span>  <br/> ||<span data-ttu-id="7d69b-147">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7d69b-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7d69b-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="7d69b-148">ShapeID</span></span>  <br/> |<span data-ttu-id="7d69b-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7d69b-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d69b-150">opcional</span><span class="sxs-lookup"><span data-stu-id="7d69b-150">optional</span></span>  <br/> ||<span data-ttu-id="7d69b-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7d69b-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

