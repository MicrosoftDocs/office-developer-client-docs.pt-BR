---
title: Elemento DataColumns (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contém todos os elementos de DataColumn em um conjunto de registros de dados.
ms.openlocfilehash: a7a0a8faefdb965384e435ee3a9b059a3acbc3f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382516"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="4a863-103">Elemento DataColumns (DataRecordSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4a863-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4a863-104">Contém todos os elementos de **DataColumn** em um conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="4a863-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4a863-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="4a863-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a863-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4a863-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4a863-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="4a863-107">DataColumns_Type complexType</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4a863-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4a863-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4a863-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4a863-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4a863-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4a863-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4a863-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="4a863-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4a863-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="4a863-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a863-113">Definição</span><span class="sxs-lookup"><span data-stu-id="4a863-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4a863-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4a863-114">Elements and attributes</span></span>

<span data-ttu-id="4a863-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4a863-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4a863-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="4a863-116">Parent elements</span></span>

|<span data-ttu-id="4a863-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a863-117">**Element**</span></span>|<span data-ttu-id="4a863-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4a863-118">**Type**</span></span>|<span data-ttu-id="4a863-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a863-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a863-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="4a863-120">DataRecordSet element</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a863-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="4a863-121">DataRecordSet_Type complexType</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a863-122">Armazena, formata, atualiza e expõe dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="4a863-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4a863-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4a863-123">Child elements</span></span>

|<span data-ttu-id="4a863-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a863-124">**Element**</span></span>|<span data-ttu-id="4a863-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4a863-125">**Type**</span></span>|<span data-ttu-id="4a863-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a863-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a863-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="4a863-127">DataColumn element</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a863-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="4a863-128">DataColumn_Type complexType</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a863-129">Define a aparência de uma coluna de dados na janela **Dados Externos** na interface de usuário do Visio e qualifica os dados na coluna definindo o tipo de dados e formatação.</span><span class="sxs-lookup"><span data-stu-id="4a863-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4a863-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="4a863-130">Attributes</span></span>

|<span data-ttu-id="4a863-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4a863-131">**Attribute**</span></span>|<span data-ttu-id="4a863-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4a863-132">**Type**</span></span>|<span data-ttu-id="4a863-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4a863-133">**Required**</span></span>|<span data-ttu-id="4a863-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a863-134">**Description**</span></span>|<span data-ttu-id="4a863-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4a863-135">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4a863-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="4a863-136">SortAsc</span></span>  <br/> |<span data-ttu-id="4a863-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4a863-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4a863-138">opcional</span><span class="sxs-lookup"><span data-stu-id="4a863-138">optional</span></span>  <br/> |<span data-ttu-id="4a863-139">A coluna na qual classificar os dados.</span><span class="sxs-lookup"><span data-stu-id="4a863-139">The second field on which to sort the mail merge data.</span></span>  <br/> |<span data-ttu-id="4a863-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4a863-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4a863-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="4a863-141">SortColumn</span></span>  <br/> |<span data-ttu-id="4a863-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4a863-142">xsd:string</span></span>  <br/> |<span data-ttu-id="4a863-143">opcional</span><span class="sxs-lookup"><span data-stu-id="4a863-143">optional</span></span>  <br/> |<span data-ttu-id="4a863-144">Especifica se a coluna **SortColumn** será classificada em ordem decrescente (0) ou crescente (1).</span><span class="sxs-lookup"><span data-stu-id="4a863-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="4a863-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4a863-145">Values of the xsd:string type.</span></span>  <br/> |
   

