---
title: Elemento SnapSettings (Window_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Especifica os objetos que as formas ajustadas ajustar quando está ativo na janela.
ms.openlocfilehash: b4793c6d9c13a922db4d3ed9504a3a08e933230a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385204"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="91527-103">Elemento SnapSettings (Window_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="91527-103">SnapSettings element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="91527-104">Especifica os objetos que as formas ajustadas ajustar quando está ativo na janela.</span><span class="sxs-lookup"><span data-stu-id="91527-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91527-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="91527-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91527-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="91527-106">**Element type**</span></span> <br/> |[<span data-ttu-id="91527-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="91527-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="91527-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="91527-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="91527-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="91527-109">**Schema file**</span></span> <br/> |<span data-ttu-id="91527-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="91527-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="91527-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="91527-111">**Document parts**</span></span> <br/> |<span data-ttu-id="91527-112">Windows.XML</span><span class="sxs-lookup"><span data-stu-id="91527-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91527-113">Definição</span><span class="sxs-lookup"><span data-stu-id="91527-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="91527-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="91527-114">Elements and attributes</span></span>

<span data-ttu-id="91527-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="91527-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="91527-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="91527-116">Parent elements</span></span>

|<span data-ttu-id="91527-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="91527-117">**Element**</span></span>|<span data-ttu-id="91527-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="91527-118">**Type**</span></span>|<span data-ttu-id="91527-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="91527-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91527-120">Window</span><span class="sxs-lookup"><span data-stu-id="91527-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="91527-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="91527-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="91527-122">Representa uma janela aberta em uma estância do Microsoft Visio.
</span><span class="sxs-lookup"><span data-stu-id="91527-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="91527-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="91527-123">Child elements</span></span>

<span data-ttu-id="91527-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="91527-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91527-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="91527-125">Attributes</span></span>

<span data-ttu-id="91527-126">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="91527-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91527-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="91527-127">Remarks</span></span>

<span data-ttu-id="91527-128">O valor pode ser uma soma dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="91527-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="91527-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="91527-129">**Value**</span></span>|<span data-ttu-id="91527-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="91527-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="91527-131">0</span><span class="sxs-lookup"><span data-stu-id="91527-131">0</span></span>  <br/> |<span data-ttu-id="91527-132">Ajustar a nada.</span><span class="sxs-lookup"><span data-stu-id="91527-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="91527-133">1</span><span class="sxs-lookup"><span data-stu-id="91527-133">1</span></span>  <br/> |<span data-ttu-id="91527-134">Ajustar às subdivisões da régua.</span><span class="sxs-lookup"><span data-stu-id="91527-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="91527-135">2</span><span class="sxs-lookup"><span data-stu-id="91527-135">2</span></span>  <br/> |<span data-ttu-id="91527-136">Ajustar à grade.</span><span class="sxs-lookup"><span data-stu-id="91527-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="91527-137">4</span><span class="sxs-lookup"><span data-stu-id="91527-137">4</span></span>  <br/> |<span data-ttu-id="91527-138">Ajustar às guias.</span><span class="sxs-lookup"><span data-stu-id="91527-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="91527-139">8</span><span class="sxs-lookup"><span data-stu-id="91527-139">8</span></span>  <br/> |<span data-ttu-id="91527-140">Ajustar às alças de seleção.</span><span class="sxs-lookup"><span data-stu-id="91527-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="91527-141">16</span><span class="sxs-lookup"><span data-stu-id="91527-141">16</span></span>  <br/> |<span data-ttu-id="91527-142">Ajustar aos vértices.</span><span class="sxs-lookup"><span data-stu-id="91527-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="91527-143">32</span><span class="sxs-lookup"><span data-stu-id="91527-143">32</span></span>  <br/> |<span data-ttu-id="91527-144">Ajustar aos pontos de conexão.</span><span class="sxs-lookup"><span data-stu-id="91527-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="91527-145">256</span><span class="sxs-lookup"><span data-stu-id="91527-145">256</span></span>  <br/> |<span data-ttu-id="91527-146">Ajustar às bordas visíveis das formas.</span><span class="sxs-lookup"><span data-stu-id="91527-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="91527-147">512</span><span class="sxs-lookup"><span data-stu-id="91527-147">512</span></span>  <br/> |<span data-ttu-id="91527-148">Ajustar à caixa de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="91527-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="91527-149">1024</span><span class="sxs-lookup"><span data-stu-id="91527-149">1024</span></span>  <br/> |<span data-ttu-id="91527-150">Ajustar às opções de extensões da forma.</span><span class="sxs-lookup"><span data-stu-id="91527-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="91527-151">32768</span><span class="sxs-lookup"><span data-stu-id="91527-151">32768</span></span>  <br/> |<span data-ttu-id="91527-152">Snap desabilitada.</span><span class="sxs-lookup"><span data-stu-id="91527-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="91527-153">65536</span><span class="sxs-lookup"><span data-stu-id="91527-153">65536</span></span>  <br/> |<span data-ttu-id="91527-154">Ajustar às intersecções.</span><span class="sxs-lookup"><span data-stu-id="91527-154">Snap to intersections.</span></span>  <br/> |
   

