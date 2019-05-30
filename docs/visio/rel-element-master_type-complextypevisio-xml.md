---
title: Elemento rel (Master_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Especifica uma relação com uma parte com o XML mestre correspondente.
ms.openlocfilehash: 032c1ef4a94bb6acf18587a1257fe82285124e87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542797"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="c65a4-103">Elemento rel (Master_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="c65a4-103">Rel element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c65a4-104">Especifica uma relação com uma parte com o XML mestre correspondente.</span><span class="sxs-lookup"><span data-stu-id="c65a4-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c65a4-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="c65a4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c65a4-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c65a4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c65a4-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c65a4-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c65a4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c65a4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c65a4-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c65a4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c65a4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c65a4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c65a4-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="c65a4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c65a4-112">Pages. xml, Masters. xml, Recordsets. xml, Page #. xml, Master #. xml</span><span class="sxs-lookup"><span data-stu-id="c65a4-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c65a4-113">Definição</span><span class="sxs-lookup"><span data-stu-id="c65a4-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c65a4-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c65a4-114">Elements and attributes</span></span>

<span data-ttu-id="c65a4-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c65a4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c65a4-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c65a4-116">Parent elements</span></span>

|<span data-ttu-id="c65a4-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c65a4-117">**Element**</span></span>|<span data-ttu-id="c65a4-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c65a4-118">**Type**</span></span>|<span data-ttu-id="c65a4-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c65a4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c65a4-120">Master</span><span class="sxs-lookup"><span data-stu-id="c65a4-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c65a4-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="c65a4-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c65a4-122">Especifica uma instância do XML mestre armazenado no desenho.</span><span class="sxs-lookup"><span data-stu-id="c65a4-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c65a4-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c65a4-123">Child elements</span></span>

<span data-ttu-id="c65a4-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c65a4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c65a4-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="c65a4-125">Attributes</span></span>

|<span data-ttu-id="c65a4-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c65a4-126">**Attribute**</span></span>|<span data-ttu-id="c65a4-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c65a4-127">**Type**</span></span>|<span data-ttu-id="c65a4-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c65a4-128">**Required**</span></span>|<span data-ttu-id="c65a4-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c65a4-129">**Description**</span></span>|<span data-ttu-id="c65a4-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c65a4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c65a4-131">r:id</span><span class="sxs-lookup"><span data-stu-id="c65a4-131">r:id</span></span>  <br/> |<span data-ttu-id="c65a4-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c65a4-132">xsd:string</span></span>  <br/> <span data-ttu-id="c65a4-133">Consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="c65a4-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="c65a4-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c65a4-134">required</span></span>  <br/> |<span data-ttu-id="c65a4-135">Especifica uma relação com uma parte.</span><span class="sxs-lookup"><span data-stu-id="c65a4-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="c65a4-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="c65a4-136">"rId#"</span></span>  <br/> <span data-ttu-id="c65a4-137">Consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="c65a4-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c65a4-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="c65a4-138">Remarks</span></span>

<span data-ttu-id="c65a4-139">O valor do atributo **r:ID** deve ser um tipo **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="c65a4-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="c65a4-140">O tipo **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato "rId #", onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="c65a4-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="c65a4-141">O número deve ser exclusivo entre todos os elementos irmãos do elemento **rel** .</span><span class="sxs-lookup"><span data-stu-id="c65a4-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="c65a4-142">Para obter mais informações sobre o tipo ST_RelationshipID, consulte a [Especificação ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="c65a4-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

