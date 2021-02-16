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
# <a name="celldef_type-complextype-visio-xml"></a><span data-ttu-id="c6807-102">CellDef_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="c6807-102">CellDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c6807-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="c6807-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6807-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c6807-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c6807-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c6807-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c6807-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c6807-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c6807-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="c6807-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c6807-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c6807-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c6807-109">Definição</span><span class="sxs-lookup"><span data-stu-id="c6807-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c6807-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c6807-110">Elements and attributes</span></span>

<span data-ttu-id="c6807-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c6807-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c6807-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c6807-112">Child elements</span></span>

<span data-ttu-id="c6807-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c6807-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6807-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c6807-114">Attributes</span></span>

|<span data-ttu-id="c6807-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c6807-115">**Attribute**</span></span>|<span data-ttu-id="c6807-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c6807-116">**Type**</span></span>|<span data-ttu-id="c6807-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c6807-117">**Required**</span></span>|<span data-ttu-id="c6807-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c6807-118">**Description**</span></span>|<span data-ttu-id="c6807-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c6807-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c6807-120">F</span><span class="sxs-lookup"><span data-stu-id="c6807-120">F</span></span>  <br/> |<span data-ttu-id="c6807-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c6807-121">xsd:string</span></span>  <br/> |<span data-ttu-id="c6807-122">opcional</span><span class="sxs-lookup"><span data-stu-id="c6807-122">optional</span></span>  <br/> ||<span data-ttu-id="c6807-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c6807-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c6807-124">IX</span><span class="sxs-lookup"><span data-stu-id="c6807-124">IX</span></span>  <br/> |<span data-ttu-id="c6807-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c6807-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c6807-126">opcional</span><span class="sxs-lookup"><span data-stu-id="c6807-126">optional</span></span>  <br/> ||<span data-ttu-id="c6807-127">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c6807-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c6807-128">N</span><span class="sxs-lookup"><span data-stu-id="c6807-128">N</span></span>  <br/> |<span data-ttu-id="c6807-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c6807-129">xsd:string</span></span>  <br/> |<span data-ttu-id="c6807-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c6807-130">required</span></span>  <br/> ||<span data-ttu-id="c6807-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c6807-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c6807-132">S</span><span class="sxs-lookup"><span data-stu-id="c6807-132">S</span></span>  <br/> |<span data-ttu-id="c6807-133">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c6807-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="c6807-134">opcional</span><span class="sxs-lookup"><span data-stu-id="c6807-134">optional</span></span>  <br/> ||<span data-ttu-id="c6807-135">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="c6807-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="c6807-136">E</span><span class="sxs-lookup"><span data-stu-id="c6807-136">T</span></span>  <br/> |<span data-ttu-id="c6807-137">xsd:token</span><span class="sxs-lookup"><span data-stu-id="c6807-137">xsd:token</span></span>  <br/> |<span data-ttu-id="c6807-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c6807-138">required</span></span>  <br/> ||<span data-ttu-id="c6807-139">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="c6807-139">Values of the xsd:token type.</span></span>  <br/> |
   

