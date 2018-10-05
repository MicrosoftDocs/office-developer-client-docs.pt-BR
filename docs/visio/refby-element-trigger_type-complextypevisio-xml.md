---
title: Elemento RefBy (Trigger_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Especifica uma referência a uma página de desenho.
ms.openlocfilehash: d987825345b64bd6e202970fc786aedaf49c6a94
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383314"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="ee595-103">Elemento RefBy (Trigger_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ee595-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ee595-104">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="ee595-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ee595-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="ee595-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee595-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ee595-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ee595-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="ee595-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ee595-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ee595-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ee595-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ee595-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ee595-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ee595-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ee595-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="ee595-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="ee595-112">Definição</span><span class="sxs-lookup"><span data-stu-id="ee595-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ee595-113">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ee595-113">Elements and attributes</span></span>

<span data-ttu-id="ee595-114">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ee595-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ee595-115">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ee595-115">Parent elements</span></span>

|<span data-ttu-id="ee595-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ee595-116">**Element**</span></span>|<span data-ttu-id="ee595-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ee595-117">**Type**</span></span>|<span data-ttu-id="ee595-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ee595-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ee595-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="ee595-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="ee595-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="ee595-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ee595-121">Fornece instruções para o Microsoft Visio recalcular uma relação entre as partes de documentos em um arquivo do Visio.</span><span class="sxs-lookup"><span data-stu-id="ee595-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="ee595-122">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ee595-122">Child elements</span></span>

<span data-ttu-id="ee595-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ee595-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee595-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee595-124">Attributes</span></span>

|<span data-ttu-id="ee595-125">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ee595-125">**Attribute**</span></span>|<span data-ttu-id="ee595-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ee595-126">**Type**</span></span>|<span data-ttu-id="ee595-127">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ee595-127">**Required**</span></span>|<span data-ttu-id="ee595-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ee595-128">**Description**</span></span>|<span data-ttu-id="ee595-129">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ee595-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ee595-130">ID</span><span class="sxs-lookup"><span data-stu-id="ee595-130">ID</span></span>  <br/> |<span data-ttu-id="ee595-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ee595-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee595-132">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ee595-132">required</span></span>  <br/> |<span data-ttu-id="ee595-133">Especifica o atributo ID de uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="ee595-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="ee595-134">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ee595-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee595-135">T</span><span class="sxs-lookup"><span data-stu-id="ee595-135">T</span></span>  <br/> |<span data-ttu-id="ee595-136">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ee595-136">xsd:string</span></span>  <br/> |<span data-ttu-id="ee595-137">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ee595-137">required</span></span>  <br/> |<span data-ttu-id="ee595-138">Especifica o tipo de referência.</span><span class="sxs-lookup"><span data-stu-id="ee595-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="ee595-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ee595-139">Values of the xsd:string type.</span></span>  <br/> |
   

