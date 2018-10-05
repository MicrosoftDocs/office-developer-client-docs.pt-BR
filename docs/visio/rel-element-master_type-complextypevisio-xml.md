---
title: Elemento REL (Master_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Especifica uma relação a uma parte com o XML de mestre correspondente.
ms.openlocfilehash: 82552eeab746d9675f6175b62c34cef4a9c3c418
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393044"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="ec420-103">Elemento REL (Master_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ec420-103">Rel element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ec420-104">Especifica uma relação a uma parte com o XML de mestre correspondente.</span><span class="sxs-lookup"><span data-stu-id="ec420-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec420-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="ec420-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec420-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ec420-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ec420-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="ec420-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ec420-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ec420-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ec420-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ec420-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ec420-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ec420-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ec420-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="ec420-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ec420-112">Pages.XML, masters.xml, recordsets.xml,. XML n º de página, mestre. XML de #</span><span class="sxs-lookup"><span data-stu-id="ec420-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec420-113">Definição</span><span class="sxs-lookup"><span data-stu-id="ec420-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ec420-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ec420-114">Elements and attributes</span></span>

<span data-ttu-id="ec420-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ec420-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ec420-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ec420-116">Parent elements</span></span>

|<span data-ttu-id="ec420-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ec420-117">**Element**</span></span>|<span data-ttu-id="ec420-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ec420-118">**Type**</span></span>|<span data-ttu-id="ec420-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ec420-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ec420-120">Master</span><span class="sxs-lookup"><span data-stu-id="ec420-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec420-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="ec420-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ec420-122">Especifica uma instância do mestre XML armazenado no desenho.</span><span class="sxs-lookup"><span data-stu-id="ec420-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ec420-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ec420-123">Child elements</span></span>

<span data-ttu-id="ec420-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ec420-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec420-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="ec420-125">Attributes</span></span>

|<span data-ttu-id="ec420-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ec420-126">**Attribute**</span></span>|<span data-ttu-id="ec420-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ec420-127">**Type**</span></span>|<span data-ttu-id="ec420-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ec420-128">**Required**</span></span>|<span data-ttu-id="ec420-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ec420-129">**Description**</span></span>|<span data-ttu-id="ec420-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ec420-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ec420-131">r: id</span><span class="sxs-lookup"><span data-stu-id="ec420-131">r:id</span></span>  <br/> |<span data-ttu-id="ec420-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ec420-132">xsd:string</span></span>  <br/> <span data-ttu-id="ec420-133">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="ec420-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="ec420-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ec420-134">required</span></span>  <br/> |<span data-ttu-id="ec420-135">Especifica uma relação a uma parte.</span><span class="sxs-lookup"><span data-stu-id="ec420-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="ec420-136">"livrar #"</span><span class="sxs-lookup"><span data-stu-id="ec420-136">"rId#"</span></span>  <br/> <span data-ttu-id="ec420-137">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="ec420-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec420-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec420-138">Remarks</span></span>

<span data-ttu-id="ec420-139">O valor do atributo **id de r:** deve ser um tipo de **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="ec420-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="ec420-140">O tipo de **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato 'eliminar #', onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="ec420-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="ec420-141">O número deve ser exclusivo entre todos os elementos filho do elemento **Rel** .</span><span class="sxs-lookup"><span data-stu-id="ec420-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="ec420-142">Para obter mais informações sobre o tipo de ST_RelationshipID, consulte a [especificação de ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="ec420-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

