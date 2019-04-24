---
title: RuleSets_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9bd05541-7cd8-321b-8dd6-fa885c269057
ms.openlocfilehash: 41172a4f15b0d9038fd0ffb0c0a7d8c3d4078798
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319037"
---
# <a name="rulesetstype-complextype-visio-xml"></a><span data-ttu-id="4c193-102">RuleSets_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4c193-102">RuleSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4c193-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="4c193-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c193-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4c193-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4c193-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4c193-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4c193-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4c193-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4c193-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="4c193-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4c193-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4c193-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4c193-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4c193-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSets_Type">
          
          <xs:sequence>
    <xs:element name="RuleSet"  type="RuleSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4c193-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4c193-110">Elements and attributes</span></span>

<span data-ttu-id="4c193-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4c193-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4c193-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4c193-112">Child elements</span></span>

|<span data-ttu-id="4c193-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4c193-113">**Element**</span></span>|<span data-ttu-id="4c193-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4c193-114">**Type**</span></span>|<span data-ttu-id="4c193-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4c193-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4c193-116">RuleSet</span><span class="sxs-lookup"><span data-stu-id="4c193-116">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4c193-117">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="4c193-117">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4c193-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c193-118">Attributes</span></span>

<span data-ttu-id="4c193-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4c193-119">None.</span></span>
  

