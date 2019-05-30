---
title: AuthorEntry_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 41279e9f4ffa0bba17d4f74eb2f40d724589c17d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537875"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="c4080-102">AuthorEntry_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="c4080-102">AuthorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c4080-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="c4080-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4080-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c4080-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c4080-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c4080-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c4080-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c4080-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c4080-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="c4080-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c4080-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c4080-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4080-109">Definição</span><span class="sxs-lookup"><span data-stu-id="c4080-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c4080-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c4080-110">Elements and attributes</span></span>

<span data-ttu-id="c4080-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c4080-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c4080-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c4080-112">Child elements</span></span>

<span data-ttu-id="c4080-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c4080-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4080-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4080-114">Attributes</span></span>

|<span data-ttu-id="c4080-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c4080-115">**Attribute**</span></span>|<span data-ttu-id="c4080-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c4080-116">**Type**</span></span>|<span data-ttu-id="c4080-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c4080-117">**Required**</span></span>|<span data-ttu-id="c4080-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c4080-118">**Description**</span></span>|<span data-ttu-id="c4080-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c4080-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c4080-120">ID</span><span class="sxs-lookup"><span data-stu-id="c4080-120">ID</span></span>  <br/> |<span data-ttu-id="c4080-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c4080-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c4080-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c4080-122">required</span></span>  <br/> ||<span data-ttu-id="c4080-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c4080-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c4080-124">Initials</span><span class="sxs-lookup"><span data-stu-id="c4080-124">Initials</span></span>  <br/> |<span data-ttu-id="c4080-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4080-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c4080-126">opcional</span><span class="sxs-lookup"><span data-stu-id="c4080-126">optional</span></span>  <br/> ||<span data-ttu-id="c4080-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c4080-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c4080-128">Nome</span><span class="sxs-lookup"><span data-stu-id="c4080-128">Name</span></span>  <br/> |<span data-ttu-id="c4080-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4080-129">xsd:string</span></span>  <br/> |<span data-ttu-id="c4080-130">opcional</span><span class="sxs-lookup"><span data-stu-id="c4080-130">optional</span></span>  <br/> ||<span data-ttu-id="c4080-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c4080-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c4080-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="c4080-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="c4080-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4080-133">xsd:string</span></span>  <br/> |<span data-ttu-id="c4080-134">opcional</span><span class="sxs-lookup"><span data-stu-id="c4080-134">optional</span></span>  <br/> ||<span data-ttu-id="c4080-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c4080-135">Values of the xsd:string type.</span></span>  <br/> |
   

