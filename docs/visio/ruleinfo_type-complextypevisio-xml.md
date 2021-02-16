---
title: RuleInfo_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 8e7b04e938997786cf0dc99e92057f77cfe0cf76
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541642"
---
# <a name="ruleinfo_type-complextype-visio-xml"></a><span data-ttu-id="4ceb2-102">RuleInfo_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="4ceb2-102">RuleInfo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4ceb2-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="4ceb2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ceb2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4ceb2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4ceb2-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4ceb2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4ceb2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4ceb2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4ceb2-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="4ceb2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4ceb2-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4ceb2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ceb2-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4ceb2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4ceb2-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4ceb2-110">Elements and attributes</span></span>

<span data-ttu-id="4ceb2-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4ceb2-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4ceb2-112">Child elements</span></span>

<span data-ttu-id="4ceb2-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ceb2-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="4ceb2-114">Attributes</span></span>

|<span data-ttu-id="4ceb2-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4ceb2-115">**Attribute**</span></span>|<span data-ttu-id="4ceb2-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4ceb2-116">**Type**</span></span>|<span data-ttu-id="4ceb2-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4ceb2-117">**Required**</span></span>|<span data-ttu-id="4ceb2-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4ceb2-118">**Description**</span></span>|<span data-ttu-id="4ceb2-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4ceb2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4ceb2-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="4ceb2-120">RuleID</span></span>  <br/> |<span data-ttu-id="4ceb2-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4ceb2-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4ceb2-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4ceb2-122">required</span></span>  <br/> ||<span data-ttu-id="4ceb2-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4ceb2-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="4ceb2-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="4ceb2-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4ceb2-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4ceb2-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4ceb2-126">required</span></span>  <br/> ||<span data-ttu-id="4ceb2-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4ceb2-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

