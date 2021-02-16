---
title: Elemento Rel (Solution_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Especifica uma relação com uma parte com o XML da solução associado a essa solução.
ms.openlocfilehash: 1fe48579da28501b74fedd507f3e44d59736ae87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542762"
---
# <a name="rel-element-solution_type-complextype-visio-xml"></a><span data-ttu-id="9a7a5-103">Elemento Rel (Solution_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="9a7a5-103">Rel element (Solution_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9a7a5-104">Especifica uma relação com uma parte com o XML da solução associado a essa solução.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a7a5-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="9a7a5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a7a5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9a7a5-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="9a7a5-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9a7a5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9a7a5-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9a7a5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9a7a5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9a7a5-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9a7a5-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="9a7a5-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a7a5-113">Definição</span><span class="sxs-lookup"><span data-stu-id="9a7a5-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9a7a5-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9a7a5-114">Elements and attributes</span></span>

<span data-ttu-id="9a7a5-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9a7a5-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9a7a5-116">Parent elements</span></span>

|<span data-ttu-id="9a7a5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-117">**Element**</span></span>|<span data-ttu-id="9a7a5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-118">**Type**</span></span>|<span data-ttu-id="9a7a5-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a7a5-120">Solution</span><span class="sxs-lookup"><span data-stu-id="9a7a5-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a7a5-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="9a7a5-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9a7a5-122">Especifica uma instância de SOLUÇÃO XML armazenada no desenho.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9a7a5-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9a7a5-123">Child elements</span></span>

<span data-ttu-id="9a7a5-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a7a5-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a7a5-125">Attributes</span></span>

|<span data-ttu-id="9a7a5-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-126">**Attribute**</span></span>|<span data-ttu-id="9a7a5-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-127">**Type**</span></span>|<span data-ttu-id="9a7a5-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-128">**Required**</span></span>|<span data-ttu-id="9a7a5-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-129">**Description**</span></span>|<span data-ttu-id="9a7a5-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a7a5-131">r:id</span><span class="sxs-lookup"><span data-stu-id="9a7a5-131">r:id</span></span>  <br/> |<span data-ttu-id="9a7a5-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a7a5-132">xsd:string</span></span>  <br/> <span data-ttu-id="9a7a5-133">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="9a7a5-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9a7a5-134">required</span></span>  <br/> |<span data-ttu-id="9a7a5-135">Especifica uma relação com uma parte.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="9a7a5-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="9a7a5-136">"rId#"</span></span>  <br/> <span data-ttu-id="9a7a5-137">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a7a5-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a7a5-138">Remarks</span></span>

<span data-ttu-id="9a7a5-139">O valor do atributo **r:id** deve ser um **tipo ST_RelationshipID** usuário.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="9a7a5-140">O **ST_RelationshipID** tipo é uma cadeia de caracteres que deve estar no formato 'rId#', onde o caractere final deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="9a7a5-141">O número deve ser exclusivo entre todos os elementos irmãos do **elemento Rel.**</span><span class="sxs-lookup"><span data-stu-id="9a7a5-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="9a7a5-142">Para obter mais informações sobre o ST_RelationshipID, consulte a especificação [ISO/IEC 29500 Parte 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)</span><span class="sxs-lookup"><span data-stu-id="9a7a5-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

