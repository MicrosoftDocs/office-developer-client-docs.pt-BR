---
title: Elemento EventItem (EventList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula um código de evento.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394395"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="a319b-103">Elemento EventItem (EventList_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a319b-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a319b-104">Encapsula um código de evento.</span><span class="sxs-lookup"><span data-stu-id="a319b-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a319b-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="a319b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a319b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a319b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a319b-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="a319b-107">EventItem_Type complexType</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a319b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a319b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a319b-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a319b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a319b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a319b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a319b-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="a319b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a319b-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="a319b-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a319b-113">Definição</span><span class="sxs-lookup"><span data-stu-id="a319b-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a319b-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a319b-114">Elements and attributes</span></span>

<span data-ttu-id="a319b-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a319b-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a319b-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a319b-116">Parent elements</span></span>

|<span data-ttu-id="a319b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a319b-117">**Element**</span></span>|<span data-ttu-id="a319b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a319b-118">**Type**</span></span>|<span data-ttu-id="a319b-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a319b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a319b-120">EventList</span><span class="sxs-lookup"><span data-stu-id="a319b-120">EventList Property</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a319b-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="a319b-121">EventList_Type complexType</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a319b-122">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="a319b-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a319b-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a319b-123">Child elements</span></span>

<span data-ttu-id="a319b-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a319b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a319b-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="a319b-125">Attributes</span></span>

|<span data-ttu-id="a319b-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a319b-126">**Attribute**</span></span>|<span data-ttu-id="a319b-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a319b-127">**Type**</span></span>|<span data-ttu-id="a319b-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a319b-128">**Required**</span></span>|<span data-ttu-id="a319b-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a319b-129">**Description**</span></span>|<span data-ttu-id="a319b-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a319b-130">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a319b-131">Ação</span><span class="sxs-lookup"><span data-stu-id="a319b-131">Action</span></span>  <br/> |<span data-ttu-id="a319b-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a319b-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a319b-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a319b-133">required</span></span>  <br/> |<span data-ttu-id="a319b-134">Especifica o código de ação do elemento pai **EventItem**.</span><span class="sxs-lookup"><span data-stu-id="a319b-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="a319b-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a319b-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a319b-136">Habilitado</span><span class="sxs-lookup"><span data-stu-id="a319b-136">Enabled</span></span>  <br/> |<span data-ttu-id="a319b-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a319b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a319b-138">opcional</span><span class="sxs-lookup"><span data-stu-id="a319b-138">optional</span></span>  <br/> |<span data-ttu-id="a319b-139">Representa um sinalizador que indica se o evento está ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="a319b-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="a319b-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a319b-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a319b-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="a319b-141">EventCode</span></span>  <br/> |<span data-ttu-id="a319b-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a319b-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a319b-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a319b-143">required</span></span>  <br/> |<span data-ttu-id="a319b-144">Um código que indica o evento que aciona o complemento.</span><span class="sxs-lookup"><span data-stu-id="a319b-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="a319b-145">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a319b-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a319b-146">ID</span><span class="sxs-lookup"><span data-stu-id="a319b-146">ID</span></span>  <br/> |<span data-ttu-id="a319b-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a319b-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a319b-148">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a319b-148">required</span></span>  <br/> |<span data-ttu-id="a319b-149">A ID do evento.</span><span class="sxs-lookup"><span data-stu-id="a319b-149">The unique ID of the event. Read only.</span></span>  <br/> |<span data-ttu-id="a319b-150">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a319b-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a319b-151">Destino</span><span class="sxs-lookup"><span data-stu-id="a319b-151">Target</span></span>  <br/> |<span data-ttu-id="a319b-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a319b-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a319b-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a319b-153">required</span></span>  <br/> |<span data-ttu-id="a319b-154">Especifica o destino de um evento.</span><span class="sxs-lookup"><span data-stu-id="a319b-154">Gets or sets the target of an event. Read/write.</span></span>  <br/> |<span data-ttu-id="a319b-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a319b-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a319b-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="a319b-156">TargetArgs Property</span></span>  <br/> |<span data-ttu-id="a319b-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a319b-157">xsd:string</span></span>  <br/> |<span data-ttu-id="a319b-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a319b-158">required</span></span>  <br/> |<span data-ttu-id="a319b-159">Especifica uma cadeia de caracteres que contém os argumentos a serem enviados para o destino de um evento.</span><span class="sxs-lookup"><span data-stu-id="a319b-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="a319b-160">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a319b-160">Values of the xsd:string type.</span></span>  <br/> |
   

