---
title: Elemento EventItem (EventList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula um código de evento.
ms.openlocfilehash: dcdd3aa264e8ddfb1aa6f2e908f1c43a0d470872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771818"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="8c725-103">Elemento EventItem (EventList_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8c725-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8c725-104">Encapsula um código de evento.</span><span class="sxs-lookup"><span data-stu-id="8c725-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c725-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="8c725-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c725-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8c725-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8c725-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="8c725-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8c725-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8c725-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8c725-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8c725-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8c725-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8c725-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8c725-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="8c725-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8c725-112">Document</span><span class="sxs-lookup"><span data-stu-id="8c725-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8c725-113">Definição</span><span class="sxs-lookup"><span data-stu-id="8c725-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8c725-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8c725-114">Elements and attributes</span></span>

<span data-ttu-id="8c725-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8c725-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8c725-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8c725-116">Parent elements</span></span>

|<span data-ttu-id="8c725-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8c725-117">**Element**</span></span>|<span data-ttu-id="8c725-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8c725-118">**Type**</span></span>|<span data-ttu-id="8c725-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8c725-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8c725-120">EventList</span><span class="sxs-lookup"><span data-stu-id="8c725-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c725-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="8c725-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8c725-122">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="8c725-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8c725-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8c725-123">Child elements</span></span>

<span data-ttu-id="8c725-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8c725-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c725-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="8c725-125">Attributes</span></span>

|<span data-ttu-id="8c725-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8c725-126">**Attribute**</span></span>|<span data-ttu-id="8c725-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8c725-127">**Type**</span></span>|<span data-ttu-id="8c725-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8c725-128">**Required**</span></span>|<span data-ttu-id="8c725-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8c725-129">**Description**</span></span>|<span data-ttu-id="8c725-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8c725-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8c725-131">Ação</span><span class="sxs-lookup"><span data-stu-id="8c725-131">Action</span></span>  <br/> |<span data-ttu-id="8c725-132">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8c725-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8c725-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8c725-133">required</span></span>  <br/> |<span data-ttu-id="8c725-134">Especifica o código de ação do elemento **EventItem** pai.</span><span class="sxs-lookup"><span data-stu-id="8c725-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="8c725-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8c725-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8c725-136">Habilitado</span><span class="sxs-lookup"><span data-stu-id="8c725-136">Enabled</span></span>  <br/> |<span data-ttu-id="8c725-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="8c725-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8c725-138">opcional</span><span class="sxs-lookup"><span data-stu-id="8c725-138">optional</span></span>  <br/> |<span data-ttu-id="8c725-139">Representa um sinalizador que indica se o evento está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8c725-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="8c725-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8c725-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8c725-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="8c725-141">EventCode</span></span>  <br/> |<span data-ttu-id="8c725-142">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8c725-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8c725-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8c725-143">required</span></span>  <br/> |<span data-ttu-id="8c725-144">Um código que indica o evento que dispara o complemento.</span><span class="sxs-lookup"><span data-stu-id="8c725-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="8c725-145">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8c725-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8c725-146">ID</span><span class="sxs-lookup"><span data-stu-id="8c725-146">ID</span></span>  <br/> |<span data-ttu-id="8c725-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8c725-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8c725-148">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8c725-148">required</span></span>  <br/> |<span data-ttu-id="8c725-149">A ID do evento.</span><span class="sxs-lookup"><span data-stu-id="8c725-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="8c725-150">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8c725-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8c725-151">Destino</span><span class="sxs-lookup"><span data-stu-id="8c725-151">Target</span></span>  <br/> |<span data-ttu-id="8c725-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8c725-152">xsd:string</span></span>  <br/> |<span data-ttu-id="8c725-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8c725-153">required</span></span>  <br/> |<span data-ttu-id="8c725-154">Especifica o destino de um evento.</span><span class="sxs-lookup"><span data-stu-id="8c725-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="8c725-155">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8c725-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8c725-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="8c725-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="8c725-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8c725-157">xsd:string</span></span>  <br/> |<span data-ttu-id="8c725-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8c725-158">required</span></span>  <br/> |<span data-ttu-id="8c725-159">Especifica uma cadeia de caracteres que contém os argumentos a serem enviados para o destino de um evento.</span><span class="sxs-lookup"><span data-stu-id="8c725-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="8c725-160">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8c725-160">Values of the xsd:string type.</span></span>  <br/> |
   

