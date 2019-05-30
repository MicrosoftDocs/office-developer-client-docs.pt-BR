---
title: Elemento RefreshConflict (DataRecordSet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indica uma linha do conjunto de dados vinculados a uma forma que está em conflito após a atualização de conjunto do registros de dados.
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542832"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="bc09f-103">Elemento RefreshConflict (DataRecordSet_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="bc09f-103">RefreshConflict element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="bc09f-104">Indica uma linha do conjunto de dados vinculados a uma forma que está em conflito após a atualização de conjunto do registros de dados.</span><span class="sxs-lookup"><span data-stu-id="bc09f-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc09f-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="bc09f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc09f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="bc09f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bc09f-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="bc09f-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bc09f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bc09f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bc09f-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bc09f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bc09f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bc09f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bc09f-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="bc09f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bc09f-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="bc09f-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bc09f-113">Definição</span><span class="sxs-lookup"><span data-stu-id="bc09f-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bc09f-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="bc09f-114">Elements and attributes</span></span>

<span data-ttu-id="bc09f-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="bc09f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bc09f-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="bc09f-116">Parent elements</span></span>

|<span data-ttu-id="bc09f-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bc09f-117">**Element**</span></span>|<span data-ttu-id="bc09f-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bc09f-118">**Type**</span></span>|<span data-ttu-id="bc09f-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bc09f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bc09f-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="bc09f-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bc09f-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="bc09f-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bc09f-122">Armazena, formata, atualiza e expõe dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="bc09f-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bc09f-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bc09f-123">Child elements</span></span>

<span data-ttu-id="bc09f-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="bc09f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc09f-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="bc09f-125">Attributes</span></span>

|<span data-ttu-id="bc09f-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bc09f-126">**Attribute**</span></span>|<span data-ttu-id="bc09f-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bc09f-127">**Type**</span></span>|<span data-ttu-id="bc09f-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="bc09f-128">**Required**</span></span>|<span data-ttu-id="bc09f-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bc09f-129">**Description**</span></span>|<span data-ttu-id="bc09f-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="bc09f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bc09f-131">PageID</span><span class="sxs-lookup"><span data-stu-id="bc09f-131">PageID</span></span>  <br/> |<span data-ttu-id="bc09f-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bc09f-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bc09f-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bc09f-133">required</span></span>  <br/> |<span data-ttu-id="bc09f-134">ID de página da forma envolvida no conflito.</span><span class="sxs-lookup"><span data-stu-id="bc09f-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="bc09f-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bc09f-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bc09f-136">RowID</span><span class="sxs-lookup"><span data-stu-id="bc09f-136">RowID</span></span>  <br/> |<span data-ttu-id="bc09f-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bc09f-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bc09f-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bc09f-138">required</span></span>  <br/> |<span data-ttu-id="bc09f-139">A ID da linha original da linha agora está em conflito após a atualização dos dados.</span><span class="sxs-lookup"><span data-stu-id="bc09f-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="bc09f-140">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bc09f-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bc09f-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="bc09f-141">ShapeID</span></span>  <br/> |<span data-ttu-id="bc09f-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bc09f-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bc09f-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bc09f-143">required</span></span>  <br/> |<span data-ttu-id="bc09f-144">ID da forma envolvida no conflito.</span><span class="sxs-lookup"><span data-stu-id="bc09f-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="bc09f-145">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bc09f-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

