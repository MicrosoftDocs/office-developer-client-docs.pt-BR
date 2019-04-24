---
title: Validation_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 6f751db1566e39d919fd0a456d3aab72559ceeba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332792"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="7d1fa-102">Validation_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7d1fa-102">Validation_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7d1fa-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="7d1fa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d1fa-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7d1fa-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7d1fa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7d1fa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7d1fa-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7d1fa-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7d1fa-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7d1fa-109">Definição</span><span class="sxs-lookup"><span data-stu-id="7d1fa-109">Definition</span></span>

```XML
          <xs:complexType name="Validation_Type">
          
          <xs:sequence>
    <xs:element name="ValidationProperties"  type="ValidationProperties_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleSets"  type="RuleSets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Issues"  type="Issues_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7d1fa-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7d1fa-110">Elements and attributes</span></span>

<span data-ttu-id="7d1fa-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7d1fa-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7d1fa-112">Child elements</span></span>

|<span data-ttu-id="7d1fa-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-113">**Element**</span></span>|<span data-ttu-id="7d1fa-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-114">**Type**</span></span>|<span data-ttu-id="7d1fa-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7d1fa-116">Issues</span><span class="sxs-lookup"><span data-stu-id="7d1fa-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7d1fa-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="7d1fa-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7d1fa-118">RuleSets</span><span class="sxs-lookup"><span data-stu-id="7d1fa-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7d1fa-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="7d1fa-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7d1fa-120">Validationproperties</span><span class="sxs-lookup"><span data-stu-id="7d1fa-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7d1fa-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="7d1fa-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7d1fa-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d1fa-122">Attributes</span></span>

<span data-ttu-id="7d1fa-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-123">None.</span></span>
  

