---
title: Elemento REL (Solution_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Especifica uma relação a uma parte com a solução que XML associada a essa solução.
ms.openlocfilehash: e8a1350691e8d29551fb126a2151655175cc068c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400784"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="ef319-103">Elemento REL (Solution_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ef319-103">Rel element (Solution_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ef319-104">Especifica uma relação a uma parte com a solução que XML associada a essa solução.</span><span class="sxs-lookup"><span data-stu-id="ef319-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef319-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="ef319-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef319-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ef319-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ef319-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="ef319-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ef319-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ef319-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ef319-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ef319-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ef319-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ef319-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ef319-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="ef319-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ef319-112">Pages.XML, masters.xml, recordsets.xml,. XML n º de página, mestre. XML de #</span><span class="sxs-lookup"><span data-stu-id="ef319-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef319-113">Definição</span><span class="sxs-lookup"><span data-stu-id="ef319-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ef319-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ef319-114">Elements and attributes</span></span>

<span data-ttu-id="ef319-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ef319-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ef319-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ef319-116">Parent elements</span></span>

|<span data-ttu-id="ef319-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ef319-117">**Element**</span></span>|<span data-ttu-id="ef319-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ef319-118">**Type**</span></span>|<span data-ttu-id="ef319-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ef319-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef319-120">Solution</span><span class="sxs-lookup"><span data-stu-id="ef319-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef319-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="ef319-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef319-122">Especifica uma instância da solução que XML armazenado no desenho.</span><span class="sxs-lookup"><span data-stu-id="ef319-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef319-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ef319-123">Child elements</span></span>

<span data-ttu-id="ef319-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ef319-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef319-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef319-125">Attributes</span></span>

|<span data-ttu-id="ef319-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ef319-126">**Attribute**</span></span>|<span data-ttu-id="ef319-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ef319-127">**Type**</span></span>|<span data-ttu-id="ef319-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ef319-128">**Required**</span></span>|<span data-ttu-id="ef319-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ef319-129">**Description**</span></span>|<span data-ttu-id="ef319-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ef319-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ef319-131">r: id</span><span class="sxs-lookup"><span data-stu-id="ef319-131">r:id</span></span>  <br/> |<span data-ttu-id="ef319-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ef319-132">xsd:string</span></span>  <br/> <span data-ttu-id="ef319-133">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="ef319-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="ef319-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ef319-134">required</span></span>  <br/> |<span data-ttu-id="ef319-135">Especifica uma relação a uma parte.</span><span class="sxs-lookup"><span data-stu-id="ef319-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="ef319-136">"livrar #"</span><span class="sxs-lookup"><span data-stu-id="ef319-136">"rId#"</span></span>  <br/> <span data-ttu-id="ef319-137">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="ef319-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef319-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef319-138">Remarks</span></span>

<span data-ttu-id="ef319-139">O valor do atributo **id de r:** deve ser um tipo de **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="ef319-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="ef319-140">O tipo de **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato 'eliminar #', onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="ef319-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="ef319-141">O número deve ser exclusivo entre todos os elementos filho do elemento **Rel** .</span><span class="sxs-lookup"><span data-stu-id="ef319-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="ef319-142">Para obter mais informações sobre o tipo de ST_RelationshipID, consulte a [especificação de ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="ef319-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

