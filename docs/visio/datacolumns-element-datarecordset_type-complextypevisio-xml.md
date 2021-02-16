---
title: Elemento DataColumns (DataRecordSet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contém todos os elementos de DataColumn em um conjunto de registros de dados.
ms.openlocfilehash: e42354076c5e3e34c118145e7ec7fcdbd4977372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541194"
---
# <a name="datacolumns-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="54f00-103">Elemento DataColumns (DataRecordSet_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="54f00-103">DataColumns element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="54f00-104">Contém todos os elementos de **DataColumn** em um conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="54f00-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="54f00-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="54f00-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54f00-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="54f00-106">**Element type**</span></span> <br/> |[<span data-ttu-id="54f00-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="54f00-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="54f00-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="54f00-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="54f00-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="54f00-109">**Schema file**</span></span> <br/> |<span data-ttu-id="54f00-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="54f00-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="54f00-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="54f00-111">**Document parts**</span></span> <br/> |<span data-ttu-id="54f00-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="54f00-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54f00-113">Definição</span><span class="sxs-lookup"><span data-stu-id="54f00-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="54f00-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="54f00-114">Elements and attributes</span></span>

<span data-ttu-id="54f00-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="54f00-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="54f00-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="54f00-116">Parent elements</span></span>

|<span data-ttu-id="54f00-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="54f00-117">**Element**</span></span>|<span data-ttu-id="54f00-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="54f00-118">**Type**</span></span>|<span data-ttu-id="54f00-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="54f00-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54f00-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="54f00-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="54f00-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="54f00-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="54f00-122">Armazena, formata, atualiza e expõe dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="54f00-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="54f00-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="54f00-123">Child elements</span></span>

|<span data-ttu-id="54f00-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="54f00-124">**Element**</span></span>|<span data-ttu-id="54f00-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="54f00-125">**Type**</span></span>|<span data-ttu-id="54f00-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="54f00-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54f00-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="54f00-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="54f00-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="54f00-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="54f00-129">Define a aparência de uma coluna de dados na janela **Dados Externos** na interface de usuário do Visio e qualifica os dados na coluna definindo o tipo de dados e formatação.</span><span class="sxs-lookup"><span data-stu-id="54f00-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="54f00-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="54f00-130">Attributes</span></span>

|<span data-ttu-id="54f00-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="54f00-131">**Attribute**</span></span>|<span data-ttu-id="54f00-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="54f00-132">**Type**</span></span>|<span data-ttu-id="54f00-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="54f00-133">**Required**</span></span>|<span data-ttu-id="54f00-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="54f00-134">**Description**</span></span>|<span data-ttu-id="54f00-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="54f00-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="54f00-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="54f00-136">SortAsc</span></span>  <br/> |<span data-ttu-id="54f00-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="54f00-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="54f00-138">opcional</span><span class="sxs-lookup"><span data-stu-id="54f00-138">optional</span></span>  <br/> |<span data-ttu-id="54f00-139">A coluna na qual classificar os dados.</span><span class="sxs-lookup"><span data-stu-id="54f00-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="54f00-140">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="54f00-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="54f00-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="54f00-141">SortColumn</span></span>  <br/> |<span data-ttu-id="54f00-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="54f00-142">xsd:string</span></span>  <br/> |<span data-ttu-id="54f00-143">opcional</span><span class="sxs-lookup"><span data-stu-id="54f00-143">optional</span></span>  <br/> |<span data-ttu-id="54f00-144">Especifica se a coluna **SortColumn** será classificada em ordem decrescente (0) ou crescente (1).</span><span class="sxs-lookup"><span data-stu-id="54f00-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="54f00-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="54f00-145">Values of the xsd:string type.</span></span>  <br/> |
   

