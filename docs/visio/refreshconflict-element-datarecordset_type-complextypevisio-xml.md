---
title: Elemento RefreshConflict (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indica uma linha no conjunto de registros de dados vinculada a uma forma que está em conflito após a atualização dos registros de dados.
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397398"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="80727-103">Elemento RefreshConflict (DataRecordSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="80727-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="80727-104">Indica uma linha no conjunto de registros de dados vinculada a uma forma que está em conflito após a atualização dos registros de dados.</span><span class="sxs-lookup"><span data-stu-id="80727-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80727-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="80727-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80727-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="80727-106">**Element type**</span></span> <br/> |[<span data-ttu-id="80727-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="80727-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="80727-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="80727-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="80727-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="80727-109">**Schema file**</span></span> <br/> |<span data-ttu-id="80727-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="80727-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="80727-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="80727-111">**Document parts**</span></span> <br/> |<span data-ttu-id="80727-112">Recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="80727-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="80727-113">Definição</span><span class="sxs-lookup"><span data-stu-id="80727-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="80727-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="80727-114">Elements and attributes</span></span>

<span data-ttu-id="80727-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="80727-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="80727-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="80727-116">Parent elements</span></span>

|<span data-ttu-id="80727-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="80727-117">**Element**</span></span>|<span data-ttu-id="80727-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="80727-118">**Type**</span></span>|<span data-ttu-id="80727-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80727-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="80727-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="80727-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="80727-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="80727-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="80727-122">Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="80727-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="80727-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="80727-123">Child elements</span></span>

<span data-ttu-id="80727-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="80727-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80727-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="80727-125">Attributes</span></span>

|<span data-ttu-id="80727-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="80727-126">**Attribute**</span></span>|<span data-ttu-id="80727-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="80727-127">**Type**</span></span>|<span data-ttu-id="80727-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="80727-128">**Required**</span></span>|<span data-ttu-id="80727-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80727-129">**Description**</span></span>|<span data-ttu-id="80727-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="80727-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="80727-131">PageID</span><span class="sxs-lookup"><span data-stu-id="80727-131">PageID</span></span>  <br/> |<span data-ttu-id="80727-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="80727-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="80727-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="80727-133">required</span></span>  <br/> |<span data-ttu-id="80727-134">ID da página da forma envolvida no conflito.</span><span class="sxs-lookup"><span data-stu-id="80727-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="80727-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="80727-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="80727-136">RowID</span><span class="sxs-lookup"><span data-stu-id="80727-136">RowID</span></span>  <br/> |<span data-ttu-id="80727-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="80727-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="80727-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="80727-138">required</span></span>  <br/> |<span data-ttu-id="80727-139">A identificação da linha original da linha agora está em conflito após a atualização dos dados era.</span><span class="sxs-lookup"><span data-stu-id="80727-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="80727-140">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="80727-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="80727-141">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="80727-141">ShapeID</span></span>  <br/> |<span data-ttu-id="80727-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="80727-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="80727-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="80727-143">required</span></span>  <br/> |<span data-ttu-id="80727-144">Identificação da forma envolvida no conflito da forma.</span><span class="sxs-lookup"><span data-stu-id="80727-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="80727-145">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="80727-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

