---
title: MasterShortcut_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: ed8dd8ef985c814e41017526144bd7ec8cb63424
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538057"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="9c59b-102">MasterShortcut_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="9c59b-102">MasterShortcut_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9c59b-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="9c59b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c59b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9c59b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9c59b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9c59b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9c59b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9c59b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9c59b-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="9c59b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9c59b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9c59b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c59b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="9c59b-109">Definition</span></span>

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9c59b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9c59b-110">Elements and attributes</span></span>

<span data-ttu-id="9c59b-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9c59b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9c59b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9c59b-112">Child elements</span></span>

|<span data-ttu-id="9c59b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9c59b-113">**Element**</span></span>|<span data-ttu-id="9c59b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9c59b-114">**Type**</span></span>|<span data-ttu-id="9c59b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9c59b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c59b-116">Ícone</span><span class="sxs-lookup"><span data-stu-id="9c59b-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c59b-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="9c59b-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9c59b-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="9c59b-118">Attributes</span></span>

|<span data-ttu-id="9c59b-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9c59b-119">**Attribute**</span></span>|<span data-ttu-id="9c59b-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9c59b-120">**Type**</span></span>|<span data-ttu-id="9c59b-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9c59b-121">**Required**</span></span>|<span data-ttu-id="9c59b-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9c59b-122">**Description**</span></span>|<span data-ttu-id="9c59b-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9c59b-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9c59b-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="9c59b-124">AlignName</span></span>  <br/> |<span data-ttu-id="9c59b-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9c59b-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9c59b-126">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-126">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-127">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9c59b-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="9c59b-128">IconSize</span></span>  <br/> |<span data-ttu-id="9c59b-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9c59b-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9c59b-130">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-130">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9c59b-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-132">ID</span><span class="sxs-lookup"><span data-stu-id="9c59b-132">ID</span></span>  <br/> |<span data-ttu-id="9c59b-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c59b-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c59b-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9c59b-134">required</span></span>  <br/> ||<span data-ttu-id="9c59b-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9c59b-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="9c59b-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="9c59b-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9c59b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9c59b-138">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-138">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9c59b-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="9c59b-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="9c59b-141">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9c59b-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9c59b-142">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-142">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-143">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9c59b-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="9c59b-144">MasterType</span></span>  <br/> |<span data-ttu-id="9c59b-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9c59b-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9c59b-146">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-146">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-147">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9c59b-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-148">Nome</span><span class="sxs-lookup"><span data-stu-id="9c59b-148">Name</span></span>  <br/> |<span data-ttu-id="9c59b-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9c59b-149">xsd:string</span></span>  <br/> |<span data-ttu-id="9c59b-150">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-150">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-151">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9c59b-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-152">NameU</span><span class="sxs-lookup"><span data-stu-id="9c59b-152">NameU</span></span>  <br/> |<span data-ttu-id="9c59b-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9c59b-153">xsd:string</span></span>  <br/> |<span data-ttu-id="9c59b-154">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-154">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9c59b-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="9c59b-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="9c59b-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9c59b-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9c59b-158">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-158">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-159">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9c59b-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="9c59b-160">Prompt</span></span>  <br/> |<span data-ttu-id="9c59b-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9c59b-161">xsd:string</span></span>  <br/> |<span data-ttu-id="9c59b-162">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-162">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-163">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9c59b-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="9c59b-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="9c59b-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9c59b-165">xsd:string</span></span>  <br/> |<span data-ttu-id="9c59b-166">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-166">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-167">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9c59b-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9c59b-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="9c59b-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="9c59b-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9c59b-169">xsd:string</span></span>  <br/> |<span data-ttu-id="9c59b-170">opcional</span><span class="sxs-lookup"><span data-stu-id="9c59b-170">optional</span></span>  <br/> ||<span data-ttu-id="9c59b-171">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9c59b-171">Values of the xsd:string type.</span></span>  <br/> |
   

