---
title: Elemento SnapExtensions (Window_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Especifica se uma configuração de extensão de ajuste específica está habilitada ou desabilitada da janela ativa. O valor pode ser uma soma dos valores na tabela a seguir.
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540319"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a><span data-ttu-id="ac590-104">Elemento SnapExtensions (Window_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="ac590-104">SnapExtensions element (Window_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ac590-105">Especifica se uma configuração de extensão de ajuste específica está habilitada ou desabilitada da janela ativa.</span><span class="sxs-lookup"><span data-stu-id="ac590-105">Specifies whether a specific snap extension setting is enabled or disabled for the active window.</span></span> <span data-ttu-id="ac590-106">O valor pode ser uma soma dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac590-106">The value can be a sum of the values in the following table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac590-107">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="ac590-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac590-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ac590-108">**Element type**</span></span> <br/> |[<span data-ttu-id="ac590-109">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="ac590-109">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ac590-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ac590-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ac590-111">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ac590-111">**Schema file**</span></span> <br/> |<span data-ttu-id="ac590-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ac590-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ac590-113">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="ac590-113">**Document parts**</span></span> <br/> |<span data-ttu-id="ac590-114">windows.xml</span><span class="sxs-lookup"><span data-stu-id="ac590-114">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ac590-115">Definição</span><span class="sxs-lookup"><span data-stu-id="ac590-115">Definition</span></span>

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ac590-116">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ac590-116">Elements and attributes</span></span>

<span data-ttu-id="ac590-117">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ac590-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ac590-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ac590-118">Parent elements</span></span>

|<span data-ttu-id="ac590-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ac590-119">**Element**</span></span>|<span data-ttu-id="ac590-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ac590-120">**Type**</span></span>|<span data-ttu-id="ac590-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ac590-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac590-122">Janela</span><span class="sxs-lookup"><span data-stu-id="ac590-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ac590-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="ac590-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a><span data-ttu-id="ac590-124">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ac590-124">Child elements</span></span>

<span data-ttu-id="ac590-125">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ac590-125">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac590-126">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac590-126">Attributes</span></span>

<span data-ttu-id="ac590-127">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ac590-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ac590-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac590-128">Remarks</span></span>

<span data-ttu-id="ac590-129">O valor do **elemento SnapExtensions** pode ser uma soma dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac590-129">The value of the **SnapExtensions** element can be a sum of the values in the following table.</span></span> 
  
|<span data-ttu-id="ac590-130">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ac590-130">**Value**</span></span>|<span data-ttu-id="ac590-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ac590-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac590-132">0</span><span class="sxs-lookup"><span data-stu-id="ac590-132">0</span></span>  <br/> |<span data-ttu-id="ac590-133">Ajustar a nada.</span><span class="sxs-lookup"><span data-stu-id="ac590-133">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="ac590-134">1 </span><span class="sxs-lookup"><span data-stu-id="ac590-134">1</span></span>  <br/> |<span data-ttu-id="ac590-135">Ajustar à extensão da caixa de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="ac590-135">Snap to alignment box extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-136">2 </span><span class="sxs-lookup"><span data-stu-id="ac590-136">2</span></span>  <br/> |<span data-ttu-id="ac590-137">Ajustar à extensão do eixo central.</span><span class="sxs-lookup"><span data-stu-id="ac590-137">Snap to center axis extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-138">4 </span><span class="sxs-lookup"><span data-stu-id="ac590-138">4</span></span>  <br/> |<span data-ttu-id="ac590-139">Ajustar à extensão de tangente curva.</span><span class="sxs-lookup"><span data-stu-id="ac590-139">Snap to curve tangent extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-140">8 </span><span class="sxs-lookup"><span data-stu-id="ac590-140">8</span></span>  <br/> |<span data-ttu-id="ac590-141">Ajustar à extensão do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ac590-141">Snap to endpoint extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-142">16 </span><span class="sxs-lookup"><span data-stu-id="ac590-142">16</span></span>  <br/> |<span data-ttu-id="ac590-143">Ajustar à extensão do ponto médio.</span><span class="sxs-lookup"><span data-stu-id="ac590-143">Snap to midpoint extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-144">32</span><span class="sxs-lookup"><span data-stu-id="ac590-144">32</span></span>  <br/> |<span data-ttu-id="ac590-145">Ajustar à extensão linear.</span><span class="sxs-lookup"><span data-stu-id="ac590-145">Snap to linear extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-146">64</span><span class="sxs-lookup"><span data-stu-id="ac590-146">64</span></span>  <br/> |<span data-ttu-id="ac590-147">Ajustar à extensão de curva.</span><span class="sxs-lookup"><span data-stu-id="ac590-147">Snap to curve extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-148">128</span><span class="sxs-lookup"><span data-stu-id="ac590-148">128</span></span>  <br/> |<span data-ttu-id="ac590-149">Ajustar à extensão perpendicular do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ac590-149">Snap to endpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-150">256</span><span class="sxs-lookup"><span data-stu-id="ac590-150">256</span></span>  <br/> |<span data-ttu-id="ac590-151">Ajustar à extensão perpendicular do ponto médio.</span><span class="sxs-lookup"><span data-stu-id="ac590-151">Snap to midpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-152">512</span><span class="sxs-lookup"><span data-stu-id="ac590-152">512</span></span>  <br/> |<span data-ttu-id="ac590-153">Ajustar à extensão horizontal do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ac590-153">Snap to endpoint horizontal extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-154">1024</span><span class="sxs-lookup"><span data-stu-id="ac590-154">1024</span></span>  <br/> |<span data-ttu-id="ac590-155">Ajustar à extensão vertical do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ac590-155">Snap to endpoint vertical extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-156">2048</span><span class="sxs-lookup"><span data-stu-id="ac590-156">2048</span></span>  <br/> |<span data-ttu-id="ac590-157">Ajustar à extensão do centro de elipse.</span><span class="sxs-lookup"><span data-stu-id="ac590-157">Snap to ellipse center extension.</span></span>  <br/> |
|<span data-ttu-id="ac590-158">4096</span><span class="sxs-lookup"><span data-stu-id="ac590-158">4096</span></span>  <br/> |<span data-ttu-id="ac590-159">Ajustar à extensão de ângulos isométricos.</span><span class="sxs-lookup"><span data-stu-id="ac590-159">Snap to isometric angles extension.</span></span>  <br/> |
   

