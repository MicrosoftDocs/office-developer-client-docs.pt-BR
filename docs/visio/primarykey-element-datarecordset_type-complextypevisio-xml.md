---
title: Elemento PrimaryKey (DataRecordSet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifica uma ou mais colunas de chave primárias do conjunto de dados.
ms.openlocfilehash: bd77b1d18490695dc2b0cb43520f42bb845e91ab
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537707"
---
# <a name="primarykey-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="fe374-103">Elemento PrimaryKey (DataRecordSet_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="fe374-103">PrimaryKey element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fe374-104">Identifica uma ou mais colunas de chave primárias do conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="fe374-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe374-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="fe374-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe374-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fe374-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fe374-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="fe374-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fe374-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fe374-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fe374-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fe374-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fe374-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fe374-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fe374-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="fe374-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fe374-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="fe374-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fe374-113">Definição</span><span class="sxs-lookup"><span data-stu-id="fe374-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fe374-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fe374-114">Elements and attributes</span></span>

<span data-ttu-id="fe374-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fe374-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fe374-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fe374-116">Parent elements</span></span>

|<span data-ttu-id="fe374-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fe374-117">**Element**</span></span>|<span data-ttu-id="fe374-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fe374-118">**Type**</span></span>|<span data-ttu-id="fe374-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fe374-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fe374-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="fe374-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fe374-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="fe374-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fe374-122">Armazena, formata, atualiza e expõe dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="fe374-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fe374-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fe374-123">Child elements</span></span>

|<span data-ttu-id="fe374-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fe374-124">**Element**</span></span>|<span data-ttu-id="fe374-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fe374-125">**Type**</span></span>|<span data-ttu-id="fe374-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fe374-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fe374-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="fe374-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fe374-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="fe374-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fe374-129">Especifica o valor deste componente da chave primária para uma linha individual de um recordset.</span><span class="sxs-lookup"><span data-stu-id="fe374-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="fe374-130">DEVE haver pelo menos uma ocorrência desse elemento filho.</span><span class="sxs-lookup"><span data-stu-id="fe374-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fe374-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="fe374-131">Attributes</span></span>

|<span data-ttu-id="fe374-132">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fe374-132">**Attribute**</span></span>|<span data-ttu-id="fe374-133">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fe374-133">**Type**</span></span>|<span data-ttu-id="fe374-134">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="fe374-134">**Required**</span></span>|<span data-ttu-id="fe374-135">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fe374-135">**Description**</span></span>|<span data-ttu-id="fe374-136">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="fe374-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fe374-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="fe374-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="fe374-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fe374-138">xsd:string</span></span>  <br/> |<span data-ttu-id="fe374-139">opcional</span><span class="sxs-lookup"><span data-stu-id="fe374-139">optional</span></span>  <br/> |<span data-ttu-id="fe374-140">Especifica o nome de um campo que é um componente da chave primária.</span><span class="sxs-lookup"><span data-stu-id="fe374-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="fe374-141">Deve ser o valor do atributo **ColumnNameID** de um DataColumn_Type descendente do DataRecordSet_Type cuja chave primária está sendo especificada.</span><span class="sxs-lookup"><span data-stu-id="fe374-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="fe374-142">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fe374-142">Values of the xsd:string type.</span></span>  <br/> |
   

