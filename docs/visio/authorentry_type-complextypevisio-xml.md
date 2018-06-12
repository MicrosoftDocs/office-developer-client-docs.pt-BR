---
title: AuthorEntry_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 39cf47915230b18d22db78f5470fd9c26b9c77ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771265"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="0a14b-102">AuthorEntry_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="0a14b-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0a14b-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="0a14b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a14b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0a14b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0a14b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0a14b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0a14b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0a14b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0a14b-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="0a14b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0a14b-108">None</span><span class="sxs-lookup"><span data-stu-id="0a14b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a14b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="0a14b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0a14b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="0a14b-110">Elements and attributes</span></span>

<span data-ttu-id="0a14b-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="0a14b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0a14b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0a14b-112">Child elements</span></span>

<span data-ttu-id="0a14b-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0a14b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a14b-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0a14b-114">Attributes</span></span>

|<span data-ttu-id="0a14b-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0a14b-115">**Attribute**</span></span>|<span data-ttu-id="0a14b-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0a14b-116">**Type**</span></span>|<span data-ttu-id="0a14b-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="0a14b-117">**Required**</span></span>|<span data-ttu-id="0a14b-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0a14b-118">**Description**</span></span>|<span data-ttu-id="0a14b-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="0a14b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0a14b-120">Id</span><span class="sxs-lookup"><span data-stu-id="0a14b-120">ID</span></span>  <br/> |<span data-ttu-id="0a14b-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0a14b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0a14b-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="0a14b-122">required</span></span>  <br/> ||<span data-ttu-id="0a14b-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0a14b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0a14b-124">Iniciais</span><span class="sxs-lookup"><span data-stu-id="0a14b-124">Initials</span></span>  <br/> |<span data-ttu-id="0a14b-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0a14b-125">xsd:string</span></span>  <br/> |<span data-ttu-id="0a14b-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0a14b-126">optional</span></span>  <br/> ||<span data-ttu-id="0a14b-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0a14b-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a14b-128">Nome</span><span class="sxs-lookup"><span data-stu-id="0a14b-128">Name</span></span>  <br/> |<span data-ttu-id="0a14b-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0a14b-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0a14b-130">opcional</span><span class="sxs-lookup"><span data-stu-id="0a14b-130">optional</span></span>  <br/> ||<span data-ttu-id="0a14b-131">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0a14b-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a14b-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="0a14b-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="0a14b-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="0a14b-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0a14b-134">opcional</span><span class="sxs-lookup"><span data-stu-id="0a14b-134">optional</span></span>  <br/> ||<span data-ttu-id="0a14b-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0a14b-135">Values of the xsd:string type.</span></span>  <br/> |
   

