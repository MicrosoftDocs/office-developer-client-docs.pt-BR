---
title: Extensions_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 1da1418e2256f7750ac2e963bac0f78321233c99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771846"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="0da38-102">Extensions_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="0da38-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0da38-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="0da38-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0da38-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0da38-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0da38-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0da38-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0da38-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0da38-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0da38-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="0da38-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0da38-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0da38-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0da38-109">Definição</span><span class="sxs-lookup"><span data-stu-id="0da38-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0da38-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="0da38-110">Elements and attributes</span></span>

<span data-ttu-id="0da38-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="0da38-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0da38-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0da38-112">Child elements</span></span>

|<span data-ttu-id="0da38-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0da38-113">**Element**</span></span>|<span data-ttu-id="0da38-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0da38-114">**Type**</span></span>|<span data-ttu-id="0da38-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0da38-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0da38-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="0da38-116">CellDef</span></span>](http://msdn.microsoft.com/library/8fb193f0-5c88-6891-1cda-f1df486aabfc%28Office.15%29.aspx) <br/> |[<span data-ttu-id="0da38-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="0da38-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0da38-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="0da38-118">FunctionDef</span></span>](http://msdn.microsoft.com/library/dad99181-c14c-cce7-3883-106fe05f20a6%28Office.15%29.aspx) <br/> |[<span data-ttu-id="0da38-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="0da38-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0da38-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="0da38-120">SectionDef</span></span>](http://msdn.microsoft.com/library/751da480-f387-4c68-6699-8948271c23ac%28Office.15%29.aspx) <br/> |[<span data-ttu-id="0da38-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="0da38-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0da38-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="0da38-122">Attributes</span></span>

<span data-ttu-id="0da38-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0da38-123">None.</span></span>
  

