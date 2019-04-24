---
title: Elemento RowMap (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Mapas de uma linha de conjunto de registros de dados para uma forma.
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332512"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="341eb-103">Elemento RowMap (DataRecordSet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="341eb-103">RowMap element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="341eb-104">Mapas de uma linha de conjunto de registros de dados para uma forma.</span><span class="sxs-lookup"><span data-stu-id="341eb-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="341eb-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="341eb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="341eb-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="341eb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="341eb-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="341eb-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="341eb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="341eb-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="341eb-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="341eb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="341eb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="341eb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="341eb-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="341eb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="341eb-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="341eb-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="341eb-113">Definição</span><span class="sxs-lookup"><span data-stu-id="341eb-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="341eb-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="341eb-114">Elements and attributes</span></span>

<span data-ttu-id="341eb-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="341eb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="341eb-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="341eb-116">Parent elements</span></span>

****

|<span data-ttu-id="341eb-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="341eb-117">**Element**</span></span>|<span data-ttu-id="341eb-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="341eb-118">**Type**</span></span>|<span data-ttu-id="341eb-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="341eb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="341eb-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="341eb-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="341eb-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="341eb-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="341eb-122">Armazena, formata, atualiza e expõe dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="341eb-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="341eb-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="341eb-123">Child elements</span></span>

<span data-ttu-id="341eb-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="341eb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="341eb-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="341eb-125">Attributes</span></span>

|<span data-ttu-id="341eb-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="341eb-126">**Attribute**</span></span>|<span data-ttu-id="341eb-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="341eb-127">**Type**</span></span>|<span data-ttu-id="341eb-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="341eb-128">**Required**</span></span>|<span data-ttu-id="341eb-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="341eb-129">**Description**</span></span>|<span data-ttu-id="341eb-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="341eb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="341eb-131">PageID</span><span class="sxs-lookup"><span data-stu-id="341eb-131">PageID</span></span>  <br/> |<span data-ttu-id="341eb-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="341eb-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="341eb-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="341eb-133">required</span></span>  <br/> |<span data-ttu-id="341eb-134">ID de página da forma vinculada aos dados na linha de conjunto de registros de dados identificada por **ROWID**.</span><span class="sxs-lookup"><span data-stu-id="341eb-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="341eb-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="341eb-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="341eb-136">RowID</span><span class="sxs-lookup"><span data-stu-id="341eb-136">RowID</span></span>  <br/> |<span data-ttu-id="341eb-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="341eb-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="341eb-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="341eb-138">required</span></span>  <br/> |<span data-ttu-id="341eb-139">ID de linha da linha, exclusiva no conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="341eb-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="341eb-140">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="341eb-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="341eb-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="341eb-141">ShapeID</span></span>  <br/> |<span data-ttu-id="341eb-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="341eb-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="341eb-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="341eb-143">required</span></span>  <br/> |<span data-ttu-id="341eb-144">ID da forma vinculada aos dados na linha de conjunto de registros de dados identificada por **ROWID**.</span><span class="sxs-lookup"><span data-stu-id="341eb-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="341eb-145">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="341eb-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

