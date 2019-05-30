---
title: ColorEntry_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: f5ada3fef8d50c2e53f63c797601980f88349868
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540144"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="06571-102">ColorEntry_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="06571-102">ColorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="06571-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="06571-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06571-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="06571-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="06571-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="06571-105">**Schema file**</span></span> <br/> |<span data-ttu-id="06571-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="06571-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="06571-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="06571-107">**Extension base**</span></span> <br/> |<span data-ttu-id="06571-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="06571-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="06571-109">Definição</span><span class="sxs-lookup"><span data-stu-id="06571-109">Definition</span></span>

```XML
      <xs:complexType name="ColorEntry_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RGB"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="06571-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="06571-110">Elements and attributes</span></span>

<span data-ttu-id="06571-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="06571-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="06571-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="06571-112">Child elements</span></span>

<span data-ttu-id="06571-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="06571-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06571-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="06571-114">Attributes</span></span>

|<span data-ttu-id="06571-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="06571-115">**Attribute**</span></span>|<span data-ttu-id="06571-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="06571-116">**Type**</span></span>|<span data-ttu-id="06571-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="06571-117">**Required**</span></span>|<span data-ttu-id="06571-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="06571-118">**Description**</span></span>|<span data-ttu-id="06571-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="06571-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="06571-120">IX</span><span class="sxs-lookup"><span data-stu-id="06571-120">IX</span></span>  <br/> |<span data-ttu-id="06571-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="06571-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="06571-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="06571-122">required</span></span>  <br/> ||<span data-ttu-id="06571-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="06571-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="06571-124">RGB</span><span class="sxs-lookup"><span data-stu-id="06571-124">RGB</span></span>  <br/> |<span data-ttu-id="06571-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="06571-125">xsd:string</span></span>  <br/> |<span data-ttu-id="06571-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="06571-126">required</span></span>  <br/> ||<span data-ttu-id="06571-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="06571-127">Values of the xsd:string type.</span></span>  <br/> |
   

