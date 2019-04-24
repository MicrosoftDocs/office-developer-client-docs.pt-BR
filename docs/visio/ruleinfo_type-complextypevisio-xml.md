---
title: RuleInfo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360463"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="a2017-102">RuleInfo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a2017-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a2017-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="a2017-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2017-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a2017-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a2017-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a2017-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a2017-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a2017-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a2017-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="a2017-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a2017-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a2017-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a2017-109">Definição</span><span class="sxs-lookup"><span data-stu-id="a2017-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a2017-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a2017-110">Elements and attributes</span></span>

<span data-ttu-id="a2017-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a2017-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a2017-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a2017-112">Child elements</span></span>

<span data-ttu-id="a2017-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a2017-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2017-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="a2017-114">Attributes</span></span>

|<span data-ttu-id="a2017-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a2017-115">**Attribute**</span></span>|<span data-ttu-id="a2017-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a2017-116">**Type**</span></span>|<span data-ttu-id="a2017-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a2017-117">**Required**</span></span>|<span data-ttu-id="a2017-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2017-118">**Description**</span></span>|<span data-ttu-id="a2017-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="a2017-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a2017-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="a2017-120">RuleID</span></span>  <br/> |<span data-ttu-id="a2017-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2017-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2017-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a2017-122">required</span></span>  <br/> ||<span data-ttu-id="a2017-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2017-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2017-124">RuleSetid</span><span class="sxs-lookup"><span data-stu-id="a2017-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="a2017-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2017-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2017-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="a2017-126">required</span></span>  <br/> ||<span data-ttu-id="a2017-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a2017-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

