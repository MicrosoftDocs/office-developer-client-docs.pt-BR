---
title: AuthorEntry_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386835"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="04eb6-102">AuthorEntry_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="04eb6-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="04eb6-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="04eb6-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04eb6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="04eb6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="04eb6-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="04eb6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="04eb6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="04eb6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="04eb6-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="04eb6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="04eb6-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="04eb6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="04eb6-109">Definição</span><span class="sxs-lookup"><span data-stu-id="04eb6-109">Definition</span></span>

```XML
      <xs:complexType name="AuthorEntry_Type">
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="Initials"
  type="xsd:string"
    />
    <xs:attribute name="ResolutionID"
  type="xsd:string"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="04eb6-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="04eb6-110">Elements and attributes</span></span>

<span data-ttu-id="04eb6-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="04eb6-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="04eb6-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="04eb6-112">Child elements</span></span>

<span data-ttu-id="04eb6-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="04eb6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04eb6-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="04eb6-114">Attributes</span></span>

|<span data-ttu-id="04eb6-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="04eb6-115">**Attribute**</span></span>|<span data-ttu-id="04eb6-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="04eb6-116">**Type**</span></span>|<span data-ttu-id="04eb6-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="04eb6-117">**Required**</span></span>|<span data-ttu-id="04eb6-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="04eb6-118">**Description**</span></span>|<span data-ttu-id="04eb6-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="04eb6-119">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="04eb6-120">ID</span><span class="sxs-lookup"><span data-stu-id="04eb6-120">ID</span></span>  <br/> |<span data-ttu-id="04eb6-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04eb6-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04eb6-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="04eb6-122">required</span></span>  <br/> ||<span data-ttu-id="04eb6-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04eb6-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04eb6-124">Initials</span><span class="sxs-lookup"><span data-stu-id="04eb6-124">Initials</span></span>  <br/> |<span data-ttu-id="04eb6-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04eb6-125">xsd:string</span></span>  <br/> |<span data-ttu-id="04eb6-126">opcional</span><span class="sxs-lookup"><span data-stu-id="04eb6-126">optional</span></span>  <br/> ||<span data-ttu-id="04eb6-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="04eb6-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04eb6-128">Nome</span><span class="sxs-lookup"><span data-stu-id="04eb6-128">Name</span></span>  <br/> |<span data-ttu-id="04eb6-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04eb6-129">xsd:string</span></span>  <br/> |<span data-ttu-id="04eb6-130">opcional</span><span class="sxs-lookup"><span data-stu-id="04eb6-130">optional</span></span>  <br/> ||<span data-ttu-id="04eb6-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="04eb6-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04eb6-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="04eb6-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="04eb6-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04eb6-133">xsd:string</span></span>  <br/> |<span data-ttu-id="04eb6-134">opcional</span><span class="sxs-lookup"><span data-stu-id="04eb6-134">optional</span></span>  <br/> ||<span data-ttu-id="04eb6-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="04eb6-135">Values of the xsd:string type.</span></span>  <br/> |
   

