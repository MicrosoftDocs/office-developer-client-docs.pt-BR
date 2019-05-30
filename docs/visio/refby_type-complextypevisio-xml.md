---
title: RefBy_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 7970ae735f4933f05e71f1758912d3ecd382bf89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538274"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="ef2ed-102">RefBy_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="ef2ed-102">RefBy_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ef2ed-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="ef2ed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef2ed-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ef2ed-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ef2ed-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ef2ed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ef2ed-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ef2ed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ef2ed-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="ef2ed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ef2ed-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ef2ed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef2ed-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ef2ed-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ef2ed-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ef2ed-110">Elements and attributes</span></span>

<span data-ttu-id="ef2ed-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ef2ed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ef2ed-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ef2ed-112">Child elements</span></span>

<span data-ttu-id="ef2ed-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ef2ed-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef2ed-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef2ed-114">Attributes</span></span>

|<span data-ttu-id="ef2ed-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ef2ed-115">**Attribute**</span></span>|<span data-ttu-id="ef2ed-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ef2ed-116">**Type**</span></span>|<span data-ttu-id="ef2ed-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ef2ed-117">**Required**</span></span>|<span data-ttu-id="ef2ed-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ef2ed-118">**Description**</span></span>|<span data-ttu-id="ef2ed-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ef2ed-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ef2ed-120">ID</span><span class="sxs-lookup"><span data-stu-id="ef2ed-120">ID</span></span>  <br/> |<span data-ttu-id="ef2ed-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ef2ed-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ef2ed-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ef2ed-122">required</span></span>  <br/> ||<span data-ttu-id="ef2ed-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ef2ed-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ef2ed-124">T</span><span class="sxs-lookup"><span data-stu-id="ef2ed-124">T</span></span>  <br/> |<span data-ttu-id="ef2ed-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ef2ed-125">xsd:string</span></span>  <br/> |<span data-ttu-id="ef2ed-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ef2ed-126">required</span></span>  <br/> ||<span data-ttu-id="ef2ed-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ef2ed-127">Values of the xsd:string type.</span></span>  <br/> |
   

