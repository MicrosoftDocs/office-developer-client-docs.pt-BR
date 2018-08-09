---
title: RefreshConflict_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 44910cd305b484771ca3d4f4d49ef8a09a6fc2dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772670"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="feede-102">RefreshConflict_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="feede-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="feede-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="feede-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="feede-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="feede-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="feede-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="feede-105">**Schema file**</span></span> <br/> |<span data-ttu-id="feede-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="feede-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="feede-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="feede-107">**Extension base**</span></span> <br/> |<span data-ttu-id="feede-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="feede-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="feede-109">Definição</span><span class="sxs-lookup"><span data-stu-id="feede-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="feede-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="feede-110">Elements and attributes</span></span>

<span data-ttu-id="feede-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="feede-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="feede-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="feede-112">Child elements</span></span>

<span data-ttu-id="feede-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="feede-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="feede-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="feede-114">Attributes</span></span>

|<span data-ttu-id="feede-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="feede-115">**Attribute**</span></span>|<span data-ttu-id="feede-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="feede-116">**Type**</span></span>|<span data-ttu-id="feede-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="feede-117">**Required**</span></span>|<span data-ttu-id="feede-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="feede-118">**Description**</span></span>|<span data-ttu-id="feede-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="feede-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="feede-120">PageID</span><span class="sxs-lookup"><span data-stu-id="feede-120">PageID</span></span>  <br/> |<span data-ttu-id="feede-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="feede-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="feede-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="feede-122">required</span></span>  <br/> ||<span data-ttu-id="feede-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="feede-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="feede-124">RowID</span><span class="sxs-lookup"><span data-stu-id="feede-124">RowID</span></span>  <br/> |<span data-ttu-id="feede-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="feede-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="feede-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="feede-126">required</span></span>  <br/> ||<span data-ttu-id="feede-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="feede-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="feede-128">Identificação da forma</span><span class="sxs-lookup"><span data-stu-id="feede-128">ShapeID</span></span>  <br/> |<span data-ttu-id="feede-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="feede-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="feede-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="feede-130">required</span></span>  <br/> ||<span data-ttu-id="feede-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="feede-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

