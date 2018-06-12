---
title: Validation_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 26e7dec4ea54e118afd85ec25f334e69849a57dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773247"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="4070f-102">Validation_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4070f-102">Validation_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4070f-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="4070f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4070f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4070f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4070f-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4070f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4070f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4070f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4070f-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="4070f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4070f-108">None</span><span class="sxs-lookup"><span data-stu-id="4070f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4070f-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4070f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4070f-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4070f-110">Elements and attributes</span></span>

<span data-ttu-id="4070f-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4070f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4070f-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4070f-112">Child elements</span></span>

|<span data-ttu-id="4070f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4070f-113">**Element**</span></span>|<span data-ttu-id="4070f-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4070f-114">**Type**</span></span>|<span data-ttu-id="4070f-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4070f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4070f-116">Problemas</span><span class="sxs-lookup"><span data-stu-id="4070f-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4070f-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="4070f-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4070f-118">RuleSets</span><span class="sxs-lookup"><span data-stu-id="4070f-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4070f-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="4070f-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4070f-120">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="4070f-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4070f-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="4070f-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4070f-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="4070f-122">Attributes</span></span>

<span data-ttu-id="4070f-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4070f-123">None.</span></span>
  

