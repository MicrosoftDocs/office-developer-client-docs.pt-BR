---
title: MasterShortcut_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: df1e10ff11470cd87fc16efbaba6ad968df6d1b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772328"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="bdb8c-102">MasterShortcut_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="bdb8c-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bdb8c-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="bdb8c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdb8c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bdb8c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bdb8c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bdb8c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bdb8c-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bdb8c-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bdb8c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bdb8c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="bdb8c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bdb8c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="bdb8c-110">Elements and attributes</span></span>

<span data-ttu-id="bdb8c-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bdb8c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bdb8c-112">Child elements</span></span>

|<span data-ttu-id="bdb8c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-113">**Element**</span></span>|<span data-ttu-id="bdb8c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-114">**Type**</span></span>|<span data-ttu-id="bdb8c-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bdb8c-116">Ícone</span><span class="sxs-lookup"><span data-stu-id="bdb8c-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bdb8c-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="bdb8c-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bdb8c-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="bdb8c-118">Attributes</span></span>

|<span data-ttu-id="bdb8c-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-119">**Attribute**</span></span>|<span data-ttu-id="bdb8c-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-120">**Type**</span></span>|<span data-ttu-id="bdb8c-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-121">**Required**</span></span>|<span data-ttu-id="bdb8c-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-122">**Description**</span></span>|<span data-ttu-id="bdb8c-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="bdb8c-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bdb8c-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="bdb8c-124">AlignName</span></span>  <br/> |<span data-ttu-id="bdb8c-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bdb8c-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bdb8c-126">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-126">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-127">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="bdb8c-128">IconSize</span></span>  <br/> |<span data-ttu-id="bdb8c-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bdb8c-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bdb8c-130">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-130">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-132">ID</span><span class="sxs-lookup"><span data-stu-id="bdb8c-132">ID</span></span>  <br/> |<span data-ttu-id="bdb8c-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bdb8c-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bdb8c-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bdb8c-134">required</span></span>  <br/> ||<span data-ttu-id="bdb8c-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="bdb8c-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="bdb8c-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="bdb8c-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bdb8c-138">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-138">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="bdb8c-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="bdb8c-141">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="bdb8c-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bdb8c-142">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-142">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-143">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="bdb8c-144">MasterType</span></span>  <br/> |<span data-ttu-id="bdb8c-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bdb8c-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bdb8c-146">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-146">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-147">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-148">Nome</span><span class="sxs-lookup"><span data-stu-id="bdb8c-148">Name</span></span>  <br/> |<span data-ttu-id="bdb8c-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bdb8c-149">xsd:string</span></span>  <br/> |<span data-ttu-id="bdb8c-150">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-150">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-151">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-152">NameU</span><span class="sxs-lookup"><span data-stu-id="bdb8c-152">NameU</span></span>  <br/> |<span data-ttu-id="bdb8c-153">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bdb8c-153">xsd:string</span></span>  <br/> |<span data-ttu-id="bdb8c-154">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-154">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-155">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="bdb8c-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="bdb8c-157">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bdb8c-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bdb8c-158">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-158">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-159">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="bdb8c-160">Prompt</span></span>  <br/> |<span data-ttu-id="bdb8c-161">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bdb8c-161">xsd:string</span></span>  <br/> |<span data-ttu-id="bdb8c-162">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-162">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-163">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="bdb8c-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="bdb8c-165">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bdb8c-165">xsd:string</span></span>  <br/> |<span data-ttu-id="bdb8c-166">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-166">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-167">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdb8c-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="bdb8c-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="bdb8c-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="bdb8c-169">xsd:string</span></span>  <br/> |<span data-ttu-id="bdb8c-170">opcional</span><span class="sxs-lookup"><span data-stu-id="bdb8c-170">optional</span></span>  <br/> ||<span data-ttu-id="bdb8c-171">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-171">Values of the xsd:string type.</span></span>  <br/> |
   

