---
title: CellDef_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 7b437e35aadfef0390908cb1337cc738668382e5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542293"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="37013-102">CellDef_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="37013-102">CellDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="37013-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="37013-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37013-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="37013-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="37013-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="37013-105">**Schema file**</span></span> <br/> |<span data-ttu-id="37013-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="37013-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="37013-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="37013-107">**Extension base**</span></span> <br/> |<span data-ttu-id="37013-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="37013-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="37013-109">Definição</span><span class="sxs-lookup"><span data-stu-id="37013-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="37013-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="37013-110">Elements and attributes</span></span>

<span data-ttu-id="37013-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="37013-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="37013-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="37013-112">Child elements</span></span>

<span data-ttu-id="37013-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="37013-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37013-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="37013-114">Attributes</span></span>

|<span data-ttu-id="37013-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="37013-115">**Attribute**</span></span>|<span data-ttu-id="37013-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="37013-116">**Type**</span></span>|<span data-ttu-id="37013-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="37013-117">**Required**</span></span>|<span data-ttu-id="37013-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="37013-118">**Description**</span></span>|<span data-ttu-id="37013-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="37013-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="37013-120">F</span><span class="sxs-lookup"><span data-stu-id="37013-120">F</span></span>  <br/> |<span data-ttu-id="37013-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="37013-121">xsd:string</span></span>  <br/> |<span data-ttu-id="37013-122">opcional</span><span class="sxs-lookup"><span data-stu-id="37013-122">optional</span></span>  <br/> ||<span data-ttu-id="37013-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="37013-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="37013-124">IX</span><span class="sxs-lookup"><span data-stu-id="37013-124">IX</span></span>  <br/> |<span data-ttu-id="37013-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="37013-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="37013-126">opcional</span><span class="sxs-lookup"><span data-stu-id="37013-126">optional</span></span>  <br/> ||<span data-ttu-id="37013-127">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="37013-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="37013-128">N</span><span class="sxs-lookup"><span data-stu-id="37013-128">N</span></span>  <br/> |<span data-ttu-id="37013-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="37013-129">xsd:string</span></span>  <br/> |<span data-ttu-id="37013-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="37013-130">required</span></span>  <br/> ||<span data-ttu-id="37013-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="37013-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="37013-132">S</span><span class="sxs-lookup"><span data-stu-id="37013-132">S</span></span>  <br/> |<span data-ttu-id="37013-133">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="37013-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="37013-134">opcional</span><span class="sxs-lookup"><span data-stu-id="37013-134">optional</span></span>  <br/> ||<span data-ttu-id="37013-135">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="37013-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="37013-136">E</span><span class="sxs-lookup"><span data-stu-id="37013-136">T</span></span>  <br/> |<span data-ttu-id="37013-137">xsd:token</span><span class="sxs-lookup"><span data-stu-id="37013-137">xsd:token</span></span>  <br/> |<span data-ttu-id="37013-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="37013-138">required</span></span>  <br/> ||<span data-ttu-id="37013-139">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="37013-139">Values of the xsd:token type.</span></span>  <br/> |
   

