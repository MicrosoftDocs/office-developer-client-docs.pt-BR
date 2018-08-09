---
title: Elemento RefreshConflict (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indica uma linha no conjunto de registros de dados vinculada a uma forma que está em conflito após a atualização dos registros de dados.
ms.openlocfilehash: 0bcfb38c1a9ef84fc8581476fcce13b0de32c308
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772662"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="04100-103">Elemento RefreshConflict (DataRecordSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="04100-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="04100-104">Indica uma linha no conjunto de registros de dados vinculada a uma forma que está em conflito após a atualização dos registros de dados.</span><span class="sxs-lookup"><span data-stu-id="04100-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04100-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="04100-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04100-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="04100-106">**Element type**</span></span> <br/> |[<span data-ttu-id="04100-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="04100-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="04100-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="04100-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="04100-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="04100-109">**Schema file**</span></span> <br/> |<span data-ttu-id="04100-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="04100-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="04100-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="04100-111">**Document parts**</span></span> <br/> |<span data-ttu-id="04100-112">Recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="04100-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="04100-113">Definição</span><span class="sxs-lookup"><span data-stu-id="04100-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="04100-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="04100-114">Elements and attributes</span></span>

<span data-ttu-id="04100-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="04100-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="04100-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="04100-116">Parent elements</span></span>

|<span data-ttu-id="04100-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="04100-117">**Element**</span></span>|<span data-ttu-id="04100-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="04100-118">**Type**</span></span>|<span data-ttu-id="04100-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="04100-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="04100-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="04100-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="04100-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="04100-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="04100-122">Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="04100-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="04100-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="04100-123">Child elements</span></span>

<span data-ttu-id="04100-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="04100-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04100-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="04100-125">Attributes</span></span>

|<span data-ttu-id="04100-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="04100-126">**Attribute**</span></span>|<span data-ttu-id="04100-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="04100-127">**Type**</span></span>|<span data-ttu-id="04100-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="04100-128">**Required**</span></span>|<span data-ttu-id="04100-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="04100-129">**Description**</span></span>|<span data-ttu-id="04100-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="04100-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="04100-131">PageID</span><span class="sxs-lookup"><span data-stu-id="04100-131">PageID</span></span>  <br/> |<span data-ttu-id="04100-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04100-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04100-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="04100-133">required</span></span>  <br/> |<span data-ttu-id="04100-134">ID da página da forma envolvida no conflito.</span><span class="sxs-lookup"><span data-stu-id="04100-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="04100-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04100-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04100-136">RowID</span><span class="sxs-lookup"><span data-stu-id="04100-136">RowID</span></span>  <br/> |<span data-ttu-id="04100-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04100-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04100-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="04100-138">required</span></span>  <br/> |<span data-ttu-id="04100-139">A identificação da linha original da linha agora está em conflito após a atualização dos dados era.</span><span class="sxs-lookup"><span data-stu-id="04100-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="04100-140">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04100-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04100-141">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="04100-141">ShapeID</span></span>  <br/> |<span data-ttu-id="04100-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04100-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04100-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="04100-143">required</span></span>  <br/> |<span data-ttu-id="04100-144">Identificação da forma envolvida no conflito da forma.</span><span class="sxs-lookup"><span data-stu-id="04100-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="04100-145">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04100-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

