---
title: DocumentSheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326135"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="369f1-102">DocumentSheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="369f1-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="369f1-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="369f1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="369f1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="369f1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="369f1-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="369f1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="369f1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="369f1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="369f1-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="369f1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="369f1-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="369f1-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="369f1-109">Definição</span><span class="sxs-lookup"><span data-stu-id="369f1-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="369f1-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="369f1-110">Elements and attributes</span></span>

<span data-ttu-id="369f1-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="369f1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="369f1-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="369f1-112">Child elements</span></span>

<span data-ttu-id="369f1-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="369f1-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="369f1-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="369f1-114">Attributes</span></span>

|<span data-ttu-id="369f1-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="369f1-115">**Attribute**</span></span>|<span data-ttu-id="369f1-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="369f1-116">**Type**</span></span>|<span data-ttu-id="369f1-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="369f1-117">**Required**</span></span>|<span data-ttu-id="369f1-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="369f1-118">**Description**</span></span>|<span data-ttu-id="369f1-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="369f1-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="369f1-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="369f1-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="369f1-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="369f1-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="369f1-122">opcional</span><span class="sxs-lookup"><span data-stu-id="369f1-122">optional</span></span>  <br/> ||<span data-ttu-id="369f1-123">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="369f1-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="369f1-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="369f1-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="369f1-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="369f1-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="369f1-126">opcional</span><span class="sxs-lookup"><span data-stu-id="369f1-126">optional</span></span>  <br/> ||<span data-ttu-id="369f1-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="369f1-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="369f1-128">Name</span><span class="sxs-lookup"><span data-stu-id="369f1-128">Name</span></span>  <br/> |<span data-ttu-id="369f1-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="369f1-129">xsd:string</span></span>  <br/> |<span data-ttu-id="369f1-130">opcional</span><span class="sxs-lookup"><span data-stu-id="369f1-130">optional</span></span>  <br/> ||<span data-ttu-id="369f1-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="369f1-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="369f1-132">NameU</span><span class="sxs-lookup"><span data-stu-id="369f1-132">NameU</span></span>  <br/> |<span data-ttu-id="369f1-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="369f1-133">xsd:string</span></span>  <br/> |<span data-ttu-id="369f1-134">opcional</span><span class="sxs-lookup"><span data-stu-id="369f1-134">optional</span></span>  <br/> ||<span data-ttu-id="369f1-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="369f1-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="369f1-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="369f1-136">UniqueID</span></span>  <br/> |<span data-ttu-id="369f1-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="369f1-137">xsd:string</span></span>  <br/> |<span data-ttu-id="369f1-138">opcional</span><span class="sxs-lookup"><span data-stu-id="369f1-138">optional</span></span>  <br/> ||<span data-ttu-id="369f1-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="369f1-139">Values of the xsd:string type.</span></span>  <br/> |
   

