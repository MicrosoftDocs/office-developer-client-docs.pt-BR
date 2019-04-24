---
title: StyleSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329822"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="d8c90-102">StyleSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d8c90-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d8c90-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="d8c90-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8c90-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8c90-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d8c90-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d8c90-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d8c90-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d8c90-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d8c90-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="d8c90-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d8c90-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="d8c90-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8c90-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d8c90-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d8c90-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d8c90-110">Elements and attributes</span></span>

<span data-ttu-id="d8c90-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d8c90-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d8c90-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d8c90-112">Child elements</span></span>

<span data-ttu-id="d8c90-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d8c90-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8c90-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8c90-114">Attributes</span></span>

|<span data-ttu-id="d8c90-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d8c90-115">**Attribute**</span></span>|<span data-ttu-id="d8c90-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8c90-116">**Type**</span></span>|<span data-ttu-id="d8c90-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d8c90-117">**Required**</span></span>|<span data-ttu-id="d8c90-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8c90-118">**Description**</span></span>|<span data-ttu-id="d8c90-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d8c90-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d8c90-120">ID</span><span class="sxs-lookup"><span data-stu-id="d8c90-120">ID</span></span>  <br/> |<span data-ttu-id="d8c90-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d8c90-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d8c90-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="d8c90-122">required</span></span>  <br/> ||<span data-ttu-id="d8c90-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d8c90-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d8c90-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="d8c90-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="d8c90-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d8c90-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d8c90-126">opcional</span><span class="sxs-lookup"><span data-stu-id="d8c90-126">optional</span></span>  <br/> ||<span data-ttu-id="d8c90-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d8c90-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d8c90-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="d8c90-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="d8c90-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d8c90-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d8c90-130">opcional</span><span class="sxs-lookup"><span data-stu-id="d8c90-130">optional</span></span>  <br/> ||<span data-ttu-id="d8c90-131">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d8c90-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d8c90-132">Name</span><span class="sxs-lookup"><span data-stu-id="d8c90-132">Name</span></span>  <br/> |<span data-ttu-id="d8c90-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d8c90-133">xsd:string</span></span>  <br/> |<span data-ttu-id="d8c90-134">opcional</span><span class="sxs-lookup"><span data-stu-id="d8c90-134">optional</span></span>  <br/> ||<span data-ttu-id="d8c90-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d8c90-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d8c90-136">NameU</span><span class="sxs-lookup"><span data-stu-id="d8c90-136">NameU</span></span>  <br/> |<span data-ttu-id="d8c90-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d8c90-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d8c90-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d8c90-138">optional</span></span>  <br/> ||<span data-ttu-id="d8c90-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d8c90-139">Values of the xsd:string type.</span></span>  <br/> |
   

