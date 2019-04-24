---
title: RefBy_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: ebfc84b2e7eb88078b3b8010f0a7001e90a9cb31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348318"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="2f9f2-102">RefBy_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2f9f2-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2f9f2-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="2f9f2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f9f2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2f9f2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2f9f2-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2f9f2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2f9f2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2f9f2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2f9f2-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="2f9f2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2f9f2-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2f9f2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2f9f2-109">Definição</span><span class="sxs-lookup"><span data-stu-id="2f9f2-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2f9f2-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2f9f2-110">Elements and attributes</span></span>

<span data-ttu-id="2f9f2-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2f9f2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2f9f2-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2f9f2-112">Child elements</span></span>

<span data-ttu-id="2f9f2-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2f9f2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f9f2-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2f9f2-114">Attributes</span></span>

|<span data-ttu-id="2f9f2-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2f9f2-115">**Attribute**</span></span>|<span data-ttu-id="2f9f2-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2f9f2-116">**Type**</span></span>|<span data-ttu-id="2f9f2-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2f9f2-117">**Required**</span></span>|<span data-ttu-id="2f9f2-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2f9f2-118">**Description**</span></span>|<span data-ttu-id="2f9f2-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2f9f2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2f9f2-120">ID</span><span class="sxs-lookup"><span data-stu-id="2f9f2-120">ID</span></span>  <br/> |<span data-ttu-id="2f9f2-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2f9f2-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2f9f2-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2f9f2-122">required</span></span>  <br/> ||<span data-ttu-id="2f9f2-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2f9f2-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2f9f2-124">T</span><span class="sxs-lookup"><span data-stu-id="2f9f2-124">T</span></span>  <br/> |<span data-ttu-id="2f9f2-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2f9f2-125">xsd:string</span></span>  <br/> |<span data-ttu-id="2f9f2-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2f9f2-126">required</span></span>  <br/> ||<span data-ttu-id="2f9f2-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2f9f2-127">Values of the xsd:string type.</span></span>  <br/> |
   

