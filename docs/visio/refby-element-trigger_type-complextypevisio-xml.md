---
title: Elemento RefBy (Trigger_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Especifica uma referência a uma página no desenho.
ms.openlocfilehash: 6d081ad1bf9e089a16820db33cec92694db7ac98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538288"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a><span data-ttu-id="185d9-103">Elemento RefBy (Trigger_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="185d9-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="185d9-104">Especifica uma referência a uma página no desenho.</span><span class="sxs-lookup"><span data-stu-id="185d9-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="185d9-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="185d9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="185d9-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="185d9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="185d9-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="185d9-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="185d9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="185d9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="185d9-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="185d9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="185d9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="185d9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="185d9-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="185d9-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="185d9-112">Definição</span><span class="sxs-lookup"><span data-stu-id="185d9-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="185d9-113">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="185d9-113">Elements and attributes</span></span>

<span data-ttu-id="185d9-114">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="185d9-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="185d9-115">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="185d9-115">Parent elements</span></span>

|<span data-ttu-id="185d9-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="185d9-116">**Element**</span></span>|<span data-ttu-id="185d9-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="185d9-117">**Type**</span></span>|<span data-ttu-id="185d9-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="185d9-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="185d9-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="185d9-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="185d9-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="185d9-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="185d9-121">Fornece instruções ao Microsoft Visio para recalcular uma relação entre partes do documento em um arquivo do Visio.</span><span class="sxs-lookup"><span data-stu-id="185d9-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="185d9-122">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="185d9-122">Child elements</span></span>

<span data-ttu-id="185d9-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="185d9-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="185d9-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="185d9-124">Attributes</span></span>

|<span data-ttu-id="185d9-125">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="185d9-125">**Attribute**</span></span>|<span data-ttu-id="185d9-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="185d9-126">**Type**</span></span>|<span data-ttu-id="185d9-127">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="185d9-127">**Required**</span></span>|<span data-ttu-id="185d9-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="185d9-128">**Description**</span></span>|<span data-ttu-id="185d9-129">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="185d9-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="185d9-130">ID</span><span class="sxs-lookup"><span data-stu-id="185d9-130">ID</span></span>  <br/> |<span data-ttu-id="185d9-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="185d9-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="185d9-132">obrigatório</span><span class="sxs-lookup"><span data-stu-id="185d9-132">required</span></span>  <br/> |<span data-ttu-id="185d9-133">Especifica o atributo ID de uma página no desenho.</span><span class="sxs-lookup"><span data-stu-id="185d9-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="185d9-134">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="185d9-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="185d9-135">T</span><span class="sxs-lookup"><span data-stu-id="185d9-135">T</span></span>  <br/> |<span data-ttu-id="185d9-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="185d9-136">xsd:string</span></span>  <br/> |<span data-ttu-id="185d9-137">obrigatório</span><span class="sxs-lookup"><span data-stu-id="185d9-137">required</span></span>  <br/> |<span data-ttu-id="185d9-138">Especifica o tipo de referência.</span><span class="sxs-lookup"><span data-stu-id="185d9-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="185d9-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="185d9-139">Values of the xsd:string type.</span></span>  <br/> |
   

