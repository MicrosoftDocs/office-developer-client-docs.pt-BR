---
title: Elemento RowKeyValue (PrimaryKey_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Especifica o valor de uma chave primária para uma linha individual de um Recordset.
ms.openlocfilehash: 12d60bb0ccccdcd8c1790678cae4ad1e887e73b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283500"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="2fd25-103">Elemento RowKeyValue (PrimaryKey_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2fd25-103">RowKeyValue element (PrimaryKey_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2fd25-104">Especifica o valor de uma chave primária para uma linha individual de um Recordset.</span><span class="sxs-lookup"><span data-stu-id="2fd25-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2fd25-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="2fd25-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fd25-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2fd25-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2fd25-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="2fd25-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2fd25-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2fd25-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2fd25-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2fd25-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2fd25-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2fd25-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2fd25-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="2fd25-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2fd25-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="2fd25-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2fd25-113">Definição</span><span class="sxs-lookup"><span data-stu-id="2fd25-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2fd25-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2fd25-114">Elements and attributes</span></span>

<span data-ttu-id="2fd25-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2fd25-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2fd25-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2fd25-116">Parent elements</span></span>

|<span data-ttu-id="2fd25-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2fd25-117">**Element**</span></span>|<span data-ttu-id="2fd25-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2fd25-118">**Type**</span></span>|<span data-ttu-id="2fd25-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2fd25-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2fd25-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="2fd25-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2fd25-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="2fd25-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2fd25-122">Especifica uma chave primária de um Recordset.</span><span class="sxs-lookup"><span data-stu-id="2fd25-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2fd25-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2fd25-123">Child elements</span></span>

<span data-ttu-id="2fd25-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2fd25-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2fd25-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="2fd25-125">Attributes</span></span>

|<span data-ttu-id="2fd25-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2fd25-126">**Attribute**</span></span>|<span data-ttu-id="2fd25-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2fd25-127">**Type**</span></span>|<span data-ttu-id="2fd25-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2fd25-128">**Required**</span></span>|<span data-ttu-id="2fd25-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2fd25-129">**Description**</span></span>|<span data-ttu-id="2fd25-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2fd25-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2fd25-131">RowID</span><span class="sxs-lookup"><span data-stu-id="2fd25-131">RowID</span></span>  <br/> |<span data-ttu-id="2fd25-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2fd25-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2fd25-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2fd25-133">required</span></span>  <br/> |<span data-ttu-id="2fd25-134">Um valor exclusivo que identifica uma linha de um Recordset.</span><span class="sxs-lookup"><span data-stu-id="2fd25-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="2fd25-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2fd25-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2fd25-136">Valor</span><span class="sxs-lookup"><span data-stu-id="2fd25-136">Value</span></span>  <br/> |<span data-ttu-id="2fd25-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2fd25-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2fd25-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2fd25-138">required</span></span>  <br/> |<span data-ttu-id="2fd25-139">O valor da chave primária dessa linha do Recordset.</span><span class="sxs-lookup"><span data-stu-id="2fd25-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="2fd25-140">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2fd25-140">Values of the xsd:string type.</span></span>  <br/> |
   

