---
title: Elemento Connect (Connects_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541992"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a><span data-ttu-id="ad7ee-103">Elemento Connect (Connects_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="ad7ee-103">Connect element (Connects_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ad7ee-104">Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad7ee-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="ad7ee-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad7ee-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad7ee-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="ad7ee-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad7ee-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad7ee-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad7ee-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ad7ee-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad7ee-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad7ee-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="ad7ee-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad7ee-113">Definição</span><span class="sxs-lookup"><span data-stu-id="ad7ee-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad7ee-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ad7ee-114">Elements and attributes</span></span>

<span data-ttu-id="ad7ee-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad7ee-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ad7ee-116">Parent elements</span></span>

|<span data-ttu-id="ad7ee-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-117">**Element**</span></span>|<span data-ttu-id="ad7ee-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-118">**Type**</span></span>|<span data-ttu-id="ad7ee-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad7ee-120">Connects</span><span class="sxs-lookup"><span data-stu-id="ad7ee-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad7ee-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="ad7ee-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad7ee-122">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad7ee-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ad7ee-123">Child elements</span></span>

<span data-ttu-id="ad7ee-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad7ee-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad7ee-125">Attributes</span></span>

|<span data-ttu-id="ad7ee-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-126">**Attribute**</span></span>|<span data-ttu-id="ad7ee-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-127">**Type**</span></span>|<span data-ttu-id="ad7ee-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-128">**Required**</span></span>|<span data-ttu-id="ad7ee-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-129">**Description**</span></span>|<span data-ttu-id="ad7ee-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ad7ee-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad7ee-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="ad7ee-131">FromCell</span></span>  <br/> |<span data-ttu-id="ad7ee-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ad7ee-132">xsd:string</span></span>  <br/> |<span data-ttu-id="ad7ee-133">opcional</span><span class="sxs-lookup"><span data-stu-id="ad7ee-133">optional</span></span>  <br/> |<span data-ttu-id="ad7ee-134">A célula da qual uma conexão se origina.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="ad7ee-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad7ee-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="ad7ee-136">FromPart</span></span>  <br/> |<span data-ttu-id="ad7ee-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="ad7ee-137">xsd:int</span></span>  <br/> |<span data-ttu-id="ad7ee-138">opcional</span><span class="sxs-lookup"><span data-stu-id="ad7ee-138">optional</span></span>  <br/> |<span data-ttu-id="ad7ee-139">A parte de uma forma da qual uma conexão se origina.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="ad7ee-140">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="ad7ee-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="ad7ee-141">FromSheet</span></span>  <br/> |<span data-ttu-id="ad7ee-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad7ee-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad7ee-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ad7ee-143">required</span></span>  <br/> |<span data-ttu-id="ad7ee-144">A ID da forma a partir da qual uma ou mais conexões se originam.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="ad7ee-145">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad7ee-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="ad7ee-146">ToCell</span></span>  <br/> |<span data-ttu-id="ad7ee-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ad7ee-147">xsd:string</span></span>  <br/> |<span data-ttu-id="ad7ee-148">opcional</span><span class="sxs-lookup"><span data-stu-id="ad7ee-148">optional</span></span>  <br/> |<span data-ttu-id="ad7ee-149">A célula à qual uma conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="ad7ee-150">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad7ee-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="ad7ee-151">ToPart</span></span>  <br/> |<span data-ttu-id="ad7ee-152">xsd:int</span><span class="sxs-lookup"><span data-stu-id="ad7ee-152">xsd:int</span></span>  <br/> |<span data-ttu-id="ad7ee-153">opcional</span><span class="sxs-lookup"><span data-stu-id="ad7ee-153">optional</span></span>  <br/> |<span data-ttu-id="ad7ee-154">A parte de uma forma à qual uma conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="ad7ee-155">Valores do tipo xsd:Int.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="ad7ee-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="ad7ee-156">ToSheet</span></span>  <br/> |<span data-ttu-id="ad7ee-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad7ee-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad7ee-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ad7ee-158">required</span></span>  <br/> |<span data-ttu-id="ad7ee-159">A ID da forma à qual uma ou mais conexões foram feitas.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="ad7ee-160">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

