---
title: MasterShortcut_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396481"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="d84ce-102">MasterShortcut_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d84ce-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d84ce-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="d84ce-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d84ce-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d84ce-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d84ce-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d84ce-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d84ce-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d84ce-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d84ce-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="d84ce-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d84ce-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d84ce-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d84ce-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d84ce-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d84ce-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d84ce-110">Elements and attributes</span></span>

<span data-ttu-id="d84ce-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d84ce-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d84ce-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d84ce-112">Child elements</span></span>

|<span data-ttu-id="d84ce-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d84ce-113">**Element**</span></span>|<span data-ttu-id="d84ce-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d84ce-114">**Type**</span></span>|<span data-ttu-id="d84ce-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d84ce-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d84ce-116">Ícone</span><span class="sxs-lookup"><span data-stu-id="d84ce-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d84ce-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="d84ce-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d84ce-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d84ce-118">Attributes</span></span>

|<span data-ttu-id="d84ce-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d84ce-119">**Attribute**</span></span>|<span data-ttu-id="d84ce-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d84ce-120">**Type**</span></span>|<span data-ttu-id="d84ce-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d84ce-121">**Required**</span></span>|<span data-ttu-id="d84ce-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d84ce-122">**Description**</span></span>|<span data-ttu-id="d84ce-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d84ce-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d84ce-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="d84ce-124">AlignName</span></span>  <br/> |<span data-ttu-id="d84ce-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d84ce-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d84ce-126">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-126">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-127">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d84ce-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="d84ce-128">IconSize</span></span>  <br/> |<span data-ttu-id="d84ce-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d84ce-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d84ce-130">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-130">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d84ce-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-132">ID</span><span class="sxs-lookup"><span data-stu-id="d84ce-132">ID</span></span>  <br/> |<span data-ttu-id="d84ce-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d84ce-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d84ce-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="d84ce-134">required</span></span>  <br/> ||<span data-ttu-id="d84ce-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d84ce-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="d84ce-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="d84ce-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d84ce-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d84ce-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-138">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d84ce-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="d84ce-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="d84ce-141">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d84ce-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d84ce-142">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-142">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-143">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d84ce-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="d84ce-144">MasterType</span></span>  <br/> |<span data-ttu-id="d84ce-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d84ce-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d84ce-146">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-146">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-147">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d84ce-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-148">Nome</span><span class="sxs-lookup"><span data-stu-id="d84ce-148">Name</span></span>  <br/> |<span data-ttu-id="d84ce-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d84ce-149">xsd:string</span></span>  <br/> |<span data-ttu-id="d84ce-150">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-150">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-151">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d84ce-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-152">NameU</span><span class="sxs-lookup"><span data-stu-id="d84ce-152">NameU</span></span>  <br/> |<span data-ttu-id="d84ce-153">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d84ce-153">xsd:string</span></span>  <br/> |<span data-ttu-id="d84ce-154">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-154">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-155">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d84ce-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="d84ce-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="d84ce-157">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d84ce-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d84ce-158">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-158">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-159">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d84ce-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="d84ce-160">Prompt</span></span>  <br/> |<span data-ttu-id="d84ce-161">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d84ce-161">xsd:string</span></span>  <br/> |<span data-ttu-id="d84ce-162">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-162">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-163">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d84ce-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="d84ce-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="d84ce-165">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d84ce-165">xsd:string</span></span>  <br/> |<span data-ttu-id="d84ce-166">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-166">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-167">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d84ce-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d84ce-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="d84ce-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="d84ce-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d84ce-169">xsd:string</span></span>  <br/> |<span data-ttu-id="d84ce-170">opcional</span><span class="sxs-lookup"><span data-stu-id="d84ce-170">optional</span></span>  <br/> ||<span data-ttu-id="d84ce-171">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d84ce-171">Values of the xsd:string type.</span></span>  <br/> |
   

