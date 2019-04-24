---
title: RefreshConflict_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 25c83a8168744820fa8b570dc37bda0547ab4ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346477"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="eb490-102">RefreshConflict_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="eb490-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="eb490-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="eb490-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb490-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="eb490-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="eb490-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="eb490-105">**Schema file**</span></span> <br/> |<span data-ttu-id="eb490-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="eb490-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="eb490-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="eb490-107">**Extension base**</span></span> <br/> |<span data-ttu-id="eb490-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="eb490-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eb490-109">Definição</span><span class="sxs-lookup"><span data-stu-id="eb490-109">Definition</span></span>

```XML
      <xs:complexType name="RefreshConflict_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="eb490-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="eb490-110">Elements and attributes</span></span>

<span data-ttu-id="eb490-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="eb490-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eb490-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="eb490-112">Child elements</span></span>

<span data-ttu-id="eb490-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="eb490-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb490-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb490-114">Attributes</span></span>

|<span data-ttu-id="eb490-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="eb490-115">**Attribute**</span></span>|<span data-ttu-id="eb490-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="eb490-116">**Type**</span></span>|<span data-ttu-id="eb490-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="eb490-117">**Required**</span></span>|<span data-ttu-id="eb490-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="eb490-118">**Description**</span></span>|<span data-ttu-id="eb490-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="eb490-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eb490-120">PageID</span><span class="sxs-lookup"><span data-stu-id="eb490-120">PageID</span></span>  <br/> |<span data-ttu-id="eb490-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eb490-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eb490-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="eb490-122">required</span></span>  <br/> ||<span data-ttu-id="eb490-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eb490-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eb490-124">RowID</span><span class="sxs-lookup"><span data-stu-id="eb490-124">RowID</span></span>  <br/> |<span data-ttu-id="eb490-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eb490-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eb490-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="eb490-126">required</span></span>  <br/> ||<span data-ttu-id="eb490-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eb490-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eb490-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="eb490-128">ShapeID</span></span>  <br/> |<span data-ttu-id="eb490-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eb490-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eb490-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="eb490-130">required</span></span>  <br/> ||<span data-ttu-id="eb490-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eb490-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

