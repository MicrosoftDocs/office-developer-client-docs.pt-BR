---
title: Elemento RefBy (Trigger_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Especifica uma referência a uma página no desenho.
ms.openlocfilehash: d987825345b64bd6e202970fc786aedaf49c6a94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348402"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="790f2-103">Elemento RefBy (Trigger_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="790f2-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="790f2-104">Especifica uma referência a uma página no desenho.</span><span class="sxs-lookup"><span data-stu-id="790f2-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="790f2-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="790f2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="790f2-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="790f2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="790f2-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="790f2-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="790f2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="790f2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="790f2-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="790f2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="790f2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="790f2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="790f2-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="790f2-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="790f2-112">Definição</span><span class="sxs-lookup"><span data-stu-id="790f2-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="790f2-113">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="790f2-113">Elements and attributes</span></span>

<span data-ttu-id="790f2-114">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="790f2-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="790f2-115">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="790f2-115">Parent elements</span></span>

|<span data-ttu-id="790f2-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="790f2-116">**Element**</span></span>|<span data-ttu-id="790f2-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="790f2-117">**Type**</span></span>|<span data-ttu-id="790f2-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="790f2-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="790f2-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="790f2-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="790f2-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="790f2-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="790f2-121">Fornece instruções para o Microsoft Visio recalcular uma relação entre partes do documento em um arquivo do Visio.</span><span class="sxs-lookup"><span data-stu-id="790f2-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="790f2-122">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="790f2-122">Child elements</span></span>

<span data-ttu-id="790f2-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="790f2-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="790f2-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="790f2-124">Attributes</span></span>

|<span data-ttu-id="790f2-125">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="790f2-125">**Attribute**</span></span>|<span data-ttu-id="790f2-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="790f2-126">**Type**</span></span>|<span data-ttu-id="790f2-127">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="790f2-127">**Required**</span></span>|<span data-ttu-id="790f2-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="790f2-128">**Description**</span></span>|<span data-ttu-id="790f2-129">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="790f2-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="790f2-130">ID</span><span class="sxs-lookup"><span data-stu-id="790f2-130">ID</span></span>  <br/> |<span data-ttu-id="790f2-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="790f2-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="790f2-132">obrigatório</span><span class="sxs-lookup"><span data-stu-id="790f2-132">required</span></span>  <br/> |<span data-ttu-id="790f2-133">Especifica o atributo ID de uma página no desenho.</span><span class="sxs-lookup"><span data-stu-id="790f2-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="790f2-134">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="790f2-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="790f2-135">T</span><span class="sxs-lookup"><span data-stu-id="790f2-135">T</span></span>  <br/> |<span data-ttu-id="790f2-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="790f2-136">xsd:string</span></span>  <br/> |<span data-ttu-id="790f2-137">obrigatório</span><span class="sxs-lookup"><span data-stu-id="790f2-137">required</span></span>  <br/> |<span data-ttu-id="790f2-138">Especifica o tipo de referência.</span><span class="sxs-lookup"><span data-stu-id="790f2-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="790f2-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="790f2-139">Values of the xsd:string type.</span></span>  <br/> |
   

