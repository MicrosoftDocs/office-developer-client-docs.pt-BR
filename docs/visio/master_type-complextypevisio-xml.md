---
title: Master_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: b4dde4d00552525a5ec17116f96151f39c6d0957
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772312"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="6deb4-102">Master_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="6deb4-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6deb4-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="6deb4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6deb4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6deb4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6deb4-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6deb4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6deb4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6deb4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6deb4-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="6deb4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6deb4-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6deb4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6deb4-109">Definição</span><span class="sxs-lookup"><span data-stu-id="6deb4-109">Definition</span></span>

```XML
          <xs:complexType name="Master_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
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
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
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
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6deb4-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6deb4-110">Elements and attributes</span></span>

<span data-ttu-id="6deb4-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6deb4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6deb4-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6deb4-112">Child elements</span></span>

|<span data-ttu-id="6deb4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6deb4-113">**Element**</span></span>|<span data-ttu-id="6deb4-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6deb4-114">**Type**</span></span>|<span data-ttu-id="6deb4-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6deb4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6deb4-116">Ícone</span><span class="sxs-lookup"><span data-stu-id="6deb4-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6deb4-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="6deb4-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6deb4-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="6deb4-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6deb4-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6deb4-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6deb4-120">Rel</span><span class="sxs-lookup"><span data-stu-id="6deb4-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6deb4-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="6deb4-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6deb4-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="6deb4-122">Attributes</span></span>

|<span data-ttu-id="6deb4-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6deb4-123">**Attribute**</span></span>|<span data-ttu-id="6deb4-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6deb4-124">**Type**</span></span>|<span data-ttu-id="6deb4-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="6deb4-125">**Required**</span></span>|<span data-ttu-id="6deb4-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6deb4-126">**Description**</span></span>|<span data-ttu-id="6deb4-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="6deb4-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6deb4-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="6deb4-128">AlignName</span></span>  <br/> |<span data-ttu-id="6deb4-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6deb4-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6deb4-130">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-130">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6deb4-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="6deb4-132">BaseID</span></span>  <br/> |<span data-ttu-id="6deb4-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6deb4-133">xsd:string</span></span>  <br/> |<span data-ttu-id="6deb4-134">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-134">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6deb4-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-136">Oculto</span><span class="sxs-lookup"><span data-stu-id="6deb4-136">Hidden</span></span>  <br/> |<span data-ttu-id="6deb4-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="6deb4-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6deb4-138">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-138">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6deb4-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="6deb4-140">IconSize</span></span>  <br/> |<span data-ttu-id="6deb4-141">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6deb4-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6deb4-142">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-142">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-143">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6deb4-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="6deb4-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="6deb4-145">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="6deb4-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6deb4-146">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-146">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-147">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6deb4-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-148">ID</span><span class="sxs-lookup"><span data-stu-id="6deb4-148">ID</span></span>  <br/> |<span data-ttu-id="6deb4-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6deb4-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6deb4-150">obrigatório</span><span class="sxs-lookup"><span data-stu-id="6deb4-150">required</span></span>  <br/> ||<span data-ttu-id="6deb4-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6deb4-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="6deb4-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="6deb4-153">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="6deb4-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6deb4-154">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-154">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-155">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6deb4-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="6deb4-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="6deb4-157">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="6deb4-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6deb4-158">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-158">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-159">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6deb4-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="6deb4-160">MasterType</span></span>  <br/> |<span data-ttu-id="6deb4-161">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6deb4-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6deb4-162">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-162">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-163">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6deb4-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="6deb4-164">MatchByName</span></span>  <br/> |<span data-ttu-id="6deb4-165">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="6deb4-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6deb4-166">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-166">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-167">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6deb4-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-168">Nome</span><span class="sxs-lookup"><span data-stu-id="6deb4-168">Name</span></span>  <br/> |<span data-ttu-id="6deb4-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6deb4-169">xsd:string</span></span>  <br/> |<span data-ttu-id="6deb4-170">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-170">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-171">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6deb4-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-172">NameU</span><span class="sxs-lookup"><span data-stu-id="6deb4-172">NameU</span></span>  <br/> |<span data-ttu-id="6deb4-173">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6deb4-173">xsd:string</span></span>  <br/> |<span data-ttu-id="6deb4-174">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-174">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-175">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6deb4-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="6deb4-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="6deb4-177">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6deb4-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6deb4-178">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-178">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-179">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6deb4-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="6deb4-180">Prompt</span></span>  <br/> |<span data-ttu-id="6deb4-181">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6deb4-181">xsd:string</span></span>  <br/> |<span data-ttu-id="6deb4-182">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-182">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-183">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6deb4-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6deb4-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="6deb4-184">UniqueID</span></span>  <br/> |<span data-ttu-id="6deb4-185">XSD: String</span><span class="sxs-lookup"><span data-stu-id="6deb4-185">xsd:string</span></span>  <br/> |<span data-ttu-id="6deb4-186">opcional</span><span class="sxs-lookup"><span data-stu-id="6deb4-186">optional</span></span>  <br/> ||<span data-ttu-id="6deb4-187">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6deb4-187">Values of the xsd:string type.</span></span>  <br/> |
   

