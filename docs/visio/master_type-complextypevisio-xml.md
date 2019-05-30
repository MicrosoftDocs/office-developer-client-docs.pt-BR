---
title: Master_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 22b619149fc5393f085ca6e245c65ed6058538ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538064"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="8f449-102">Master_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="8f449-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8f449-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="8f449-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f449-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8f449-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8f449-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8f449-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8f449-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8f449-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8f449-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="8f449-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8f449-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8f449-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8f449-109">Definição</span><span class="sxs-lookup"><span data-stu-id="8f449-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8f449-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8f449-110">Elements and attributes</span></span>

<span data-ttu-id="8f449-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8f449-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8f449-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8f449-112">Child elements</span></span>

|<span data-ttu-id="8f449-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8f449-113">**Element**</span></span>|<span data-ttu-id="8f449-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8f449-114">**Type**</span></span>|<span data-ttu-id="8f449-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8f449-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f449-116">Ícone</span><span class="sxs-lookup"><span data-stu-id="8f449-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f449-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="8f449-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8f449-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="8f449-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f449-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="8f449-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8f449-120">Rel</span><span class="sxs-lookup"><span data-stu-id="8f449-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f449-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="8f449-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8f449-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f449-122">Attributes</span></span>

|<span data-ttu-id="8f449-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8f449-123">**Attribute**</span></span>|<span data-ttu-id="8f449-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8f449-124">**Type**</span></span>|<span data-ttu-id="8f449-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8f449-125">**Required**</span></span>|<span data-ttu-id="8f449-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8f449-126">**Description**</span></span>|<span data-ttu-id="8f449-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8f449-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8f449-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="8f449-128">AlignName</span></span>  <br/> |<span data-ttu-id="8f449-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8f449-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8f449-130">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-130">optional</span></span>  <br/> ||<span data-ttu-id="8f449-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8f449-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8f449-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="8f449-132">BaseID</span></span>  <br/> |<span data-ttu-id="8f449-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8f449-133">xsd:string</span></span>  <br/> |<span data-ttu-id="8f449-134">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-134">optional</span></span>  <br/> ||<span data-ttu-id="8f449-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8f449-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8f449-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="8f449-136">Hidden</span></span>  <br/> |<span data-ttu-id="8f449-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8f449-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8f449-138">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-138">optional</span></span>  <br/> ||<span data-ttu-id="8f449-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8f449-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8f449-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="8f449-140">IconSize</span></span>  <br/> |<span data-ttu-id="8f449-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8f449-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8f449-142">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-142">optional</span></span>  <br/> ||<span data-ttu-id="8f449-143">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8f449-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8f449-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="8f449-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="8f449-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8f449-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8f449-146">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-146">optional</span></span>  <br/> ||<span data-ttu-id="8f449-147">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8f449-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8f449-148">ID</span><span class="sxs-lookup"><span data-stu-id="8f449-148">ID</span></span>  <br/> |<span data-ttu-id="8f449-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8f449-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8f449-150">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8f449-150">required</span></span>  <br/> ||<span data-ttu-id="8f449-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8f449-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8f449-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="8f449-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="8f449-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8f449-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8f449-154">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-154">optional</span></span>  <br/> ||<span data-ttu-id="8f449-155">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8f449-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8f449-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="8f449-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="8f449-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8f449-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8f449-158">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-158">optional</span></span>  <br/> ||<span data-ttu-id="8f449-159">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8f449-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8f449-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="8f449-160">MasterType</span></span>  <br/> |<span data-ttu-id="8f449-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8f449-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8f449-162">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-162">optional</span></span>  <br/> ||<span data-ttu-id="8f449-163">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8f449-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8f449-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="8f449-164">MatchByName</span></span>  <br/> |<span data-ttu-id="8f449-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8f449-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8f449-166">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-166">optional</span></span>  <br/> ||<span data-ttu-id="8f449-167">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8f449-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8f449-168">Nome</span><span class="sxs-lookup"><span data-stu-id="8f449-168">Name</span></span>  <br/> |<span data-ttu-id="8f449-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8f449-169">xsd:string</span></span>  <br/> |<span data-ttu-id="8f449-170">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-170">optional</span></span>  <br/> ||<span data-ttu-id="8f449-171">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8f449-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8f449-172">NameU</span><span class="sxs-lookup"><span data-stu-id="8f449-172">NameU</span></span>  <br/> |<span data-ttu-id="8f449-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8f449-173">xsd:string</span></span>  <br/> |<span data-ttu-id="8f449-174">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-174">optional</span></span>  <br/> ||<span data-ttu-id="8f449-175">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8f449-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8f449-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="8f449-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="8f449-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8f449-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8f449-178">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-178">optional</span></span>  <br/> ||<span data-ttu-id="8f449-179">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8f449-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8f449-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="8f449-180">Prompt</span></span>  <br/> |<span data-ttu-id="8f449-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8f449-181">xsd:string</span></span>  <br/> |<span data-ttu-id="8f449-182">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-182">optional</span></span>  <br/> ||<span data-ttu-id="8f449-183">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8f449-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8f449-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="8f449-184">UniqueID</span></span>  <br/> |<span data-ttu-id="8f449-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8f449-185">xsd:string</span></span>  <br/> |<span data-ttu-id="8f449-186">opcional</span><span class="sxs-lookup"><span data-stu-id="8f449-186">optional</span></span>  <br/> ||<span data-ttu-id="8f449-187">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8f449-187">Values of the xsd:string type.</span></span>  <br/> |
   

