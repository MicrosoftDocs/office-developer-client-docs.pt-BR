---
title: RowMap_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355731"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="10095-102">RowMap_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="10095-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="10095-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="10095-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10095-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="10095-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="10095-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="10095-105">**Schema file**</span></span> <br/> |<span data-ttu-id="10095-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="10095-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="10095-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="10095-107">**Extension base**</span></span> <br/> |<span data-ttu-id="10095-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="10095-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10095-109">Definição</span><span class="sxs-lookup"><span data-stu-id="10095-109">Definition</span></span>

```XML
      <xs:complexType name="RowMap_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="10095-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="10095-110">Elements and attributes</span></span>

<span data-ttu-id="10095-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="10095-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="10095-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="10095-112">Child elements</span></span>

<span data-ttu-id="10095-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="10095-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10095-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="10095-114">Attributes</span></span>

|<span data-ttu-id="10095-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="10095-115">**Attribute**</span></span>|<span data-ttu-id="10095-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="10095-116">**Type**</span></span>|<span data-ttu-id="10095-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="10095-117">**Required**</span></span>|<span data-ttu-id="10095-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="10095-118">**Description**</span></span>|<span data-ttu-id="10095-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="10095-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="10095-120">PageID</span><span class="sxs-lookup"><span data-stu-id="10095-120">PageID</span></span>  <br/> |<span data-ttu-id="10095-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="10095-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10095-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="10095-122">required</span></span>  <br/> ||<span data-ttu-id="10095-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="10095-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="10095-124">RowID</span><span class="sxs-lookup"><span data-stu-id="10095-124">RowID</span></span>  <br/> |<span data-ttu-id="10095-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="10095-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10095-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="10095-126">required</span></span>  <br/> ||<span data-ttu-id="10095-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="10095-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="10095-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="10095-128">ShapeID</span></span>  <br/> |<span data-ttu-id="10095-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="10095-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10095-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="10095-130">required</span></span>  <br/> ||<span data-ttu-id="10095-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="10095-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

