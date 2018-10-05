---
title: RowMap_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400996"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="2b295-102">RowMap_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="2b295-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2b295-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="2b295-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b295-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2b295-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2b295-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2b295-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2b295-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2b295-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2b295-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="2b295-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2b295-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2b295-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b295-109">Definição</span><span class="sxs-lookup"><span data-stu-id="2b295-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2b295-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2b295-110">Elements and attributes</span></span>

<span data-ttu-id="2b295-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2b295-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2b295-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2b295-112">Child elements</span></span>

<span data-ttu-id="2b295-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2b295-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b295-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2b295-114">Attributes</span></span>

|<span data-ttu-id="2b295-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2b295-115">**Attribute**</span></span>|<span data-ttu-id="2b295-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2b295-116">**Type**</span></span>|<span data-ttu-id="2b295-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2b295-117">**Required**</span></span>|<span data-ttu-id="2b295-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2b295-118">**Description**</span></span>|<span data-ttu-id="2b295-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2b295-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2b295-120">PageID</span><span class="sxs-lookup"><span data-stu-id="2b295-120">PageID</span></span>  <br/> |<span data-ttu-id="2b295-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2b295-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2b295-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2b295-122">required</span></span>  <br/> ||<span data-ttu-id="2b295-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2b295-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2b295-124">RowID</span><span class="sxs-lookup"><span data-stu-id="2b295-124">RowID</span></span>  <br/> |<span data-ttu-id="2b295-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2b295-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2b295-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2b295-126">required</span></span>  <br/> ||<span data-ttu-id="2b295-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2b295-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2b295-128">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="2b295-128">ShapeID</span></span>  <br/> |<span data-ttu-id="2b295-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2b295-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2b295-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2b295-130">required</span></span>  <br/> ||<span data-ttu-id="2b295-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2b295-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

