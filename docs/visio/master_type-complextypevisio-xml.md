---
title: Master_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397706"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="ff6e0-102">Master_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ff6e0-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ff6e0-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="ff6e0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff6e0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ff6e0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ff6e0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ff6e0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ff6e0-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ff6e0-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ff6e0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff6e0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ff6e0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ff6e0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ff6e0-110">Elements and attributes</span></span>

<span data-ttu-id="ff6e0-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ff6e0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ff6e0-112">Child elements</span></span>

|<span data-ttu-id="ff6e0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-113">**Element**</span></span>|<span data-ttu-id="ff6e0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-114">**Type**</span></span>|<span data-ttu-id="ff6e0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ff6e0-116">Ícone</span><span class="sxs-lookup"><span data-stu-id="ff6e0-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff6e0-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="ff6e0-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ff6e0-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="ff6e0-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff6e0-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ff6e0-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ff6e0-120">Rel</span><span class="sxs-lookup"><span data-stu-id="ff6e0-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff6e0-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="ff6e0-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ff6e0-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="ff6e0-122">Attributes</span></span>

|<span data-ttu-id="ff6e0-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-123">**Attribute**</span></span>|<span data-ttu-id="ff6e0-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-124">**Type**</span></span>|<span data-ttu-id="ff6e0-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-125">**Required**</span></span>|<span data-ttu-id="ff6e0-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-126">**Description**</span></span>|<span data-ttu-id="ff6e0-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ff6e0-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff6e0-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="ff6e0-128">AlignName</span></span>  <br/> |<span data-ttu-id="ff6e0-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ff6e0-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ff6e0-130">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-130">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="ff6e0-132">BaseID</span></span>  <br/> |<span data-ttu-id="ff6e0-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ff6e0-133">xsd:string</span></span>  <br/> |<span data-ttu-id="ff6e0-134">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-134">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-136">Oculto</span><span class="sxs-lookup"><span data-stu-id="ff6e0-136">Hidden</span></span>  <br/> |<span data-ttu-id="ff6e0-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="ff6e0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff6e0-138">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-138">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-139">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="ff6e0-140">IconSize</span></span>  <br/> |<span data-ttu-id="ff6e0-141">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ff6e0-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ff6e0-142">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-142">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-143">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="ff6e0-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="ff6e0-145">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="ff6e0-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff6e0-146">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-146">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-147">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-148">ID</span><span class="sxs-lookup"><span data-stu-id="ff6e0-148">ID</span></span>  <br/> |<span data-ttu-id="ff6e0-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff6e0-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff6e0-150">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ff6e0-150">required</span></span>  <br/> ||<span data-ttu-id="ff6e0-151">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="ff6e0-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="ff6e0-153">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="ff6e0-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff6e0-154">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-154">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-155">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="ff6e0-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="ff6e0-157">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="ff6e0-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff6e0-158">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-158">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-159">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="ff6e0-160">MasterType</span></span>  <br/> |<span data-ttu-id="ff6e0-161">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ff6e0-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ff6e0-162">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-162">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-163">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="ff6e0-164">MatchByName</span></span>  <br/> |<span data-ttu-id="ff6e0-165">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="ff6e0-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff6e0-166">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-166">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-167">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-168">Nome</span><span class="sxs-lookup"><span data-stu-id="ff6e0-168">Name</span></span>  <br/> |<span data-ttu-id="ff6e0-169">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ff6e0-169">xsd:string</span></span>  <br/> |<span data-ttu-id="ff6e0-170">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-170">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-171">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-172">NameU</span><span class="sxs-lookup"><span data-stu-id="ff6e0-172">NameU</span></span>  <br/> |<span data-ttu-id="ff6e0-173">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ff6e0-173">xsd:string</span></span>  <br/> |<span data-ttu-id="ff6e0-174">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-174">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-175">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="ff6e0-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="ff6e0-177">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ff6e0-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ff6e0-178">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-178">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-179">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="ff6e0-180">Prompt</span></span>  <br/> |<span data-ttu-id="ff6e0-181">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ff6e0-181">xsd:string</span></span>  <br/> |<span data-ttu-id="ff6e0-182">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-182">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-183">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff6e0-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="ff6e0-184">UniqueID</span></span>  <br/> |<span data-ttu-id="ff6e0-185">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ff6e0-185">xsd:string</span></span>  <br/> |<span data-ttu-id="ff6e0-186">opcional</span><span class="sxs-lookup"><span data-stu-id="ff6e0-186">optional</span></span>  <br/> ||<span data-ttu-id="ff6e0-187">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff6e0-187">Values of the xsd:string type.</span></span>  <br/> |
   

