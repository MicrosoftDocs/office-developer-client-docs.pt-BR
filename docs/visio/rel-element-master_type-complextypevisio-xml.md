---
title: Elemento REL (Master_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Especifica uma relação a uma parte com o XML de mestre correspondente.
ms.openlocfilehash: 8cd16c55b24cd6edec993cb913709beff72ee325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772669"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="36d56-103">Elemento REL (Master_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="36d56-103">Rel element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="36d56-104">Especifica uma relação a uma parte com o XML de mestre correspondente.</span><span class="sxs-lookup"><span data-stu-id="36d56-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36d56-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="36d56-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36d56-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="36d56-106">**Element type**</span></span> <br/> |[<span data-ttu-id="36d56-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="36d56-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="36d56-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="36d56-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="36d56-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="36d56-109">**Schema file**</span></span> <br/> |<span data-ttu-id="36d56-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="36d56-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="36d56-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="36d56-111">**Document parts**</span></span> <br/> |<span data-ttu-id="36d56-112">Pages.XML, masters.xml, recordsets.xml,. XML n º de página, mestre. XML de #</span><span class="sxs-lookup"><span data-stu-id="36d56-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36d56-113">Definição</span><span class="sxs-lookup"><span data-stu-id="36d56-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="36d56-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="36d56-114">Elements and attributes</span></span>

<span data-ttu-id="36d56-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="36d56-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="36d56-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="36d56-116">Parent elements</span></span>

|<span data-ttu-id="36d56-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="36d56-117">**Element**</span></span>|<span data-ttu-id="36d56-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="36d56-118">**Type**</span></span>|<span data-ttu-id="36d56-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36d56-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="36d56-120">Master</span><span class="sxs-lookup"><span data-stu-id="36d56-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36d56-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="36d56-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="36d56-122">Especifica uma instância do mestre XML armazenado no desenho.</span><span class="sxs-lookup"><span data-stu-id="36d56-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="36d56-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="36d56-123">Child elements</span></span>

<span data-ttu-id="36d56-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="36d56-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36d56-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="36d56-125">Attributes</span></span>

|<span data-ttu-id="36d56-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="36d56-126">**Attribute**</span></span>|<span data-ttu-id="36d56-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="36d56-127">**Type**</span></span>|<span data-ttu-id="36d56-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="36d56-128">**Required**</span></span>|<span data-ttu-id="36d56-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36d56-129">**Description**</span></span>|<span data-ttu-id="36d56-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="36d56-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="36d56-131">r: id</span><span class="sxs-lookup"><span data-stu-id="36d56-131">r:id</span></span>  <br/> |<span data-ttu-id="36d56-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="36d56-132">xsd:string</span></span>  <br/> <span data-ttu-id="36d56-133">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="36d56-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="36d56-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="36d56-134">required</span></span>  <br/> |<span data-ttu-id="36d56-135">Especifica uma relação a uma parte.</span><span class="sxs-lookup"><span data-stu-id="36d56-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="36d56-136">"livrar #"</span><span class="sxs-lookup"><span data-stu-id="36d56-136">"rId#"</span></span>  <br/> <span data-ttu-id="36d56-137">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="36d56-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36d56-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="36d56-138">Remarks</span></span>

<span data-ttu-id="36d56-139">O valor do atributo **id de r:** deve ser um tipo de **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="36d56-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="36d56-140">O tipo de **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato 'eliminar #', onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="36d56-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="36d56-141">O número deve ser exclusivo entre todos os elementos filho do elemento **Rel** .</span><span class="sxs-lookup"><span data-stu-id="36d56-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="36d56-142">Para obter mais informações sobre o tipo de ST_RelationshipID, consulte a [especificação de ISO/IEC 29500 parte 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="36d56-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

