---
title: Master_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341801"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="2abae-102">Master_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2abae-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2abae-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="2abae-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2abae-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2abae-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2abae-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2abae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2abae-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2abae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2abae-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="2abae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2abae-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2abae-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2abae-109">Definição</span><span class="sxs-lookup"><span data-stu-id="2abae-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2abae-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2abae-110">Elements and attributes</span></span>

<span data-ttu-id="2abae-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2abae-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2abae-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2abae-112">Child elements</span></span>

|<span data-ttu-id="2abae-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2abae-113">**Element**</span></span>|<span data-ttu-id="2abae-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2abae-114">**Type**</span></span>|<span data-ttu-id="2abae-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2abae-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2abae-116">Ícone</span><span class="sxs-lookup"><span data-stu-id="2abae-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2abae-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="2abae-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2abae-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="2abae-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2abae-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="2abae-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2abae-120">Rel</span><span class="sxs-lookup"><span data-stu-id="2abae-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2abae-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="2abae-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2abae-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="2abae-122">Attributes</span></span>

|<span data-ttu-id="2abae-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2abae-123">**Attribute**</span></span>|<span data-ttu-id="2abae-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2abae-124">**Type**</span></span>|<span data-ttu-id="2abae-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2abae-125">**Required**</span></span>|<span data-ttu-id="2abae-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2abae-126">**Description**</span></span>|<span data-ttu-id="2abae-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2abae-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2abae-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="2abae-128">AlignName</span></span>  <br/> |<span data-ttu-id="2abae-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2abae-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2abae-130">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-130">optional</span></span>  <br/> ||<span data-ttu-id="2abae-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2abae-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2abae-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="2abae-132">BaseID</span></span>  <br/> |<span data-ttu-id="2abae-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2abae-133">xsd:string</span></span>  <br/> |<span data-ttu-id="2abae-134">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-134">optional</span></span>  <br/> ||<span data-ttu-id="2abae-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2abae-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2abae-136">Oculto</span><span class="sxs-lookup"><span data-stu-id="2abae-136">Hidden</span></span>  <br/> |<span data-ttu-id="2abae-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2abae-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2abae-138">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-138">optional</span></span>  <br/> ||<span data-ttu-id="2abae-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2abae-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2abae-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="2abae-140">IconSize</span></span>  <br/> |<span data-ttu-id="2abae-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2abae-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2abae-142">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-142">optional</span></span>  <br/> ||<span data-ttu-id="2abae-143">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2abae-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2abae-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="2abae-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="2abae-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2abae-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2abae-146">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-146">optional</span></span>  <br/> ||<span data-ttu-id="2abae-147">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2abae-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2abae-148">ID</span><span class="sxs-lookup"><span data-stu-id="2abae-148">ID</span></span>  <br/> |<span data-ttu-id="2abae-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2abae-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2abae-150">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2abae-150">required</span></span>  <br/> ||<span data-ttu-id="2abae-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2abae-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2abae-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="2abae-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="2abae-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2abae-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2abae-154">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-154">optional</span></span>  <br/> ||<span data-ttu-id="2abae-155">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2abae-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2abae-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="2abae-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="2abae-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2abae-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2abae-158">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-158">optional</span></span>  <br/> ||<span data-ttu-id="2abae-159">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2abae-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2abae-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="2abae-160">MasterType</span></span>  <br/> |<span data-ttu-id="2abae-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2abae-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2abae-162">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-162">optional</span></span>  <br/> ||<span data-ttu-id="2abae-163">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2abae-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2abae-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="2abae-164">MatchByName</span></span>  <br/> |<span data-ttu-id="2abae-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2abae-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2abae-166">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-166">optional</span></span>  <br/> ||<span data-ttu-id="2abae-167">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2abae-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2abae-168">Name</span><span class="sxs-lookup"><span data-stu-id="2abae-168">Name</span></span>  <br/> |<span data-ttu-id="2abae-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2abae-169">xsd:string</span></span>  <br/> |<span data-ttu-id="2abae-170">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-170">optional</span></span>  <br/> ||<span data-ttu-id="2abae-171">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2abae-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2abae-172">NameU</span><span class="sxs-lookup"><span data-stu-id="2abae-172">NameU</span></span>  <br/> |<span data-ttu-id="2abae-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2abae-173">xsd:string</span></span>  <br/> |<span data-ttu-id="2abae-174">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-174">optional</span></span>  <br/> ||<span data-ttu-id="2abae-175">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2abae-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2abae-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="2abae-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="2abae-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2abae-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2abae-178">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-178">optional</span></span>  <br/> ||<span data-ttu-id="2abae-179">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2abae-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2abae-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="2abae-180">Prompt</span></span>  <br/> |<span data-ttu-id="2abae-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2abae-181">xsd:string</span></span>  <br/> |<span data-ttu-id="2abae-182">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-182">optional</span></span>  <br/> ||<span data-ttu-id="2abae-183">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2abae-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2abae-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="2abae-184">UniqueID</span></span>  <br/> |<span data-ttu-id="2abae-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2abae-185">xsd:string</span></span>  <br/> |<span data-ttu-id="2abae-186">opcional</span><span class="sxs-lookup"><span data-stu-id="2abae-186">optional</span></span>  <br/> ||<span data-ttu-id="2abae-187">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2abae-187">Values of the xsd:string type.</span></span>  <br/> |
   

