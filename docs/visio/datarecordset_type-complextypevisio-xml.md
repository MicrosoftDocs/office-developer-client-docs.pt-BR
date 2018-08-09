---
title: DataRecordSet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 79fe048c578e8b9d8095d3fe7cd456af8ce08549
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771665"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="9ab73-102">DataRecordSet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9ab73-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9ab73-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="9ab73-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ab73-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9ab73-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9ab73-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9ab73-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9ab73-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9ab73-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9ab73-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="9ab73-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9ab73-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9ab73-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ab73-109">Definição</span><span class="sxs-lookup"><span data-stu-id="9ab73-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSet_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DataColumns"  type="DataColumns_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PrimaryKey"  type="PrimaryKey_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowMap"  type="RowMap_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshConflict"  type="RefreshConflict_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="AutoLinkComparison"  type="AutoLinkComparison_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ConnectionID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="Options"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TimeRefreshed"
  type="xsd:dateTime"
    />
    <xs:attribute name="NextRowID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="RowOrder"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshOverwriteAll"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshNoReconciliationUI"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshInterval"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReplaceLinks"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Checksum"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9ab73-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9ab73-110">Elements and attributes</span></span>

<span data-ttu-id="9ab73-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9ab73-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9ab73-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9ab73-112">Child elements</span></span>

|<span data-ttu-id="9ab73-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9ab73-113">**Element**</span></span>|<span data-ttu-id="9ab73-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9ab73-114">**Type**</span></span>|<span data-ttu-id="9ab73-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9ab73-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ab73-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="9ab73-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ab73-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="9ab73-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ab73-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="9ab73-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ab73-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="9ab73-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ab73-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9ab73-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ab73-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="9ab73-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ab73-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="9ab73-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ab73-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="9ab73-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ab73-124">Rel</span><span class="sxs-lookup"><span data-stu-id="9ab73-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ab73-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="9ab73-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9ab73-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="9ab73-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ab73-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="9ab73-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9ab73-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="9ab73-128">Attributes</span></span>

|<span data-ttu-id="9ab73-129">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9ab73-129">**Attribute**</span></span>|<span data-ttu-id="9ab73-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9ab73-130">**Type**</span></span>|<span data-ttu-id="9ab73-131">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9ab73-131">**Required**</span></span>|<span data-ttu-id="9ab73-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9ab73-132">**Description**</span></span>|<span data-ttu-id="9ab73-133">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9ab73-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9ab73-134">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="9ab73-134">Checksum</span></span>  <br/> |<span data-ttu-id="9ab73-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ab73-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ab73-136">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-136">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ab73-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-138">Command</span><span class="sxs-lookup"><span data-stu-id="9ab73-138">Command</span></span>  <br/> |<span data-ttu-id="9ab73-139">XSD: String</span><span class="sxs-lookup"><span data-stu-id="9ab73-139">xsd:string</span></span>  <br/> |<span data-ttu-id="9ab73-140">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-140">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-141">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9ab73-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-142">Conexão</span><span class="sxs-lookup"><span data-stu-id="9ab73-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="9ab73-143">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ab73-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ab73-144">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-144">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-145">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ab73-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-146">ID</span><span class="sxs-lookup"><span data-stu-id="9ab73-146">ID</span></span>  <br/> |<span data-ttu-id="9ab73-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ab73-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ab73-148">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9ab73-148">required</span></span>  <br/> ||<span data-ttu-id="9ab73-149">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ab73-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-150">Nome</span><span class="sxs-lookup"><span data-stu-id="9ab73-150">Name</span></span>  <br/> |<span data-ttu-id="9ab73-151">XSD: String</span><span class="sxs-lookup"><span data-stu-id="9ab73-151">xsd:string</span></span>  <br/> |<span data-ttu-id="9ab73-152">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-152">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-153">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9ab73-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="9ab73-154">NextRowID</span></span>  <br/> |<span data-ttu-id="9ab73-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ab73-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ab73-156">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-156">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-157">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ab73-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-158">Options</span><span class="sxs-lookup"><span data-stu-id="9ab73-158">Options</span></span>  <br/> |<span data-ttu-id="9ab73-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ab73-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ab73-160">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-160">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-161">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ab73-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="9ab73-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="9ab73-163">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ab73-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ab73-164">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-164">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-165">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ab73-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="9ab73-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="9ab73-167">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="9ab73-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ab73-168">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-168">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-169">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9ab73-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="9ab73-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="9ab73-171">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="9ab73-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ab73-172">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-172">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-173">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9ab73-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="9ab73-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="9ab73-175">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ab73-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ab73-176">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-176">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-177">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ab73-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="9ab73-178">RowOrder</span></span>  <br/> |<span data-ttu-id="9ab73-179">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="9ab73-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ab73-180">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-180">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-181">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9ab73-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9ab73-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="9ab73-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="9ab73-183">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="9ab73-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="9ab73-184">opcional</span><span class="sxs-lookup"><span data-stu-id="9ab73-184">optional</span></span>  <br/> ||<span data-ttu-id="9ab73-185">Valores do tipo xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="9ab73-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

