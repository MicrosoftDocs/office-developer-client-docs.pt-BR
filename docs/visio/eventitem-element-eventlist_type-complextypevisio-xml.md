---
title: Elemento EventItem (EventList_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula um código de evento.
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541835"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="1f783-103">Elemento EventItem (EventList_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="1f783-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1f783-104">Encapsula um código de evento.</span><span class="sxs-lookup"><span data-stu-id="1f783-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f783-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="1f783-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f783-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1f783-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1f783-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="1f783-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1f783-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1f783-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1f783-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1f783-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1f783-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1f783-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1f783-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="1f783-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1f783-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="1f783-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1f783-113">Definição</span><span class="sxs-lookup"><span data-stu-id="1f783-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1f783-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1f783-114">Elements and attributes</span></span>

<span data-ttu-id="1f783-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1f783-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1f783-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1f783-116">Parent elements</span></span>

|<span data-ttu-id="1f783-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1f783-117">**Element**</span></span>|<span data-ttu-id="1f783-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1f783-118">**Type**</span></span>|<span data-ttu-id="1f783-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1f783-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1f783-120">EventList</span><span class="sxs-lookup"><span data-stu-id="1f783-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f783-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="1f783-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1f783-122">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="1f783-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1f783-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1f783-123">Child elements</span></span>

<span data-ttu-id="1f783-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1f783-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f783-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f783-125">Attributes</span></span>

|<span data-ttu-id="1f783-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1f783-126">**Attribute**</span></span>|<span data-ttu-id="1f783-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1f783-127">**Type**</span></span>|<span data-ttu-id="1f783-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="1f783-128">**Required**</span></span>|<span data-ttu-id="1f783-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1f783-129">**Description**</span></span>|<span data-ttu-id="1f783-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="1f783-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1f783-131">Ação</span><span class="sxs-lookup"><span data-stu-id="1f783-131">Action</span></span>  <br/> |<span data-ttu-id="1f783-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1f783-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1f783-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1f783-133">required</span></span>  <br/> |<span data-ttu-id="1f783-134">Especifica o código de ação do elemento pai **EventItem**.</span><span class="sxs-lookup"><span data-stu-id="1f783-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="1f783-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1f783-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1f783-136">Habilitado</span><span class="sxs-lookup"><span data-stu-id="1f783-136">Enabled</span></span>  <br/> |<span data-ttu-id="1f783-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1f783-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1f783-138">opcional</span><span class="sxs-lookup"><span data-stu-id="1f783-138">optional</span></span>  <br/> |<span data-ttu-id="1f783-139">Representa um sinalizador que indica se o evento está ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="1f783-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="1f783-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1f783-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1f783-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="1f783-141">EventCode</span></span>  <br/> |<span data-ttu-id="1f783-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1f783-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1f783-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1f783-143">required</span></span>  <br/> |<span data-ttu-id="1f783-144">Um código que indica o evento que aciona o complemento.</span><span class="sxs-lookup"><span data-stu-id="1f783-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="1f783-145">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1f783-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1f783-146">ID</span><span class="sxs-lookup"><span data-stu-id="1f783-146">ID</span></span>  <br/> |<span data-ttu-id="1f783-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1f783-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1f783-148">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1f783-148">required</span></span>  <br/> |<span data-ttu-id="1f783-149">A ID do evento.</span><span class="sxs-lookup"><span data-stu-id="1f783-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="1f783-150">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1f783-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1f783-151">Destino</span><span class="sxs-lookup"><span data-stu-id="1f783-151">Target</span></span>  <br/> |<span data-ttu-id="1f783-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1f783-152">xsd:string</span></span>  <br/> |<span data-ttu-id="1f783-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1f783-153">required</span></span>  <br/> |<span data-ttu-id="1f783-154">Especifica o destino de um evento.</span><span class="sxs-lookup"><span data-stu-id="1f783-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="1f783-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1f783-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1f783-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="1f783-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="1f783-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1f783-157">xsd:string</span></span>  <br/> |<span data-ttu-id="1f783-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1f783-158">required</span></span>  <br/> |<span data-ttu-id="1f783-159">Especifica uma cadeia de caracteres que contém os argumentos a serem enviados para o destino de um evento.</span><span class="sxs-lookup"><span data-stu-id="1f783-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="1f783-160">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1f783-160">Values of the xsd:string type.</span></span>  <br/> |
   

