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
# <a name="master_type-complextype-visio-xml"></a><span data-ttu-id="f5483-102">Master_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="f5483-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f5483-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f5483-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5483-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f5483-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f5483-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f5483-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f5483-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f5483-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f5483-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f5483-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f5483-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f5483-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f5483-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f5483-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f5483-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f5483-110">Elements and attributes</span></span>

<span data-ttu-id="f5483-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f5483-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f5483-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f5483-112">Child elements</span></span>

|<span data-ttu-id="f5483-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f5483-113">**Element**</span></span>|<span data-ttu-id="f5483-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f5483-114">**Type**</span></span>|<span data-ttu-id="f5483-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f5483-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f5483-116">Ícone</span><span class="sxs-lookup"><span data-stu-id="f5483-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5483-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="f5483-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f5483-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="f5483-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5483-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f5483-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f5483-120">Rel</span><span class="sxs-lookup"><span data-stu-id="f5483-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5483-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f5483-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f5483-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="f5483-122">Attributes</span></span>

|<span data-ttu-id="f5483-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f5483-123">**Attribute**</span></span>|<span data-ttu-id="f5483-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f5483-124">**Type**</span></span>|<span data-ttu-id="f5483-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f5483-125">**Required**</span></span>|<span data-ttu-id="f5483-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f5483-126">**Description**</span></span>|<span data-ttu-id="f5483-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f5483-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f5483-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="f5483-128">AlignName</span></span>  <br/> |<span data-ttu-id="f5483-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f5483-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f5483-130">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-130">optional</span></span>  <br/> ||<span data-ttu-id="f5483-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f5483-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f5483-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="f5483-132">BaseID</span></span>  <br/> |<span data-ttu-id="f5483-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f5483-133">xsd:string</span></span>  <br/> |<span data-ttu-id="f5483-134">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-134">optional</span></span>  <br/> ||<span data-ttu-id="f5483-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f5483-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5483-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="f5483-136">Hidden</span></span>  <br/> |<span data-ttu-id="f5483-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f5483-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5483-138">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-138">optional</span></span>  <br/> ||<span data-ttu-id="f5483-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f5483-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5483-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="f5483-140">IconSize</span></span>  <br/> |<span data-ttu-id="f5483-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f5483-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f5483-142">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-142">optional</span></span>  <br/> ||<span data-ttu-id="f5483-143">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f5483-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f5483-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="f5483-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="f5483-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f5483-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5483-146">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-146">optional</span></span>  <br/> ||<span data-ttu-id="f5483-147">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f5483-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5483-148">ID</span><span class="sxs-lookup"><span data-stu-id="f5483-148">ID</span></span>  <br/> |<span data-ttu-id="f5483-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f5483-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f5483-150">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f5483-150">required</span></span>  <br/> ||<span data-ttu-id="f5483-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f5483-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f5483-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="f5483-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="f5483-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f5483-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5483-154">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-154">optional</span></span>  <br/> ||<span data-ttu-id="f5483-155">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f5483-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5483-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="f5483-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="f5483-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f5483-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5483-158">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-158">optional</span></span>  <br/> ||<span data-ttu-id="f5483-159">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f5483-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5483-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="f5483-160">MasterType</span></span>  <br/> |<span data-ttu-id="f5483-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f5483-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f5483-162">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-162">optional</span></span>  <br/> ||<span data-ttu-id="f5483-163">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f5483-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f5483-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="f5483-164">MatchByName</span></span>  <br/> |<span data-ttu-id="f5483-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f5483-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5483-166">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-166">optional</span></span>  <br/> ||<span data-ttu-id="f5483-167">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f5483-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5483-168">Nome</span><span class="sxs-lookup"><span data-stu-id="f5483-168">Name</span></span>  <br/> |<span data-ttu-id="f5483-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f5483-169">xsd:string</span></span>  <br/> |<span data-ttu-id="f5483-170">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-170">optional</span></span>  <br/> ||<span data-ttu-id="f5483-171">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f5483-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5483-172">NameU</span><span class="sxs-lookup"><span data-stu-id="f5483-172">NameU</span></span>  <br/> |<span data-ttu-id="f5483-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f5483-173">xsd:string</span></span>  <br/> |<span data-ttu-id="f5483-174">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-174">optional</span></span>  <br/> ||<span data-ttu-id="f5483-175">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f5483-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5483-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="f5483-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="f5483-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f5483-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f5483-178">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-178">optional</span></span>  <br/> ||<span data-ttu-id="f5483-179">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f5483-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f5483-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="f5483-180">Prompt</span></span>  <br/> |<span data-ttu-id="f5483-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f5483-181">xsd:string</span></span>  <br/> |<span data-ttu-id="f5483-182">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-182">optional</span></span>  <br/> ||<span data-ttu-id="f5483-183">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f5483-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5483-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="f5483-184">UniqueID</span></span>  <br/> |<span data-ttu-id="f5483-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f5483-185">xsd:string</span></span>  <br/> |<span data-ttu-id="f5483-186">opcional</span><span class="sxs-lookup"><span data-stu-id="f5483-186">optional</span></span>  <br/> ||<span data-ttu-id="f5483-187">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f5483-187">Values of the xsd:string type.</span></span>  <br/> |
   

