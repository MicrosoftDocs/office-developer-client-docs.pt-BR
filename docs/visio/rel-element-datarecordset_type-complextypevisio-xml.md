---
title: Elemento REL (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Especifica uma relação a uma parte com o recordset associado e informações de ligação de dados.
ms.openlocfilehash: ca3584cfa8f1791e126d867a541de1fe9ec4b354
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395312"
---
# <a name="rel-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="43293-103">Elemento REL (DataRecordSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="43293-103">Rel element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="43293-104">Especifica uma relação a uma parte com o recordset associado e informações de ligação de dados.</span><span class="sxs-lookup"><span data-stu-id="43293-104">Specifies a relationship to a part with the associated recordset and data binding information.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43293-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="43293-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43293-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="43293-106">**Element type**</span></span> <br/> |[<span data-ttu-id="43293-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="43293-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="43293-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="43293-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="43293-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="43293-109">**Schema file**</span></span> <br/> |<span data-ttu-id="43293-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="43293-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="43293-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="43293-111">**Document parts**</span></span> <br/> |<span data-ttu-id="43293-112">Pages.XML, masters.xml, recordsets.xml,. XML n º de página, mestre. XML de #</span><span class="sxs-lookup"><span data-stu-id="43293-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43293-113">Definição</span><span class="sxs-lookup"><span data-stu-id="43293-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="43293-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="43293-114">Elements and attributes</span></span>

<span data-ttu-id="43293-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="43293-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="43293-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="43293-116">Parent elements</span></span>

|<span data-ttu-id="43293-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="43293-117">**Element**</span></span>|<span data-ttu-id="43293-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="43293-118">**Type**</span></span>|<span data-ttu-id="43293-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43293-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="43293-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="43293-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="43293-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="43293-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="43293-122">Especifica uma instância de um conjunto de registros e informações de associação de dados armazenadas no desenho.</span><span class="sxs-lookup"><span data-stu-id="43293-122">Specifies one instance of a recordset and data binding information stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="43293-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="43293-123">Child elements</span></span>

<span data-ttu-id="43293-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="43293-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43293-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="43293-125">Attributes</span></span>

|<span data-ttu-id="43293-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="43293-126">**Attribute**</span></span>|<span data-ttu-id="43293-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="43293-127">**Type**</span></span>|<span data-ttu-id="43293-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="43293-128">**Required**</span></span>|<span data-ttu-id="43293-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43293-129">**Description**</span></span>|<span data-ttu-id="43293-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="43293-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43293-131">r: id</span><span class="sxs-lookup"><span data-stu-id="43293-131">r:id</span></span>  <br/> |<span data-ttu-id="43293-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="43293-132">xsd:string</span></span>  <br/> <span data-ttu-id="43293-133">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="43293-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="43293-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="43293-134">required</span></span>  <br/> |<span data-ttu-id="43293-135">Especifica uma relação a uma parte.</span><span class="sxs-lookup"><span data-stu-id="43293-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="43293-136">"livrar #"</span><span class="sxs-lookup"><span data-stu-id="43293-136">"rId#"</span></span>  <br/> <span data-ttu-id="43293-137">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="43293-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43293-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="43293-138">Remarks</span></span>

<span data-ttu-id="43293-139">O valor do atributo **id de r:** deve ser um tipo de **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="43293-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="43293-140">O tipo de **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato 'eliminar #', onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="43293-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="43293-141">O número deve ser exclusivo entre todos os elementos filho do elemento **Rel** .</span><span class="sxs-lookup"><span data-stu-id="43293-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="43293-142">Para obter mais informações sobre o tipo de ST_RelationshipID, consulte a [especificação de ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="43293-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

