---
title: RowMap_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 8564f5a063ac2365de50919168df0b84e8ae100a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538771"
---
# <a name="rowmap_type-complextype-visio-xml"></a><span data-ttu-id="3ef6c-102">RowMap_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="3ef6c-102">RowMap_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3ef6c-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="3ef6c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ef6c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3ef6c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3ef6c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3ef6c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3ef6c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3ef6c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3ef6c-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="3ef6c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3ef6c-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3ef6c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ef6c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="3ef6c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3ef6c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3ef6c-110">Elements and attributes</span></span>

<span data-ttu-id="3ef6c-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3ef6c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3ef6c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3ef6c-112">Child elements</span></span>

<span data-ttu-id="3ef6c-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="3ef6c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ef6c-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ef6c-114">Attributes</span></span>

|<span data-ttu-id="3ef6c-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3ef6c-115">**Attribute**</span></span>|<span data-ttu-id="3ef6c-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3ef6c-116">**Type**</span></span>|<span data-ttu-id="3ef6c-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3ef6c-117">**Required**</span></span>|<span data-ttu-id="3ef6c-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3ef6c-118">**Description**</span></span>|<span data-ttu-id="3ef6c-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3ef6c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3ef6c-120">PageID</span><span class="sxs-lookup"><span data-stu-id="3ef6c-120">PageID</span></span>  <br/> |<span data-ttu-id="3ef6c-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3ef6c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3ef6c-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3ef6c-122">required</span></span>  <br/> ||<span data-ttu-id="3ef6c-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3ef6c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3ef6c-124">RowID</span><span class="sxs-lookup"><span data-stu-id="3ef6c-124">RowID</span></span>  <br/> |<span data-ttu-id="3ef6c-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3ef6c-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3ef6c-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3ef6c-126">required</span></span>  <br/> ||<span data-ttu-id="3ef6c-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3ef6c-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3ef6c-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="3ef6c-128">ShapeID</span></span>  <br/> |<span data-ttu-id="3ef6c-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3ef6c-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3ef6c-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3ef6c-130">required</span></span>  <br/> ||<span data-ttu-id="3ef6c-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3ef6c-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

