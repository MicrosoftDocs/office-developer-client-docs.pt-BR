---
title: DataRecordSet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 36d6cf3b34ad0aa81f7b097d6452c46679342a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360354"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="e9234-102">DataRecordSet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e9234-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e9234-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="e9234-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9234-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e9234-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e9234-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e9234-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e9234-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e9234-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e9234-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="e9234-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e9234-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e9234-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e9234-109">Definição</span><span class="sxs-lookup"><span data-stu-id="e9234-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e9234-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="e9234-110">Elements and attributes</span></span>

<span data-ttu-id="e9234-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="e9234-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e9234-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e9234-112">Child elements</span></span>

|<span data-ttu-id="e9234-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e9234-113">**Element**</span></span>|<span data-ttu-id="e9234-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e9234-114">**Type**</span></span>|<span data-ttu-id="e9234-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e9234-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e9234-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="e9234-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9234-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="e9234-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e9234-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="e9234-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9234-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="e9234-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e9234-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e9234-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9234-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="e9234-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e9234-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="e9234-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9234-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="e9234-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e9234-124">Rel</span><span class="sxs-lookup"><span data-stu-id="e9234-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9234-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="e9234-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e9234-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="e9234-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9234-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="e9234-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e9234-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="e9234-128">Attributes</span></span>

|<span data-ttu-id="e9234-129">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e9234-129">**Attribute**</span></span>|<span data-ttu-id="e9234-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e9234-130">**Type**</span></span>|<span data-ttu-id="e9234-131">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="e9234-131">**Required**</span></span>|<span data-ttu-id="e9234-132">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e9234-132">**Description**</span></span>|<span data-ttu-id="e9234-133">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="e9234-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e9234-134">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="e9234-134">Checksum</span></span>  <br/> |<span data-ttu-id="e9234-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9234-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9234-136">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-136">optional</span></span>  <br/> ||<span data-ttu-id="e9234-137">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9234-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9234-138">Comando</span><span class="sxs-lookup"><span data-stu-id="e9234-138">Command</span></span>  <br/> |<span data-ttu-id="e9234-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9234-139">xsd:string</span></span>  <br/> |<span data-ttu-id="e9234-140">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-140">optional</span></span>  <br/> ||<span data-ttu-id="e9234-141">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e9234-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e9234-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="e9234-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="e9234-143">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9234-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9234-144">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-144">optional</span></span>  <br/> ||<span data-ttu-id="e9234-145">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9234-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9234-146">ID</span><span class="sxs-lookup"><span data-stu-id="e9234-146">ID</span></span>  <br/> |<span data-ttu-id="e9234-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9234-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9234-148">obrigatório</span><span class="sxs-lookup"><span data-stu-id="e9234-148">required</span></span>  <br/> ||<span data-ttu-id="e9234-149">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9234-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9234-150">Nome</span><span class="sxs-lookup"><span data-stu-id="e9234-150">Name</span></span>  <br/> |<span data-ttu-id="e9234-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9234-151">xsd:string</span></span>  <br/> |<span data-ttu-id="e9234-152">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-152">optional</span></span>  <br/> ||<span data-ttu-id="e9234-153">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e9234-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e9234-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="e9234-154">NextRowID</span></span>  <br/> |<span data-ttu-id="e9234-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9234-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9234-156">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-156">optional</span></span>  <br/> ||<span data-ttu-id="e9234-157">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9234-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9234-158">Opções</span><span class="sxs-lookup"><span data-stu-id="e9234-158">Options</span></span>  <br/> |<span data-ttu-id="e9234-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9234-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9234-160">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-160">optional</span></span>  <br/> ||<span data-ttu-id="e9234-161">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9234-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9234-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="e9234-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="e9234-163">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9234-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9234-164">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-164">optional</span></span>  <br/> ||<span data-ttu-id="e9234-165">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9234-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9234-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="e9234-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="e9234-167">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e9234-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e9234-168">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-168">optional</span></span>  <br/> ||<span data-ttu-id="e9234-169">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e9234-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e9234-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="e9234-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="e9234-171">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e9234-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e9234-172">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-172">optional</span></span>  <br/> ||<span data-ttu-id="e9234-173">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e9234-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e9234-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="e9234-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="e9234-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9234-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9234-176">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-176">optional</span></span>  <br/> ||<span data-ttu-id="e9234-177">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9234-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9234-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="e9234-178">RowOrder</span></span>  <br/> |<span data-ttu-id="e9234-179">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e9234-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e9234-180">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-180">optional</span></span>  <br/> ||<span data-ttu-id="e9234-181">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e9234-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e9234-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="e9234-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="e9234-183">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="e9234-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="e9234-184">opcional</span><span class="sxs-lookup"><span data-stu-id="e9234-184">optional</span></span>  <br/> ||<span data-ttu-id="e9234-185">Valores do tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="e9234-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

