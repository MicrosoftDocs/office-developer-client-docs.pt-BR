---
title: RuleInfo_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382565"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="fd75e-102">RuleInfo_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="fd75e-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fd75e-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="fd75e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd75e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fd75e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fd75e-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fd75e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fd75e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fd75e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fd75e-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="fd75e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fd75e-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fd75e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fd75e-109">Definição</span><span class="sxs-lookup"><span data-stu-id="fd75e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fd75e-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fd75e-110">Elements and attributes</span></span>

<span data-ttu-id="fd75e-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fd75e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fd75e-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fd75e-112">Child elements</span></span>

<span data-ttu-id="fd75e-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="fd75e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd75e-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="fd75e-114">Attributes</span></span>

|<span data-ttu-id="fd75e-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="fd75e-115">**Attribute**</span></span>|<span data-ttu-id="fd75e-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fd75e-116">**Type**</span></span>|<span data-ttu-id="fd75e-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="fd75e-117">**Required**</span></span>|<span data-ttu-id="fd75e-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fd75e-118">**Description**</span></span>|<span data-ttu-id="fd75e-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="fd75e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fd75e-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="fd75e-120">RuleID</span></span>  <br/> |<span data-ttu-id="fd75e-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fd75e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fd75e-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="fd75e-122">required</span></span>  <br/> ||<span data-ttu-id="fd75e-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fd75e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fd75e-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="fd75e-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="fd75e-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fd75e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fd75e-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="fd75e-126">required</span></span>  <br/> ||<span data-ttu-id="fd75e-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fd75e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

