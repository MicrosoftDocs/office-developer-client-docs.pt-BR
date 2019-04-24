---
title: MasterShortcut_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341689"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="1cdde-102">MasterShortcut_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1cdde-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1cdde-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="1cdde-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cdde-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1cdde-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1cdde-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1cdde-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1cdde-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1cdde-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1cdde-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="1cdde-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1cdde-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1cdde-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1cdde-109">Definição</span><span class="sxs-lookup"><span data-stu-id="1cdde-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1cdde-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1cdde-110">Elements and attributes</span></span>

<span data-ttu-id="1cdde-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1cdde-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1cdde-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1cdde-112">Child elements</span></span>

|<span data-ttu-id="1cdde-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1cdde-113">**Element**</span></span>|<span data-ttu-id="1cdde-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1cdde-114">**Type**</span></span>|<span data-ttu-id="1cdde-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1cdde-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1cdde-116">Ícone</span><span class="sxs-lookup"><span data-stu-id="1cdde-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1cdde-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="1cdde-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1cdde-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1cdde-118">Attributes</span></span>

|<span data-ttu-id="1cdde-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1cdde-119">**Attribute**</span></span>|<span data-ttu-id="1cdde-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1cdde-120">**Type**</span></span>|<span data-ttu-id="1cdde-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="1cdde-121">**Required**</span></span>|<span data-ttu-id="1cdde-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1cdde-122">**Description**</span></span>|<span data-ttu-id="1cdde-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="1cdde-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1cdde-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="1cdde-124">AlignName</span></span>  <br/> |<span data-ttu-id="1cdde-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1cdde-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1cdde-126">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-126">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-127">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1cdde-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="1cdde-128">IconSize</span></span>  <br/> |<span data-ttu-id="1cdde-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1cdde-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1cdde-130">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-130">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1cdde-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-132">ID</span><span class="sxs-lookup"><span data-stu-id="1cdde-132">ID</span></span>  <br/> |<span data-ttu-id="1cdde-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1cdde-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1cdde-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="1cdde-134">required</span></span>  <br/> ||<span data-ttu-id="1cdde-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1cdde-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="1cdde-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="1cdde-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1cdde-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1cdde-138">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-138">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1cdde-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="1cdde-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="1cdde-141">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1cdde-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1cdde-142">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-142">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-143">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1cdde-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="1cdde-144">MasterType</span></span>  <br/> |<span data-ttu-id="1cdde-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1cdde-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1cdde-146">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-146">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-147">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1cdde-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-148">Name</span><span class="sxs-lookup"><span data-stu-id="1cdde-148">Name</span></span>  <br/> |<span data-ttu-id="1cdde-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cdde-149">xsd:string</span></span>  <br/> |<span data-ttu-id="1cdde-150">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-150">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-151">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cdde-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-152">NameU</span><span class="sxs-lookup"><span data-stu-id="1cdde-152">NameU</span></span>  <br/> |<span data-ttu-id="1cdde-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cdde-153">xsd:string</span></span>  <br/> |<span data-ttu-id="1cdde-154">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-154">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-155">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cdde-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="1cdde-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="1cdde-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1cdde-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1cdde-158">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-158">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-159">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1cdde-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="1cdde-160">Prompt</span></span>  <br/> |<span data-ttu-id="1cdde-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cdde-161">xsd:string</span></span>  <br/> |<span data-ttu-id="1cdde-162">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-162">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-163">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cdde-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="1cdde-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="1cdde-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cdde-165">xsd:string</span></span>  <br/> |<span data-ttu-id="1cdde-166">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-166">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-167">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cdde-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1cdde-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="1cdde-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="1cdde-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1cdde-169">xsd:string</span></span>  <br/> |<span data-ttu-id="1cdde-170">opcional</span><span class="sxs-lookup"><span data-stu-id="1cdde-170">optional</span></span>  <br/> ||<span data-ttu-id="1cdde-171">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1cdde-171">Values of the xsd:string type.</span></span>  <br/> |
   

