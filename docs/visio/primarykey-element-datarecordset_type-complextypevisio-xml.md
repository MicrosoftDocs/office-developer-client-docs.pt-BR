---
title: Elemento PrimaryKey (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifica um ou mais colunas de chave primária no conjunto de registros de dados.
ms.openlocfilehash: c001c343c33e65c3990744b885f1c345575b1ab3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396355"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="9561b-103">Elemento PrimaryKey (DataRecordSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9561b-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9561b-104">Identifica um ou mais colunas de chave primária no conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="9561b-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9561b-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="9561b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9561b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9561b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9561b-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="9561b-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9561b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9561b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9561b-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9561b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9561b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9561b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9561b-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="9561b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9561b-112">Recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="9561b-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9561b-113">Definição</span><span class="sxs-lookup"><span data-stu-id="9561b-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9561b-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9561b-114">Elements and attributes</span></span>

<span data-ttu-id="9561b-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9561b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9561b-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9561b-116">Parent elements</span></span>

|<span data-ttu-id="9561b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9561b-117">**Element**</span></span>|<span data-ttu-id="9561b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9561b-118">**Type**</span></span>|<span data-ttu-id="9561b-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9561b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9561b-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="9561b-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9561b-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="9561b-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9561b-122">Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="9561b-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9561b-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9561b-123">Child elements</span></span>

|<span data-ttu-id="9561b-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9561b-124">**Element**</span></span>|<span data-ttu-id="9561b-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9561b-125">**Type**</span></span>|<span data-ttu-id="9561b-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9561b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9561b-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="9561b-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9561b-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="9561b-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9561b-129">Especifica o valor deste componente da chave primária para uma linha individual de um recordset.</span><span class="sxs-lookup"><span data-stu-id="9561b-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="9561b-130">DEVE haver pelo menos uma ocorrência deste elemento filho.</span><span class="sxs-lookup"><span data-stu-id="9561b-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9561b-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="9561b-131">Attributes</span></span>

|<span data-ttu-id="9561b-132">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9561b-132">**Attribute**</span></span>|<span data-ttu-id="9561b-133">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9561b-133">**Type**</span></span>|<span data-ttu-id="9561b-134">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9561b-134">**Required**</span></span>|<span data-ttu-id="9561b-135">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9561b-135">**Description**</span></span>|<span data-ttu-id="9561b-136">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9561b-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9561b-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="9561b-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="9561b-138">XSD: String</span><span class="sxs-lookup"><span data-stu-id="9561b-138">xsd:string</span></span>  <br/> |<span data-ttu-id="9561b-139">opcional</span><span class="sxs-lookup"><span data-stu-id="9561b-139">optional</span></span>  <br/> |<span data-ttu-id="9561b-140">Especifica o nome de um campo que é um componente da chave primária.</span><span class="sxs-lookup"><span data-stu-id="9561b-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="9561b-141">Ela deve ser o valor do atributo **ColumnNameID** de um elemento de descendente DataColumn_Type do DataRecordSet_Type cuja chave primária que está sendo especificado.</span><span class="sxs-lookup"><span data-stu-id="9561b-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="9561b-142">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9561b-142">Values of the xsd:string type.</span></span>  <br/> |
   

