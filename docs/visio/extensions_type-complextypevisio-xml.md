---
title: Extensions_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 7760e1b22a7d573d8f61cf08ed54789f601e9339
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398133"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="9352a-102">Extensions_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9352a-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9352a-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="9352a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9352a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9352a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9352a-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9352a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9352a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9352a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9352a-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="9352a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9352a-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9352a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9352a-109">Definição</span><span class="sxs-lookup"><span data-stu-id="9352a-109">Definition</span></span>

```XML
          <xs:complexType name="Extensions_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="FunctionDef"  type="FunctionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="SectionDef"  type="SectionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9352a-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9352a-110">Elements and attributes</span></span>

<span data-ttu-id="9352a-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9352a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9352a-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9352a-112">Child elements</span></span>

|<span data-ttu-id="9352a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9352a-113">**Element**</span></span>|<span data-ttu-id="9352a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9352a-114">**Type**</span></span>|<span data-ttu-id="9352a-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9352a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9352a-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="9352a-116">CellDef</span></span> <br/> |[<span data-ttu-id="9352a-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="9352a-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="9352a-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="9352a-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="9352a-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="9352a-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="9352a-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="9352a-120">SectionDef</span></span> <br/> |[<span data-ttu-id="9352a-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="9352a-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9352a-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="9352a-122">Attributes</span></span>

<span data-ttu-id="9352a-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9352a-123">None.</span></span>
  

