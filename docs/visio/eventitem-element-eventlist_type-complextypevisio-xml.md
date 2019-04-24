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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337195"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="cbf58-103">Elemento EventItem (EventList_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="cbf58-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cbf58-104">Encapsula um código de evento.</span><span class="sxs-lookup"><span data-stu-id="cbf58-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cbf58-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="cbf58-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbf58-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cbf58-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cbf58-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="cbf58-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cbf58-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cbf58-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cbf58-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cbf58-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cbf58-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cbf58-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cbf58-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="cbf58-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cbf58-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="cbf58-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cbf58-113">Definição</span><span class="sxs-lookup"><span data-stu-id="cbf58-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cbf58-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cbf58-114">Elements and attributes</span></span>

<span data-ttu-id="cbf58-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cbf58-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cbf58-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="cbf58-116">Parent elements</span></span>

|<span data-ttu-id="cbf58-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cbf58-117">**Element**</span></span>|<span data-ttu-id="cbf58-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cbf58-118">**Type**</span></span>|<span data-ttu-id="cbf58-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cbf58-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cbf58-120">EventList</span><span class="sxs-lookup"><span data-stu-id="cbf58-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cbf58-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="cbf58-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cbf58-122">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="cbf58-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cbf58-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cbf58-123">Child elements</span></span>

<span data-ttu-id="cbf58-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="cbf58-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbf58-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="cbf58-125">Attributes</span></span>

|<span data-ttu-id="cbf58-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cbf58-126">**Attribute**</span></span>|<span data-ttu-id="cbf58-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cbf58-127">**Type**</span></span>|<span data-ttu-id="cbf58-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="cbf58-128">**Required**</span></span>|<span data-ttu-id="cbf58-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cbf58-129">**Description**</span></span>|<span data-ttu-id="cbf58-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="cbf58-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cbf58-131">Ação</span><span class="sxs-lookup"><span data-stu-id="cbf58-131">Action</span></span>  <br/> |<span data-ttu-id="cbf58-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cbf58-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cbf58-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbf58-133">required</span></span>  <br/> |<span data-ttu-id="cbf58-134">Especifica o código de ação do elemento pai **EventItem**.</span><span class="sxs-lookup"><span data-stu-id="cbf58-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="cbf58-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="cbf58-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cbf58-136">Habilitado</span><span class="sxs-lookup"><span data-stu-id="cbf58-136">Enabled</span></span>  <br/> |<span data-ttu-id="cbf58-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="cbf58-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cbf58-138">opcional</span><span class="sxs-lookup"><span data-stu-id="cbf58-138">optional</span></span>  <br/> |<span data-ttu-id="cbf58-139">Representa um sinalizador que indica se o evento está ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="cbf58-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="cbf58-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="cbf58-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cbf58-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="cbf58-141">EventCode</span></span>  <br/> |<span data-ttu-id="cbf58-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cbf58-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cbf58-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbf58-143">required</span></span>  <br/> |<span data-ttu-id="cbf58-144">Um código que indica o evento que aciona o complemento.</span><span class="sxs-lookup"><span data-stu-id="cbf58-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="cbf58-145">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="cbf58-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cbf58-146">ID</span><span class="sxs-lookup"><span data-stu-id="cbf58-146">ID</span></span>  <br/> |<span data-ttu-id="cbf58-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cbf58-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cbf58-148">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbf58-148">required</span></span>  <br/> |<span data-ttu-id="cbf58-149">A ID do evento.</span><span class="sxs-lookup"><span data-stu-id="cbf58-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="cbf58-150">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cbf58-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cbf58-151">Destino</span><span class="sxs-lookup"><span data-stu-id="cbf58-151">Target</span></span>  <br/> |<span data-ttu-id="cbf58-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cbf58-152">xsd:string</span></span>  <br/> |<span data-ttu-id="cbf58-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbf58-153">required</span></span>  <br/> |<span data-ttu-id="cbf58-154">Especifica o destino de um evento.</span><span class="sxs-lookup"><span data-stu-id="cbf58-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="cbf58-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cbf58-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cbf58-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="cbf58-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="cbf58-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cbf58-157">xsd:string</span></span>  <br/> |<span data-ttu-id="cbf58-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbf58-158">required</span></span>  <br/> |<span data-ttu-id="cbf58-159">Especifica uma cadeia de caracteres que contém os argumentos a serem enviados para o destino de um evento.</span><span class="sxs-lookup"><span data-stu-id="cbf58-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="cbf58-160">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cbf58-160">Values of the xsd:string type.</span></span>  <br/> |
   

