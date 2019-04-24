---
title: ColorEntry_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: c5f2cafba60cd8157f80dc548cea328d179e74db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358776"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="c4eab-102">ColorEntry_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c4eab-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c4eab-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="c4eab-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4eab-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c4eab-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c4eab-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c4eab-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c4eab-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c4eab-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c4eab-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="c4eab-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c4eab-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c4eab-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4eab-109">Definição</span><span class="sxs-lookup"><span data-stu-id="c4eab-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c4eab-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c4eab-110">Elements and attributes</span></span>

<span data-ttu-id="c4eab-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c4eab-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c4eab-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c4eab-112">Child elements</span></span>

<span data-ttu-id="c4eab-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c4eab-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4eab-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4eab-114">Attributes</span></span>

|<span data-ttu-id="c4eab-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c4eab-115">**Attribute**</span></span>|<span data-ttu-id="c4eab-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c4eab-116">**Type**</span></span>|<span data-ttu-id="c4eab-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c4eab-117">**Required**</span></span>|<span data-ttu-id="c4eab-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c4eab-118">**Description**</span></span>|<span data-ttu-id="c4eab-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c4eab-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c4eab-120">IX</span><span class="sxs-lookup"><span data-stu-id="c4eab-120">IX</span></span>  <br/> |<span data-ttu-id="c4eab-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c4eab-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c4eab-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c4eab-122">required</span></span>  <br/> ||<span data-ttu-id="c4eab-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c4eab-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c4eab-124">RGB</span><span class="sxs-lookup"><span data-stu-id="c4eab-124">RGB</span></span>  <br/> |<span data-ttu-id="c4eab-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c4eab-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c4eab-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c4eab-126">required</span></span>  <br/> ||<span data-ttu-id="c4eab-127">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c4eab-127">Values of the xsd:string type.</span></span>  <br/> |
   

