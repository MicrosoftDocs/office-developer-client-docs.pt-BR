---
title: Elemento REL (ForeignData_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Especifica uma relação entre uma forma e uma parte do documento que contém os dados de imagem associados à forma.
ms.openlocfilehash: 2667d5b0b940384f10df62dfc0fbf6acfa7d4ba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383440"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="f1e6b-103">Elemento REL (ForeignData_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f1e6b-103">Rel element (ForeignData_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f1e6b-104">Especifica uma relação entre uma forma e uma parte do documento que contém os dados de imagem associados à forma.</span><span class="sxs-lookup"><span data-stu-id="f1e6b-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1e6b-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="f1e6b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1e6b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f1e6b-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f1e6b-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f1e6b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f1e6b-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f1e6b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f1e6b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f1e6b-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f1e6b-112">Pages.XML, masters.xml, recordsets.xml,. XML n º de página, mestre. XML de #</span><span class="sxs-lookup"><span data-stu-id="f1e6b-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f1e6b-113">Definição</span><span class="sxs-lookup"><span data-stu-id="f1e6b-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f1e6b-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f1e6b-114">Elements and attributes</span></span>

<span data-ttu-id="f1e6b-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f1e6b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f1e6b-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f1e6b-116">Parent elements</span></span>

|<span data-ttu-id="f1e6b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-117">**Element**</span></span>|<span data-ttu-id="f1e6b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-118">**Type**</span></span>|<span data-ttu-id="f1e6b-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1e6b-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="f1e6b-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f1e6b-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="f1e6b-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f1e6b-122">Especifica uma instância de dados de imagem armazenados no desenho.</span><span class="sxs-lookup"><span data-stu-id="f1e6b-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f1e6b-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f1e6b-123">Child elements</span></span>

<span data-ttu-id="f1e6b-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f1e6b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1e6b-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1e6b-125">Attributes</span></span>

|<span data-ttu-id="f1e6b-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-126">**Attribute**</span></span>|<span data-ttu-id="f1e6b-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-127">**Type**</span></span>|<span data-ttu-id="f1e6b-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-128">**Required**</span></span>|<span data-ttu-id="f1e6b-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-129">**Description**</span></span>|<span data-ttu-id="f1e6b-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f1e6b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f1e6b-131">r: id</span><span class="sxs-lookup"><span data-stu-id="f1e6b-131">r:id</span></span>  <br/> |<span data-ttu-id="f1e6b-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f1e6b-132">xsd:string</span></span>  <br/> <span data-ttu-id="f1e6b-133">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="f1e6b-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="f1e6b-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f1e6b-134">required</span></span>  <br/> |<span data-ttu-id="f1e6b-135">Especifica uma relação a uma parte.</span><span class="sxs-lookup"><span data-stu-id="f1e6b-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="f1e6b-136">"livrar #"</span><span class="sxs-lookup"><span data-stu-id="f1e6b-136">"rId#"</span></span>  <br/> <span data-ttu-id="f1e6b-137">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="f1e6b-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1e6b-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1e6b-138">Remarks</span></span>

<span data-ttu-id="f1e6b-139">O valor do atributo **id de r:** deve ser um tipo de **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="f1e6b-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="f1e6b-140">O tipo de **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato 'eliminar #', onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="f1e6b-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="f1e6b-141">O número deve ser exclusivo entre todos os elementos filho do elemento **Rel** .</span><span class="sxs-lookup"><span data-stu-id="f1e6b-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="f1e6b-142">Para obter mais informações sobre o tipo de ST_RelationshipID, consulte a [especificação de ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="f1e6b-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

