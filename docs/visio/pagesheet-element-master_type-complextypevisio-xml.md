---
title: Elemento PageSheet (Master_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Especifica as propriedades da página de desenho associadas ao mestre.
ms.openlocfilehash: 94fde64b130c2a05c4bd70c97552fe4218171ce7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540613"
---
# <a name="pagesheet-element-master_type-complextype-visio-xml"></a><span data-ttu-id="947d2-103">Elemento PageSheet (Master_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="947d2-103">PageSheet element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="947d2-104">Especifica as propriedades da página de desenho associada ao mestre.</span><span class="sxs-lookup"><span data-stu-id="947d2-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="947d2-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="947d2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="947d2-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="947d2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="947d2-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="947d2-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="947d2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="947d2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="947d2-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="947d2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="947d2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="947d2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="947d2-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="947d2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="947d2-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="947d2-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="947d2-113">Definição</span><span class="sxs-lookup"><span data-stu-id="947d2-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="947d2-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="947d2-114">Elements and attributes</span></span>

<span data-ttu-id="947d2-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="947d2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="947d2-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="947d2-116">Parent elements</span></span>

|<span data-ttu-id="947d2-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="947d2-117">**Element**</span></span>|<span data-ttu-id="947d2-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="947d2-118">**Type**</span></span>|<span data-ttu-id="947d2-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="947d2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="947d2-120">Master</span><span class="sxs-lookup"><span data-stu-id="947d2-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="947d2-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="947d2-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="947d2-122">Especifica um mestre em um desenho.</span><span class="sxs-lookup"><span data-stu-id="947d2-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="947d2-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="947d2-123">Child elements</span></span>

<span data-ttu-id="947d2-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="947d2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="947d2-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="947d2-125">Attributes</span></span>

|<span data-ttu-id="947d2-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="947d2-126">**Attribute**</span></span>|<span data-ttu-id="947d2-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="947d2-127">**Type**</span></span>|<span data-ttu-id="947d2-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="947d2-128">**Required**</span></span>|<span data-ttu-id="947d2-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="947d2-129">**Description**</span></span>|<span data-ttu-id="947d2-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="947d2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="947d2-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="947d2-131">FillStyle</span></span>  <br/> |<span data-ttu-id="947d2-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="947d2-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="947d2-133">opcional</span><span class="sxs-lookup"><span data-stu-id="947d2-133">optional</span></span>  <br/> |<span data-ttu-id="947d2-134">especifica a ID da folha de estilos da qual será herdada a formatação de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="947d2-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="947d2-135">Deve ser o valor do **atributo ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="947d2-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="947d2-136">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="947d2-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="947d2-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="947d2-137">LineStyle</span></span>  <br/> |<span data-ttu-id="947d2-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="947d2-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="947d2-139">opcional</span><span class="sxs-lookup"><span data-stu-id="947d2-139">optional</span></span>  <br/> |<span data-ttu-id="947d2-140">Especifica a ID da folha de estilos da qual será herdada a formatação de linha.</span><span class="sxs-lookup"><span data-stu-id="947d2-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="947d2-141">Deve ser o valor do **atributo ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="947d2-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="947d2-142">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="947d2-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="947d2-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="947d2-143">TextStyle</span></span>  <br/> |<span data-ttu-id="947d2-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="947d2-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="947d2-145">opcional</span><span class="sxs-lookup"><span data-stu-id="947d2-145">optional</span></span>  <br/> |<span data-ttu-id="947d2-146">Especifica a ID da folha de estilos da qual será herdada a formatação de texto.</span><span class="sxs-lookup"><span data-stu-id="947d2-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="947d2-147">Deve ser o valor do **atributo ID** associado a um **StyleSheet_Type** no desenho.</span><span class="sxs-lookup"><span data-stu-id="947d2-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="947d2-148">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="947d2-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="947d2-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="947d2-149">UniqueID</span></span>  <br/> |<span data-ttu-id="947d2-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="947d2-150">xsd:string</span></span>  <br/> |<span data-ttu-id="947d2-151">opcional</span><span class="sxs-lookup"><span data-stu-id="947d2-151">optional</span></span>  <br/> |<span data-ttu-id="947d2-152">A ID exclusiva do elemento dentro de seu elemento pai.</span><span class="sxs-lookup"><span data-stu-id="947d2-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="947d2-153">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="947d2-153">Values of the xsd:string type.</span></span>  <br/> |
   

