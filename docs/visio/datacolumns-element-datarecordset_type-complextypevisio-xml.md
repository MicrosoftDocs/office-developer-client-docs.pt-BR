---
title: Elemento DataColumns (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contém todos os elementos de DataColumn em um conjunto de registros de dados.
ms.openlocfilehash: b90b6cb18fc2bd1edc393d58a9d761cfb36ea220
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771652"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="75da3-103">Elemento DataColumns (DataRecordSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="75da3-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="75da3-104">Contém todos os elementos de **DataColumn** em um conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="75da3-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="75da3-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="75da3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75da3-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="75da3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="75da3-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="75da3-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="75da3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="75da3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="75da3-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="75da3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="75da3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="75da3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="75da3-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="75da3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="75da3-112">Recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="75da3-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75da3-113">Definição</span><span class="sxs-lookup"><span data-stu-id="75da3-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="75da3-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="75da3-114">Elements and attributes</span></span>

<span data-ttu-id="75da3-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="75da3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="75da3-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="75da3-116">Parent elements</span></span>

|<span data-ttu-id="75da3-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="75da3-117">**Element**</span></span>|<span data-ttu-id="75da3-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="75da3-118">**Type**</span></span>|<span data-ttu-id="75da3-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="75da3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75da3-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="75da3-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75da3-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="75da3-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75da3-122">Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="75da3-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="75da3-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="75da3-123">Child elements</span></span>

|<span data-ttu-id="75da3-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="75da3-124">**Element**</span></span>|<span data-ttu-id="75da3-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="75da3-125">**Type**</span></span>|<span data-ttu-id="75da3-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="75da3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75da3-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="75da3-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75da3-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="75da3-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75da3-129">Define como uma coluna de dados aparece na janela **Dados externos** na interface do usuário do Visio e qualifica os dados na coluna definindo seu tipo de dados e formatação.</span><span class="sxs-lookup"><span data-stu-id="75da3-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="75da3-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="75da3-130">Attributes</span></span>

|<span data-ttu-id="75da3-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="75da3-131">**Attribute**</span></span>|<span data-ttu-id="75da3-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="75da3-132">**Type**</span></span>|<span data-ttu-id="75da3-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="75da3-133">**Required**</span></span>|<span data-ttu-id="75da3-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="75da3-134">**Description**</span></span>|<span data-ttu-id="75da3-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="75da3-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="75da3-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="75da3-136">SortAsc</span></span>  <br/> |<span data-ttu-id="75da3-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="75da3-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="75da3-138">opcional</span><span class="sxs-lookup"><span data-stu-id="75da3-138">optional</span></span>  <br/> |<span data-ttu-id="75da3-139">A coluna no qual você deseja classificar os dados.</span><span class="sxs-lookup"><span data-stu-id="75da3-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="75da3-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="75da3-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="75da3-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="75da3-141">SortColumn</span></span>  <br/> |<span data-ttu-id="75da3-142">XSD: String</span><span class="sxs-lookup"><span data-stu-id="75da3-142">xsd:string</span></span>  <br/> |<span data-ttu-id="75da3-143">opcional</span><span class="sxs-lookup"><span data-stu-id="75da3-143">optional</span></span>  <br/> |<span data-ttu-id="75da3-144">Se deseja classificar a coluna **SortColumn** em crescente (1) ou em ordem decrescente de (0).</span><span class="sxs-lookup"><span data-stu-id="75da3-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="75da3-145">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="75da3-145">Values of the xsd:string type.</span></span>  <br/> |
   

