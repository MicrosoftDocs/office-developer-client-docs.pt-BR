---
title: RowMap_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 18f573a480e3ae057074a219def192f6b1b2829b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772799"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="91910-102">RowMap_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="91910-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="91910-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="91910-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91910-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="91910-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="91910-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="91910-105">**Schema file**</span></span> <br/> |<span data-ttu-id="91910-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="91910-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="91910-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="91910-107">**Extension base**</span></span> <br/> |<span data-ttu-id="91910-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="91910-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91910-109">Definição</span><span class="sxs-lookup"><span data-stu-id="91910-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="91910-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="91910-110">Elements and attributes</span></span>

<span data-ttu-id="91910-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="91910-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="91910-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="91910-112">Child elements</span></span>

<span data-ttu-id="91910-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="91910-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91910-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="91910-114">Attributes</span></span>

|<span data-ttu-id="91910-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="91910-115">**Attribute**</span></span>|<span data-ttu-id="91910-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="91910-116">**Type**</span></span>|<span data-ttu-id="91910-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="91910-117">**Required**</span></span>|<span data-ttu-id="91910-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="91910-118">**Description**</span></span>|<span data-ttu-id="91910-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="91910-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="91910-120">PageID</span><span class="sxs-lookup"><span data-stu-id="91910-120">PageID</span></span>  <br/> |<span data-ttu-id="91910-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="91910-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="91910-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="91910-122">required</span></span>  <br/> ||<span data-ttu-id="91910-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="91910-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="91910-124">RowID</span><span class="sxs-lookup"><span data-stu-id="91910-124">RowID</span></span>  <br/> |<span data-ttu-id="91910-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="91910-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="91910-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="91910-126">required</span></span>  <br/> ||<span data-ttu-id="91910-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="91910-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="91910-128">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="91910-128">ShapeID</span></span>  <br/> |<span data-ttu-id="91910-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="91910-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="91910-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="91910-130">required</span></span>  <br/> ||<span data-ttu-id="91910-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="91910-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

