---
title: DocumentSheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396341"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="2a444-102">DocumentSheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="2a444-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2a444-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="2a444-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a444-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2a444-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2a444-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2a444-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2a444-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2a444-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2a444-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="2a444-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2a444-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="2a444-108">Sheet_Type complexType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2a444-109">Definição</span><span class="sxs-lookup"><span data-stu-id="2a444-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2a444-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2a444-110">Elements and attributes</span></span>

<span data-ttu-id="2a444-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2a444-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2a444-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2a444-112">Child elements</span></span>

<span data-ttu-id="2a444-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2a444-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a444-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a444-114">Attributes</span></span>

|<span data-ttu-id="2a444-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2a444-115">**Attribute**</span></span>|<span data-ttu-id="2a444-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2a444-116">**Type**</span></span>|<span data-ttu-id="2a444-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2a444-117">**Required**</span></span>|<span data-ttu-id="2a444-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2a444-118">**Description**</span></span>|<span data-ttu-id="2a444-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2a444-119">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2a444-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="2a444-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="2a444-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2a444-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2a444-122">opcional</span><span class="sxs-lookup"><span data-stu-id="2a444-122">optional</span></span>  <br/> ||<span data-ttu-id="2a444-123">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2a444-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2a444-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="2a444-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="2a444-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2a444-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2a444-126">opcional</span><span class="sxs-lookup"><span data-stu-id="2a444-126">optional</span></span>  <br/> ||<span data-ttu-id="2a444-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2a444-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2a444-128">Nome</span><span class="sxs-lookup"><span data-stu-id="2a444-128">Name</span></span>  <br/> |<span data-ttu-id="2a444-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2a444-129">xsd:string</span></span>  <br/> |<span data-ttu-id="2a444-130">opcional</span><span class="sxs-lookup"><span data-stu-id="2a444-130">optional</span></span>  <br/> ||<span data-ttu-id="2a444-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2a444-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2a444-132">NameU</span><span class="sxs-lookup"><span data-stu-id="2a444-132">NameU Property</span></span>  <br/> |<span data-ttu-id="2a444-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2a444-133">xsd:string</span></span>  <br/> |<span data-ttu-id="2a444-134">opcional</span><span class="sxs-lookup"><span data-stu-id="2a444-134">optional</span></span>  <br/> ||<span data-ttu-id="2a444-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2a444-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2a444-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="2a444-136">uniqueId</span></span>  <br/> |<span data-ttu-id="2a444-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2a444-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2a444-138">opcional</span><span class="sxs-lookup"><span data-stu-id="2a444-138">optional</span></span>  <br/> ||<span data-ttu-id="2a444-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2a444-139">Values of the xsd:string type.</span></span>  <br/> |
   

