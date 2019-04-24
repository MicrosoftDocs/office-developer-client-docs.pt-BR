---
title: Elemento rel (Page_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Especifica uma relação com uma parte com a página XML correspondente.
ms.openlocfilehash: 7a45764817175f670cdb009157e21a1a25f31cc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319996"
---
# <a name="rel-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="cc2ad-103">Elemento rel (Page_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cc2ad-103">Rel element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cc2ad-104">Especifica uma relação com uma parte com a página XML correspondente.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc2ad-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="cc2ad-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc2ad-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cc2ad-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="cc2ad-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cc2ad-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cc2ad-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cc2ad-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cc2ad-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cc2ad-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cc2ad-112">Pages. xml, Masters. xml, Recordsets. xml, Page #. xml, Master #. xml</span><span class="sxs-lookup"><span data-stu-id="cc2ad-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc2ad-113">Definição</span><span class="sxs-lookup"><span data-stu-id="cc2ad-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc2ad-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cc2ad-114">Elements and attributes</span></span>

<span data-ttu-id="cc2ad-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cc2ad-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="cc2ad-116">Parent elements</span></span>

|<span data-ttu-id="cc2ad-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-117">**Element**</span></span>|<span data-ttu-id="cc2ad-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-118">**Type**</span></span>|<span data-ttu-id="cc2ad-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc2ad-120">Page</span><span class="sxs-lookup"><span data-stu-id="cc2ad-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc2ad-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="cc2ad-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cc2ad-122">Especifica uma instância do XML de página armazenada no desenho.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cc2ad-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cc2ad-123">Child elements</span></span>

<span data-ttu-id="cc2ad-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc2ad-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc2ad-125">Attributes</span></span>

|<span data-ttu-id="cc2ad-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-126">**Attribute**</span></span>|<span data-ttu-id="cc2ad-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-127">**Type**</span></span>|<span data-ttu-id="cc2ad-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-128">**Required**</span></span>|<span data-ttu-id="cc2ad-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-129">**Description**</span></span>|<span data-ttu-id="cc2ad-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="cc2ad-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cc2ad-131">r:ID</span><span class="sxs-lookup"><span data-stu-id="cc2ad-131">r:id</span></span>  <br/> |<span data-ttu-id="cc2ad-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cc2ad-132">xsd:string</span></span>  <br/> <span data-ttu-id="cc2ad-133">Consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="cc2ad-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc2ad-134">required</span></span>  <br/> |<span data-ttu-id="cc2ad-135">Especifica uma relação com uma parte.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="cc2ad-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="cc2ad-136">"rId#"</span></span>  <br/> <span data-ttu-id="cc2ad-137">Consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc2ad-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc2ad-138">Remarks</span></span>

<span data-ttu-id="cc2ad-139">O valor do atributo **r:ID** deve ser um tipo **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="cc2ad-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="cc2ad-140">O tipo **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato "rId #", onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="cc2ad-141">O número deve ser exclusivo entre todos os elementos irmãos do elemento **rel** .</span><span class="sxs-lookup"><span data-stu-id="cc2ad-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="cc2ad-142">Para obter mais informações sobre o tipo ST_RelationshipID, consulte a [Especificação ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="cc2ad-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

