---
title: Elemento REL (ForeignData_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Especifica uma relação entre uma forma e uma parte do documento que contém os dados de imagem associados à forma.
ms.openlocfilehash: f54cd76788d6f5d916b9ed181f309687109dd589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772674"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="d7213-103">Elemento REL (ForeignData_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d7213-103">Rel element (ForeignData_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d7213-104">Especifica uma relação entre uma forma e uma parte do documento que contém os dados de imagem associados à forma.</span><span class="sxs-lookup"><span data-stu-id="d7213-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7213-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="d7213-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7213-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="d7213-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d7213-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="d7213-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d7213-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d7213-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d7213-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d7213-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d7213-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d7213-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d7213-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="d7213-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d7213-112">Pages.XML, masters.xml, recordsets.xml,. XML n º de página, mestre. XML de #</span><span class="sxs-lookup"><span data-stu-id="d7213-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d7213-113">Definição</span><span class="sxs-lookup"><span data-stu-id="d7213-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d7213-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d7213-114">Elements and attributes</span></span>

<span data-ttu-id="d7213-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d7213-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d7213-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d7213-116">Parent elements</span></span>

|<span data-ttu-id="d7213-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d7213-117">**Element**</span></span>|<span data-ttu-id="d7213-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d7213-118">**Type**</span></span>|<span data-ttu-id="d7213-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d7213-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d7213-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="d7213-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7213-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="d7213-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7213-122">Especifica uma instância de dados de imagem armazenados no desenho.</span><span class="sxs-lookup"><span data-stu-id="d7213-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d7213-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d7213-123">Child elements</span></span>

<span data-ttu-id="d7213-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d7213-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7213-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7213-125">Attributes</span></span>

|<span data-ttu-id="d7213-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d7213-126">**Attribute**</span></span>|<span data-ttu-id="d7213-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d7213-127">**Type**</span></span>|<span data-ttu-id="d7213-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d7213-128">**Required**</span></span>|<span data-ttu-id="d7213-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d7213-129">**Description**</span></span>|<span data-ttu-id="d7213-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d7213-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d7213-131">r: id</span><span class="sxs-lookup"><span data-stu-id="d7213-131">r:id</span></span>  <br/> |<span data-ttu-id="d7213-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d7213-132">xsd:string</span></span>  <br/> <span data-ttu-id="d7213-133">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="d7213-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="d7213-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="d7213-134">required</span></span>  <br/> |<span data-ttu-id="d7213-135">Especifica uma relação a uma parte.</span><span class="sxs-lookup"><span data-stu-id="d7213-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="d7213-136">"livrar #"</span><span class="sxs-lookup"><span data-stu-id="d7213-136">"rId#"</span></span>  <br/> <span data-ttu-id="d7213-137">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="d7213-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7213-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7213-138">Remarks</span></span>

<span data-ttu-id="d7213-139">O valor do atributo **id de r:** deve ser um tipo de **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="d7213-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="d7213-140">O tipo de **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato 'eliminar #', onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="d7213-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="d7213-141">O número deve ser exclusivo entre todos os elementos filho do elemento **Rel** .</span><span class="sxs-lookup"><span data-stu-id="d7213-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="d7213-142">Para obter mais informações sobre o tipo de ST_RelationshipID, consulte a [especificação de ISO/IEC 29500 parte 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="d7213-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

