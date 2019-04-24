---
title: Elemento Connect (Connects_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346505"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="a4339-103">Elemento Connect (Connects_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a4339-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a4339-104">Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.</span><span class="sxs-lookup"><span data-stu-id="a4339-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4339-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="a4339-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4339-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a4339-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a4339-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="a4339-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a4339-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a4339-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a4339-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a4339-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a4339-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a4339-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a4339-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="a4339-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a4339-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="a4339-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a4339-113">Definição</span><span class="sxs-lookup"><span data-stu-id="a4339-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a4339-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a4339-114">Elements and attributes</span></span>

<span data-ttu-id="a4339-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a4339-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a4339-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a4339-116">Parent elements</span></span>

|<span data-ttu-id="a4339-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a4339-117">**Element**</span></span>|<span data-ttu-id="a4339-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a4339-118">**Type**</span></span>|<span data-ttu-id="a4339-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a4339-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4339-120">Connects</span><span class="sxs-lookup"><span data-stu-id="a4339-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a4339-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="a4339-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a4339-122">Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.</span><span class="sxs-lookup"><span data-stu-id="a4339-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a4339-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a4339-123">Child elements</span></span>

<span data-ttu-id="a4339-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a4339-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4339-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="a4339-125">Attributes</span></span>

|<span data-ttu-id="a4339-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a4339-126">**Attribute**</span></span>|<span data-ttu-id="a4339-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a4339-127">**Type**</span></span>|<span data-ttu-id="a4339-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a4339-128">**Required**</span></span>|<span data-ttu-id="a4339-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a4339-129">**Description**</span></span>|<span data-ttu-id="a4339-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a4339-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a4339-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="a4339-131">FromCell</span></span>  <br/> |<span data-ttu-id="a4339-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a4339-132">xsd:string</span></span>  <br/> |<span data-ttu-id="a4339-133">opcional</span><span class="sxs-lookup"><span data-stu-id="a4339-133">optional</span></span>  <br/> |<span data-ttu-id="a4339-134">A célula da qual uma conexão se origina.</span><span class="sxs-lookup"><span data-stu-id="a4339-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="a4339-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a4339-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a4339-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="a4339-136">FromPart</span></span>  <br/> |<span data-ttu-id="a4339-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="a4339-137">xsd:int</span></span>  <br/> |<span data-ttu-id="a4339-138">opcional</span><span class="sxs-lookup"><span data-stu-id="a4339-138">optional</span></span>  <br/> |<span data-ttu-id="a4339-139">A parte de uma forma da qual uma conexão se origina.</span><span class="sxs-lookup"><span data-stu-id="a4339-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="a4339-140">Valores do tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="a4339-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="a4339-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="a4339-141">FromSheet</span></span>  <br/> |<span data-ttu-id="a4339-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a4339-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a4339-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a4339-143">required</span></span>  <br/> |<span data-ttu-id="a4339-144">A ID da forma a partir da qual uma ou mais conexões se originam.</span><span class="sxs-lookup"><span data-stu-id="a4339-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="a4339-145">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a4339-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a4339-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="a4339-146">ToCell</span></span>  <br/> |<span data-ttu-id="a4339-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a4339-147">xsd:string</span></span>  <br/> |<span data-ttu-id="a4339-148">opcional</span><span class="sxs-lookup"><span data-stu-id="a4339-148">optional</span></span>  <br/> |<span data-ttu-id="a4339-149">A célula à qual uma conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="a4339-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="a4339-150">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a4339-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a4339-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="a4339-151">ToPart</span></span>  <br/> |<span data-ttu-id="a4339-152">xsd:int</span><span class="sxs-lookup"><span data-stu-id="a4339-152">xsd:int</span></span>  <br/> |<span data-ttu-id="a4339-153">opcional</span><span class="sxs-lookup"><span data-stu-id="a4339-153">optional</span></span>  <br/> |<span data-ttu-id="a4339-154">A parte de uma forma à qual uma conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="a4339-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="a4339-155">Valores do tipo xsd:Int.</span><span class="sxs-lookup"><span data-stu-id="a4339-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="a4339-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="a4339-156">ToSheet</span></span>  <br/> |<span data-ttu-id="a4339-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a4339-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a4339-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a4339-158">required</span></span>  <br/> |<span data-ttu-id="a4339-159">A ID da forma à qual uma ou mais conexões foram feitas.</span><span class="sxs-lookup"><span data-stu-id="a4339-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="a4339-160">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a4339-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

