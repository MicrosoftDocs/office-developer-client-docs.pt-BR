---
title: Elemento PrimaryKey (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifica um ou mais colunas de chave primária no conjunto de registros de dados.
ms.openlocfilehash: f720636bbdf2c55baca6d98aa7d0761607e53ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772611"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="3ecf7-103">Elemento PrimaryKey (DataRecordSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="3ecf7-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3ecf7-104">Identifica um ou mais colunas de chave primária no conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ecf7-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="3ecf7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ecf7-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3ecf7-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="3ecf7-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3ecf7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3ecf7-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3ecf7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3ecf7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3ecf7-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3ecf7-112">Recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="3ecf7-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ecf7-113">Definição</span><span class="sxs-lookup"><span data-stu-id="3ecf7-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3ecf7-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3ecf7-114">Elements and attributes</span></span>

<span data-ttu-id="3ecf7-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3ecf7-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3ecf7-116">Parent elements</span></span>

|<span data-ttu-id="3ecf7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-117">**Element**</span></span>|<span data-ttu-id="3ecf7-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-118">**Type**</span></span>|<span data-ttu-id="3ecf7-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ecf7-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="3ecf7-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3ecf7-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="3ecf7-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ecf7-122">Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3ecf7-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3ecf7-123">Child elements</span></span>

|<span data-ttu-id="3ecf7-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-124">**Element**</span></span>|<span data-ttu-id="3ecf7-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-125">**Type**</span></span>|<span data-ttu-id="3ecf7-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ecf7-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="3ecf7-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3ecf7-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="3ecf7-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ecf7-129">Especifica o valor deste componente da chave primária para uma linha individual de um recordset.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="3ecf7-130">DEVE haver pelo menos uma ocorrência deste elemento filho.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3ecf7-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ecf7-131">Attributes</span></span>

|<span data-ttu-id="3ecf7-132">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-132">**Attribute**</span></span>|<span data-ttu-id="3ecf7-133">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-133">**Type**</span></span>|<span data-ttu-id="3ecf7-134">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-134">**Required**</span></span>|<span data-ttu-id="3ecf7-135">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-135">**Description**</span></span>|<span data-ttu-id="3ecf7-136">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3ecf7-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3ecf7-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="3ecf7-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="3ecf7-138">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3ecf7-138">xsd:string</span></span>  <br/> |<span data-ttu-id="3ecf7-139">opcional</span><span class="sxs-lookup"><span data-stu-id="3ecf7-139">optional</span></span>  <br/> |<span data-ttu-id="3ecf7-140">Especifica o nome de um campo que é um componente da chave primária.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="3ecf7-141">Ela deve ser o valor do atributo **ColumnNameID** de um elemento de descendente DataColumn_Type do DataRecordSet_Type cuja chave primária que está sendo especificado.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="3ecf7-142">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-142">Values of the xsd:string type.</span></span>  <br/> |
   

