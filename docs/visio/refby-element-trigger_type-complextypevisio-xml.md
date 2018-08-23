---
title: Elemento RefBy (Trigger_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Especifica uma referência a uma página de desenho.
ms.openlocfilehash: e4726a8fe49a7492cd2f7833bbcf5e6810bae18d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572428"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="e2417-103">Elemento RefBy (Trigger_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e2417-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e2417-104">Especifica uma referência a uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="e2417-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2417-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="e2417-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2417-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e2417-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e2417-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="e2417-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e2417-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e2417-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e2417-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e2417-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e2417-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e2417-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e2417-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="e2417-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="e2417-112">Definição</span><span class="sxs-lookup"><span data-stu-id="e2417-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e2417-113">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="e2417-113">Elements and attributes</span></span>

<span data-ttu-id="e2417-114">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="e2417-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e2417-115">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e2417-115">Parent elements</span></span>

|<span data-ttu-id="e2417-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e2417-116">**Element**</span></span>|<span data-ttu-id="e2417-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e2417-117">**Type**</span></span>|<span data-ttu-id="e2417-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e2417-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e2417-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="e2417-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="e2417-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="e2417-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2417-121">Fornece instruções para o Microsoft Visio recalcular uma relação entre as partes de documentos em um arquivo do Visio.</span><span class="sxs-lookup"><span data-stu-id="e2417-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="e2417-122">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e2417-122">Child elements</span></span>

<span data-ttu-id="e2417-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e2417-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2417-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="e2417-124">Attributes</span></span>

|<span data-ttu-id="e2417-125">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e2417-125">**Attribute**</span></span>|<span data-ttu-id="e2417-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e2417-126">**Type**</span></span>|<span data-ttu-id="e2417-127">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="e2417-127">**Required**</span></span>|<span data-ttu-id="e2417-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e2417-128">**Description**</span></span>|<span data-ttu-id="e2417-129">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="e2417-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e2417-130">ID</span><span class="sxs-lookup"><span data-stu-id="e2417-130">ID</span></span>  <br/> |<span data-ttu-id="e2417-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e2417-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e2417-132">obrigatório</span><span class="sxs-lookup"><span data-stu-id="e2417-132">required</span></span>  <br/> |<span data-ttu-id="e2417-133">Especifica o atributo ID de uma página de desenho.</span><span class="sxs-lookup"><span data-stu-id="e2417-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="e2417-134">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e2417-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e2417-135">T</span><span class="sxs-lookup"><span data-stu-id="e2417-135">T</span></span>  <br/> |<span data-ttu-id="e2417-136">XSD: String</span><span class="sxs-lookup"><span data-stu-id="e2417-136">xsd:string</span></span>  <br/> |<span data-ttu-id="e2417-137">obrigatório</span><span class="sxs-lookup"><span data-stu-id="e2417-137">required</span></span>  <br/> |<span data-ttu-id="e2417-138">Especifica o tipo de referência.</span><span class="sxs-lookup"><span data-stu-id="e2417-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="e2417-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e2417-139">Values of the xsd:string type.</span></span>  <br/> |
   

