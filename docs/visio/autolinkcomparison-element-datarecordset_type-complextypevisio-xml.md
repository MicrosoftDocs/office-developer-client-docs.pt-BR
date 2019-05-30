---
title: Elemento AutoLinkComparison (DataRecordSet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Define uma regra que compara uma coluna pai do elemento DataRecordset com um item de dados de forma na última ação de vinculação automática bem-sucedida, executadas na interface do usuário.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537868"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="5d28c-103">Elemento AutoLinkComparison (DataRecordSet_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="5d28c-103">AutoLinkComparison element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5d28c-104">Define uma regra que compara uma coluna pai do elemento **ConjuntoDeRegistrosDeDados** com um item de dados de forma na última ação de vinculação automática bem-sucedida, executadas na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5d28c-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5d28c-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="5d28c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d28c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5d28c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5d28c-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="5d28c-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5d28c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5d28c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5d28c-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5d28c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5d28c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5d28c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5d28c-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="5d28c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5d28c-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="5d28c-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5d28c-113">Definição</span><span class="sxs-lookup"><span data-stu-id="5d28c-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5d28c-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5d28c-114">Elements and attributes</span></span>

<span data-ttu-id="5d28c-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5d28c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5d28c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5d28c-116">Parent elements</span></span>

|<span data-ttu-id="5d28c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d28c-117">**Element**</span></span>|<span data-ttu-id="5d28c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5d28c-118">**Type**</span></span>|<span data-ttu-id="5d28c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5d28c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5d28c-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="5d28c-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5d28c-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="5d28c-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5d28c-122">Especifica um conjunto de registros e a vinculação de dados entre esse conjunto e as formas em páginas de desenho.</span><span class="sxs-lookup"><span data-stu-id="5d28c-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5d28c-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5d28c-123">Child elements</span></span>

<span data-ttu-id="5d28c-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5d28c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d28c-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d28c-125">Attributes</span></span>

|<span data-ttu-id="5d28c-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5d28c-126">**Attribute**</span></span>|<span data-ttu-id="5d28c-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5d28c-127">**Type**</span></span>|<span data-ttu-id="5d28c-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="5d28c-128">**Required**</span></span>|<span data-ttu-id="5d28c-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5d28c-129">**Description**</span></span>|<span data-ttu-id="5d28c-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="5d28c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5d28c-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="5d28c-131">ColumnName</span></span>  <br/> |<span data-ttu-id="5d28c-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5d28c-132">xsd:string</span></span>  <br/> |<span data-ttu-id="5d28c-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5d28c-133">required</span></span>  <br/> |<span data-ttu-id="5d28c-134">Corresponde a um nome de coluna do conjunto de registros ADO.</span><span class="sxs-lookup"><span data-stu-id="5d28c-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="5d28c-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5d28c-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5d28c-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="5d28c-136">ContextType</span></span>  <br/> |<span data-ttu-id="5d28c-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5d28c-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5d28c-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="5d28c-138">required</span></span>  <br/> |<span data-ttu-id="5d28c-139">Especifica as propriedades do grupo ou da forma a serem usadas para a comparação.</span><span class="sxs-lookup"><span data-stu-id="5d28c-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="5d28c-140">Os valores possíveis são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d28c-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="5d28c-141">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5d28c-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5d28c-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="5d28c-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="5d28c-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5d28c-143">xsd:string</span></span>  <br/> |<span data-ttu-id="5d28c-144">opcional</span><span class="sxs-lookup"><span data-stu-id="5d28c-144">optional</span></span>  <br/> |<span data-ttu-id="5d28c-145">Se o valor de ContextType for 2 ou 3, esse atributo será obrigatório para definir uma comparação.</span><span class="sxs-lookup"><span data-stu-id="5d28c-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="5d28c-146">Se ContextType = 2, ContextTypeLabel deverá ser o rótulo do item de dados da forma. Se **ContextType** = 3, ContextTypeLabel deverá ser o nome da linha local.</span><span class="sxs-lookup"><span data-stu-id="5d28c-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="5d28c-147">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5d28c-147">Values of the xsd:string type.</span></span>  <br/> |
   

