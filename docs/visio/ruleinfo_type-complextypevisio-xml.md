---
title: RuleInfo_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0a0ac32729b83a5d648b2826bffe5a9df4d9fc0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772808"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="bd0b2-102">RuleInfo_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="bd0b2-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bd0b2-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="bd0b2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd0b2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bd0b2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bd0b2-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bd0b2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bd0b2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bd0b2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bd0b2-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="bd0b2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bd0b2-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bd0b2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bd0b2-109">Definição</span><span class="sxs-lookup"><span data-stu-id="bd0b2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bd0b2-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="bd0b2-110">Elements and attributes</span></span>

<span data-ttu-id="bd0b2-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="bd0b2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bd0b2-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bd0b2-112">Child elements</span></span>

<span data-ttu-id="bd0b2-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="bd0b2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd0b2-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="bd0b2-114">Attributes</span></span>

|<span data-ttu-id="bd0b2-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bd0b2-115">**Attribute**</span></span>|<span data-ttu-id="bd0b2-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bd0b2-116">**Type**</span></span>|<span data-ttu-id="bd0b2-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="bd0b2-117">**Required**</span></span>|<span data-ttu-id="bd0b2-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bd0b2-118">**Description**</span></span>|<span data-ttu-id="bd0b2-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="bd0b2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bd0b2-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="bd0b2-120">RuleID</span></span>  <br/> |<span data-ttu-id="bd0b2-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd0b2-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd0b2-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bd0b2-122">required</span></span>  <br/> ||<span data-ttu-id="bd0b2-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bd0b2-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bd0b2-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="bd0b2-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="bd0b2-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd0b2-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd0b2-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="bd0b2-126">required</span></span>  <br/> ||<span data-ttu-id="bd0b2-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bd0b2-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

