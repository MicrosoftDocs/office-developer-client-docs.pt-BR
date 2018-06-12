---
title: Elemento AutoLinkComparison (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Define uma regra que compara uma coluna no elemento pai DataRecordset com um item de dados da forma da última bem-sucedida automática vinculação ação executada na interface do usuário.
ms.openlocfilehash: 38970a84676f769c36c9bdc3f8334652f7d9ec21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771292"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="c3b06-103">Elemento AutoLinkComparison (DataRecordSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c3b06-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c3b06-104">Define uma regra que compara uma coluna no elemento pai **DataRecordset** com um item de dados da forma da última bem-sucedida automática vinculação ação executada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c3b06-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c3b06-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="c3b06-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3b06-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c3b06-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c3b06-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="c3b06-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c3b06-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3b06-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c3b06-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c3b06-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c3b06-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c3b06-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c3b06-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="c3b06-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c3b06-112">Recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="c3b06-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3b06-113">Definição</span><span class="sxs-lookup"><span data-stu-id="c3b06-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c3b06-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c3b06-114">Elements and attributes</span></span>

<span data-ttu-id="c3b06-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c3b06-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c3b06-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c3b06-116">Parent elements</span></span>

|<span data-ttu-id="c3b06-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c3b06-117">**Element**</span></span>|<span data-ttu-id="c3b06-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c3b06-118">**Type**</span></span>|<span data-ttu-id="c3b06-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c3b06-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3b06-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3b06-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3b06-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="c3b06-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c3b06-122">Especifica um conjunto de registros e a vinculação de dados entre esse recordset e as formas em páginas de desenho.</span><span class="sxs-lookup"><span data-stu-id="c3b06-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c3b06-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c3b06-123">Child elements</span></span>

<span data-ttu-id="c3b06-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c3b06-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3b06-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3b06-125">Attributes</span></span>

|<span data-ttu-id="c3b06-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c3b06-126">**Attribute**</span></span>|<span data-ttu-id="c3b06-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c3b06-127">**Type**</span></span>|<span data-ttu-id="c3b06-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c3b06-128">**Required**</span></span>|<span data-ttu-id="c3b06-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c3b06-129">**Description**</span></span>|<span data-ttu-id="c3b06-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c3b06-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c3b06-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="c3b06-131">ColumnName</span></span>  <br/> |<span data-ttu-id="c3b06-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c3b06-132">xsd:string</span></span>  <br/> |<span data-ttu-id="c3b06-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c3b06-133">required</span></span>  <br/> |<span data-ttu-id="c3b06-134">Corresponde a um nome de coluna no conjunto de registros ADO.</span><span class="sxs-lookup"><span data-stu-id="c3b06-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="c3b06-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c3b06-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c3b06-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="c3b06-136">ContextType</span></span>  <br/> |<span data-ttu-id="c3b06-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3b06-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3b06-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c3b06-138">required</span></span>  <br/> |<span data-ttu-id="c3b06-139">Especifica as propriedades do grupo ou forma a ser usada para comparação.</span><span class="sxs-lookup"><span data-stu-id="c3b06-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="c3b06-140">Valores possíveis são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3b06-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="c3b06-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3b06-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3b06-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="c3b06-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="c3b06-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c3b06-143">xsd:string</span></span>  <br/> |<span data-ttu-id="c3b06-144">opcional</span><span class="sxs-lookup"><span data-stu-id="c3b06-144">optional</span></span>  <br/> |<span data-ttu-id="c3b06-145">Se o valor de ContextType for 2 ou 3, este atributo é necessário para definir uma comparação.</span><span class="sxs-lookup"><span data-stu-id="c3b06-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="c3b06-146">Para ContextType = 2, ContextTypeLabel deve ser o rótulo de item de dados de forma e se **ContextType** = 3, ContextTypeLabel deve ser o nome de linha local.</span><span class="sxs-lookup"><span data-stu-id="c3b06-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="c3b06-147">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c3b06-147">Values of the xsd:string type.</span></span>  <br/> |
   

