---
title: StyleSheet_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 6dcb6bbfd01c37b499dfca4d54d6cb0832e59b5a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541978"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="264bf-102">StyleSheet_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="264bf-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="264bf-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="264bf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="264bf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="264bf-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="264bf-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="264bf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="264bf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="264bf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="264bf-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="264bf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="264bf-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="264bf-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="264bf-109">Definição</span><span class="sxs-lookup"><span data-stu-id="264bf-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="264bf-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="264bf-110">Elements and attributes</span></span>

<span data-ttu-id="264bf-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="264bf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="264bf-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="264bf-112">Child elements</span></span>

<span data-ttu-id="264bf-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="264bf-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="264bf-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="264bf-114">Attributes</span></span>

|<span data-ttu-id="264bf-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="264bf-115">**Attribute**</span></span>|<span data-ttu-id="264bf-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="264bf-116">**Type**</span></span>|<span data-ttu-id="264bf-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="264bf-117">**Required**</span></span>|<span data-ttu-id="264bf-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="264bf-118">**Description**</span></span>|<span data-ttu-id="264bf-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="264bf-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="264bf-120">ID</span><span class="sxs-lookup"><span data-stu-id="264bf-120">ID</span></span>  <br/> |<span data-ttu-id="264bf-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="264bf-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="264bf-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="264bf-122">required</span></span>  <br/> ||<span data-ttu-id="264bf-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="264bf-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="264bf-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="264bf-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="264bf-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="264bf-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="264bf-126">opcional</span><span class="sxs-lookup"><span data-stu-id="264bf-126">optional</span></span>  <br/> ||<span data-ttu-id="264bf-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="264bf-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="264bf-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="264bf-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="264bf-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="264bf-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="264bf-130">opcional</span><span class="sxs-lookup"><span data-stu-id="264bf-130">optional</span></span>  <br/> ||<span data-ttu-id="264bf-131">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="264bf-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="264bf-132">Nome</span><span class="sxs-lookup"><span data-stu-id="264bf-132">Name</span></span>  <br/> |<span data-ttu-id="264bf-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="264bf-133">xsd:string</span></span>  <br/> |<span data-ttu-id="264bf-134">opcional</span><span class="sxs-lookup"><span data-stu-id="264bf-134">optional</span></span>  <br/> ||<span data-ttu-id="264bf-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="264bf-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="264bf-136">NameU</span><span class="sxs-lookup"><span data-stu-id="264bf-136">NameU</span></span>  <br/> |<span data-ttu-id="264bf-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="264bf-137">xsd:string</span></span>  <br/> |<span data-ttu-id="264bf-138">opcional</span><span class="sxs-lookup"><span data-stu-id="264bf-138">optional</span></span>  <br/> ||<span data-ttu-id="264bf-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="264bf-139">Values of the xsd:string type.</span></span>  <br/> |
   

