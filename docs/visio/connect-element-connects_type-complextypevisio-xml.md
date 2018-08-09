---
title: Conecte-se o elemento (Connects_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.\n"
ms.openlocfilehash: 1bd3e1f006afe8d5bbb698e0b3a2179b74728315
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771582"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="84207-103">Conecte-se o elemento (Connects_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="84207-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="84207-104">
			Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.
</span><span class="sxs-lookup"><span data-stu-id="84207-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84207-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="84207-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84207-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="84207-106">**Element type**</span></span> <br/> |[<span data-ttu-id="84207-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="84207-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="84207-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="84207-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="84207-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="84207-109">**Schema file**</span></span> <br/> |<span data-ttu-id="84207-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="84207-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="84207-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="84207-111">**Document parts**</span></span> <br/> |<span data-ttu-id="84207-112">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="84207-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="84207-113">Definição</span><span class="sxs-lookup"><span data-stu-id="84207-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="84207-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="84207-114">Elements and attributes</span></span>

<span data-ttu-id="84207-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="84207-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="84207-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="84207-116">Parent elements</span></span>

|<span data-ttu-id="84207-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="84207-117">**Element**</span></span>|<span data-ttu-id="84207-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="84207-118">**Type**</span></span>|<span data-ttu-id="84207-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="84207-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="84207-120">Connects</span><span class="sxs-lookup"><span data-stu-id="84207-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="84207-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="84207-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="84207-122">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="84207-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="84207-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="84207-123">Child elements</span></span>

<span data-ttu-id="84207-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="84207-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84207-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="84207-125">Attributes</span></span>

|<span data-ttu-id="84207-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="84207-126">**Attribute**</span></span>|<span data-ttu-id="84207-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="84207-127">**Type**</span></span>|<span data-ttu-id="84207-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="84207-128">**Required**</span></span>|<span data-ttu-id="84207-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="84207-129">**Description**</span></span>|<span data-ttu-id="84207-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="84207-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="84207-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="84207-131">FromCell</span></span>  <br/> |<span data-ttu-id="84207-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="84207-132">xsd:string</span></span>  <br/> |<span data-ttu-id="84207-133">opcional</span><span class="sxs-lookup"><span data-stu-id="84207-133">optional</span></span>  <br/> |<span data-ttu-id="84207-134">A célula do qual se origina uma conexão.</span><span class="sxs-lookup"><span data-stu-id="84207-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="84207-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="84207-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="84207-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="84207-136">FromPart</span></span>  <br/> |<span data-ttu-id="84207-137">XSD:int</span><span class="sxs-lookup"><span data-stu-id="84207-137">xsd:int</span></span>  <br/> |<span data-ttu-id="84207-138">opcional</span><span class="sxs-lookup"><span data-stu-id="84207-138">optional</span></span>  <br/> |<span data-ttu-id="84207-139">A parte de uma forma a partir do qual se origina uma conexão.</span><span class="sxs-lookup"><span data-stu-id="84207-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="84207-140">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="84207-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="84207-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="84207-141">FromSheet</span></span>  <br/> |<span data-ttu-id="84207-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="84207-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="84207-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="84207-143">required</span></span>  <br/> |<span data-ttu-id="84207-144">A identificação da forma da qual uma conexão ou conexões se originam.</span><span class="sxs-lookup"><span data-stu-id="84207-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="84207-145">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="84207-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="84207-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="84207-146">ToCell</span></span>  <br/> |<span data-ttu-id="84207-147">XSD: String</span><span class="sxs-lookup"><span data-stu-id="84207-147">xsd:string</span></span>  <br/> |<span data-ttu-id="84207-148">opcional</span><span class="sxs-lookup"><span data-stu-id="84207-148">optional</span></span>  <br/> |<span data-ttu-id="84207-149">A célula à qual uma conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="84207-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="84207-150">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="84207-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="84207-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="84207-151">ToPart</span></span>  <br/> |<span data-ttu-id="84207-152">XSD:int</span><span class="sxs-lookup"><span data-stu-id="84207-152">xsd:int</span></span>  <br/> |<span data-ttu-id="84207-153">opcional</span><span class="sxs-lookup"><span data-stu-id="84207-153">optional</span></span>  <br/> |<span data-ttu-id="84207-154">A parte de uma forma ao qual uma conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="84207-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="84207-155">Valores do tipo xsd:Int.</span><span class="sxs-lookup"><span data-stu-id="84207-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="84207-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="84207-156">ToSheet</span></span>  <br/> |<span data-ttu-id="84207-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="84207-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="84207-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="84207-158">required</span></span>  <br/> |<span data-ttu-id="84207-159">A identificação da forma à qual uma ou mais conexões são feitas.</span><span class="sxs-lookup"><span data-stu-id="84207-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="84207-160">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="84207-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

