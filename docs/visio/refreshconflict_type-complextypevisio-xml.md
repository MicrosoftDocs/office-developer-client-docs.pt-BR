---
title: RefreshConflict_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 7b52bc87af213e9c26f4bc359adf6cf900b34957
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542825"
---
# <a name="refreshconflict_type-complextype-visio-xml"></a><span data-ttu-id="f20a5-102">RefreshConflict_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="f20a5-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f20a5-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f20a5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f20a5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f20a5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f20a5-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f20a5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f20a5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f20a5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f20a5-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f20a5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f20a5-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f20a5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f20a5-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f20a5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f20a5-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f20a5-110">Elements and attributes</span></span>

<span data-ttu-id="f20a5-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f20a5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f20a5-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f20a5-112">Child elements</span></span>

<span data-ttu-id="f20a5-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f20a5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f20a5-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f20a5-114">Attributes</span></span>

|<span data-ttu-id="f20a5-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f20a5-115">**Attribute**</span></span>|<span data-ttu-id="f20a5-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f20a5-116">**Type**</span></span>|<span data-ttu-id="f20a5-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f20a5-117">**Required**</span></span>|<span data-ttu-id="f20a5-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f20a5-118">**Description**</span></span>|<span data-ttu-id="f20a5-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f20a5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f20a5-120">PageID</span><span class="sxs-lookup"><span data-stu-id="f20a5-120">PageID</span></span>  <br/> |<span data-ttu-id="f20a5-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f20a5-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f20a5-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f20a5-122">required</span></span>  <br/> ||<span data-ttu-id="f20a5-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f20a5-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f20a5-124">RowID</span><span class="sxs-lookup"><span data-stu-id="f20a5-124">RowID</span></span>  <br/> |<span data-ttu-id="f20a5-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f20a5-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f20a5-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f20a5-126">required</span></span>  <br/> ||<span data-ttu-id="f20a5-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f20a5-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f20a5-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="f20a5-128">ShapeID</span></span>  <br/> |<span data-ttu-id="f20a5-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f20a5-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f20a5-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f20a5-130">required</span></span>  <br/> ||<span data-ttu-id="f20a5-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f20a5-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

