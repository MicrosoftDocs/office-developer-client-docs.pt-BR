---
title: Elemento Rel (ForeignData_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Especifica uma relação entre uma forma e uma parte do documento que contém os dados de imagem associados à forma.
ms.openlocfilehash: 5836fd306670600f65eda1f3a998ef4c5479114b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542804"
---
# <a name="rel-element-foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="f0bab-103">Elemento Rel (ForeignData_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="f0bab-103">Rel element (ForeignData_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f0bab-104">Especifica uma relação entre uma forma e uma parte do documento que contém os dados de imagem associados à forma.</span><span class="sxs-lookup"><span data-stu-id="f0bab-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0bab-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="f0bab-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0bab-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f0bab-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f0bab-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f0bab-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f0bab-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f0bab-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f0bab-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f0bab-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f0bab-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f0bab-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f0bab-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="f0bab-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f0bab-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="f0bab-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f0bab-113">Definição</span><span class="sxs-lookup"><span data-stu-id="f0bab-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f0bab-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f0bab-114">Elements and attributes</span></span>

<span data-ttu-id="f0bab-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f0bab-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f0bab-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f0bab-116">Parent elements</span></span>

|<span data-ttu-id="f0bab-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f0bab-117">**Element**</span></span>|<span data-ttu-id="f0bab-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0bab-118">**Type**</span></span>|<span data-ttu-id="f0bab-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f0bab-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f0bab-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="f0bab-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f0bab-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="f0bab-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f0bab-122">Especifica uma instância de dados de imagem armazenados no desenho.</span><span class="sxs-lookup"><span data-stu-id="f0bab-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f0bab-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f0bab-123">Child elements</span></span>

<span data-ttu-id="f0bab-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f0bab-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0bab-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0bab-125">Attributes</span></span>

|<span data-ttu-id="f0bab-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f0bab-126">**Attribute**</span></span>|<span data-ttu-id="f0bab-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0bab-127">**Type**</span></span>|<span data-ttu-id="f0bab-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f0bab-128">**Required**</span></span>|<span data-ttu-id="f0bab-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f0bab-129">**Description**</span></span>|<span data-ttu-id="f0bab-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f0bab-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f0bab-131">r:id</span><span class="sxs-lookup"><span data-stu-id="f0bab-131">r:id</span></span>  <br/> |<span data-ttu-id="f0bab-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f0bab-132">xsd:string</span></span>  <br/> <span data-ttu-id="f0bab-133">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="f0bab-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="f0bab-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f0bab-134">required</span></span>  <br/> |<span data-ttu-id="f0bab-135">Especifica uma relação com uma parte.</span><span class="sxs-lookup"><span data-stu-id="f0bab-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="f0bab-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="f0bab-136">"rId#"</span></span>  <br/> <span data-ttu-id="f0bab-137">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="f0bab-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0bab-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0bab-138">Remarks</span></span>

<span data-ttu-id="f0bab-139">O valor do atributo **r:id** deve ser um **tipo ST_RelationshipID** usuário.</span><span class="sxs-lookup"><span data-stu-id="f0bab-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="f0bab-140">O **ST_RelationshipID** tipo é uma cadeia de caracteres que deve estar no formato 'rId#', onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="f0bab-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="f0bab-141">O número deve ser exclusivo entre todos os elementos irmãos do **elemento Rel.**</span><span class="sxs-lookup"><span data-stu-id="f0bab-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="f0bab-142">Para obter mais informações sobre o ST_RelationshipID, consulte a especificação [ISO/IEC 29500 Parte 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)</span><span class="sxs-lookup"><span data-stu-id="f0bab-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

