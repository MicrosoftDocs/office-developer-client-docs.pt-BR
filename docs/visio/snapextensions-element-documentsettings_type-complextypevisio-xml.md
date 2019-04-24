---
title: Elemento SnapExtensions (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Especifica se uma configuração de extensão de ajuste específica está habilitada ou desabilitada da janela ativa.
ms.openlocfilehash: 9f21653fca7f1f5fa7be7449f1e588cf5ef67263
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334528"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="272bc-103">Elemento SnapExtensions (DocumentSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="272bc-103">SnapExtensions element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="272bc-104">Especifica se uma configuração de extensão de ajuste específica está habilitada ou desabilitada da janela ativa.</span><span class="sxs-lookup"><span data-stu-id="272bc-104">Specifies whether a specific snap extension setting is enabled or disabled for the active window.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="272bc-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="272bc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="272bc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="272bc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="272bc-107">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="272bc-107">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="272bc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="272bc-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="272bc-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="272bc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="272bc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="272bc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="272bc-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="272bc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="272bc-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="272bc-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="272bc-113">Definição</span><span class="sxs-lookup"><span data-stu-id="272bc-113">Definition</span></span>

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="272bc-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="272bc-114">Elements and attributes</span></span>

<span data-ttu-id="272bc-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="272bc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="272bc-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="272bc-116">Parent elements</span></span>

|<span data-ttu-id="272bc-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="272bc-117">**Element**</span></span>|<span data-ttu-id="272bc-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="272bc-118">**Type**</span></span>|<span data-ttu-id="272bc-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="272bc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="272bc-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="272bc-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="272bc-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="272bc-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="272bc-122">Contém elementos que especificam configurações de documentos.</span><span class="sxs-lookup"><span data-stu-id="272bc-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="272bc-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="272bc-123">Child elements</span></span>

<span data-ttu-id="272bc-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="272bc-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="272bc-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="272bc-125">Attributes</span></span>

<span data-ttu-id="272bc-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="272bc-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="272bc-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="272bc-127">Remarks</span></span>

<span data-ttu-id="272bc-128">O valor do elemento **SnapExtensions** pode ser uma soma dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="272bc-128">The value of the **SnapExtensions** element can be a sum of the values in the following table.</span></span> 
  
|<span data-ttu-id="272bc-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="272bc-129">**Value**</span></span>|<span data-ttu-id="272bc-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="272bc-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="272bc-131">,0</span><span class="sxs-lookup"><span data-stu-id="272bc-131">0</span></span>  <br/> |<span data-ttu-id="272bc-132">Ajustar a nada.</span><span class="sxs-lookup"><span data-stu-id="272bc-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="272bc-133">1</span><span class="sxs-lookup"><span data-stu-id="272bc-133">1</span></span>  <br/> |<span data-ttu-id="272bc-134">Ajustar à extensão da caixa de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="272bc-134">Snap to alignment box extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-135">duas</span><span class="sxs-lookup"><span data-stu-id="272bc-135">2</span></span>  <br/> |<span data-ttu-id="272bc-136">Ajustar à extensão do eixo central.</span><span class="sxs-lookup"><span data-stu-id="272bc-136">Snap to center axis extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-137">quatro</span><span class="sxs-lookup"><span data-stu-id="272bc-137">4</span></span>  <br/> |<span data-ttu-id="272bc-138">Ajustar à extensão da tangente da curva.</span><span class="sxs-lookup"><span data-stu-id="272bc-138">Snap to curve tangent extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-139">8</span><span class="sxs-lookup"><span data-stu-id="272bc-139">8</span></span>  <br/> |<span data-ttu-id="272bc-140">Ajustar à extensão do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="272bc-140">Snap to endpoint extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-141">dezesseis</span><span class="sxs-lookup"><span data-stu-id="272bc-141">16</span></span>  <br/> |<span data-ttu-id="272bc-142">Ajustar à extensão intermediária.</span><span class="sxs-lookup"><span data-stu-id="272bc-142">Snap to midpoint extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-143">32</span><span class="sxs-lookup"><span data-stu-id="272bc-143">32</span></span>  <br/> |<span data-ttu-id="272bc-144">Ajustar à extensão linear.</span><span class="sxs-lookup"><span data-stu-id="272bc-144">Snap to linear extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-145">64</span><span class="sxs-lookup"><span data-stu-id="272bc-145">64</span></span>  <br/> |<span data-ttu-id="272bc-146">Ajustar à extensão da curva.</span><span class="sxs-lookup"><span data-stu-id="272bc-146">Snap to curve extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-147">128</span><span class="sxs-lookup"><span data-stu-id="272bc-147">128</span></span>  <br/> |<span data-ttu-id="272bc-148">Ajustar à extensão perpendicular de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="272bc-148">Snap to endpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-149">256</span><span class="sxs-lookup"><span data-stu-id="272bc-149">256</span></span>  <br/> |<span data-ttu-id="272bc-150">Ajustar à extensão perpendicular de ponto central.</span><span class="sxs-lookup"><span data-stu-id="272bc-150">Snap to midpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-151">512</span><span class="sxs-lookup"><span data-stu-id="272bc-151">512</span></span>  <br/> |<span data-ttu-id="272bc-152">Ajustar à extensão horizontal do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="272bc-152">Snap to endpoint horizontal extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-153">1024</span><span class="sxs-lookup"><span data-stu-id="272bc-153">1024</span></span>  <br/> |<span data-ttu-id="272bc-154">Ajustar à extensão vertical do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="272bc-154">Snap to endpoint vertical extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-155">2048</span><span class="sxs-lookup"><span data-stu-id="272bc-155">2048</span></span>  <br/> |<span data-ttu-id="272bc-156">Ajustar à extensão do centro da elipse.</span><span class="sxs-lookup"><span data-stu-id="272bc-156">Snap to ellipse center extension.</span></span>  <br/> |
|<span data-ttu-id="272bc-157">4096</span><span class="sxs-lookup"><span data-stu-id="272bc-157">4096</span></span>  <br/> |<span data-ttu-id="272bc-158">Ajuste à extensão de ângulos isométrica.</span><span class="sxs-lookup"><span data-stu-id="272bc-158">Snap to isometric angles extension.</span></span>  <br/> |
   

