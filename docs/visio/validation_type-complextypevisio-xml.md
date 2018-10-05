---
title: Validation_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 6f751db1566e39d919fd0a456d3aab72559ceeba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385589"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="36e5c-102">Validation_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="36e5c-102">Validation_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="36e5c-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="36e5c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36e5c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="36e5c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="36e5c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="36e5c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="36e5c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="36e5c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="36e5c-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="36e5c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="36e5c-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="36e5c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36e5c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="36e5c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="36e5c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="36e5c-110">Elements and attributes</span></span>

<span data-ttu-id="36e5c-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="36e5c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="36e5c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="36e5c-112">Child elements</span></span>

|<span data-ttu-id="36e5c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="36e5c-113">**Element**</span></span>|<span data-ttu-id="36e5c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="36e5c-114">**Type**</span></span>|<span data-ttu-id="36e5c-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36e5c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="36e5c-116">Problemas</span><span class="sxs-lookup"><span data-stu-id="36e5c-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36e5c-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="36e5c-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="36e5c-118">RuleSets</span><span class="sxs-lookup"><span data-stu-id="36e5c-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36e5c-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="36e5c-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="36e5c-120">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="36e5c-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36e5c-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="36e5c-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="36e5c-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="36e5c-122">Attributes</span></span>

<span data-ttu-id="36e5c-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="36e5c-123">None.</span></span>
  

