---
title: Elemento RowKeyValue (PrimaryKey_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Especifica o valor de uma chave primária para uma linha individual de um Recordset.
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538127"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="771b7-103">Elemento RowKeyValue (PrimaryKey_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="771b7-103">RowKeyValue element (PrimaryKey_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="771b7-104">Especifica o valor de uma chave primária para uma linha individual de um Recordset.</span><span class="sxs-lookup"><span data-stu-id="771b7-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="771b7-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="771b7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="771b7-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="771b7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="771b7-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="771b7-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="771b7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="771b7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="771b7-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="771b7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="771b7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="771b7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="771b7-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="771b7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="771b7-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="771b7-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="771b7-113">Definição</span><span class="sxs-lookup"><span data-stu-id="771b7-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="771b7-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="771b7-114">Elements and attributes</span></span>

<span data-ttu-id="771b7-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="771b7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="771b7-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="771b7-116">Parent elements</span></span>

|<span data-ttu-id="771b7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="771b7-117">**Element**</span></span>|<span data-ttu-id="771b7-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="771b7-118">**Type**</span></span>|<span data-ttu-id="771b7-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="771b7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="771b7-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="771b7-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="771b7-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="771b7-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="771b7-122">Especifica uma chave primária de um Recordset.</span><span class="sxs-lookup"><span data-stu-id="771b7-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="771b7-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="771b7-123">Child elements</span></span>

<span data-ttu-id="771b7-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="771b7-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="771b7-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="771b7-125">Attributes</span></span>

|<span data-ttu-id="771b7-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="771b7-126">**Attribute**</span></span>|<span data-ttu-id="771b7-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="771b7-127">**Type**</span></span>|<span data-ttu-id="771b7-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="771b7-128">**Required**</span></span>|<span data-ttu-id="771b7-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="771b7-129">**Description**</span></span>|<span data-ttu-id="771b7-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="771b7-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="771b7-131">RowID</span><span class="sxs-lookup"><span data-stu-id="771b7-131">RowID</span></span>  <br/> |<span data-ttu-id="771b7-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="771b7-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="771b7-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="771b7-133">required</span></span>  <br/> |<span data-ttu-id="771b7-134">Um valor exclusivo que identifica uma linha de um Recordset.</span><span class="sxs-lookup"><span data-stu-id="771b7-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="771b7-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="771b7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="771b7-136">Valor</span><span class="sxs-lookup"><span data-stu-id="771b7-136">Value</span></span>  <br/> |<span data-ttu-id="771b7-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="771b7-137">xsd:string</span></span>  <br/> |<span data-ttu-id="771b7-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="771b7-138">required</span></span>  <br/> |<span data-ttu-id="771b7-139">O valor da chave primária dessa linha do Recordset.</span><span class="sxs-lookup"><span data-stu-id="771b7-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="771b7-140">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="771b7-140">Values of the xsd:string type.</span></span>  <br/> |
   

