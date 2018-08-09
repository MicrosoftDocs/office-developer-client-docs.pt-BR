---
title: SplineKnot_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 114d5460-c5fd-0e31-def4-f943b93bd1ae
ms.openlocfilehash: a6e47f2e75691d4791fa17483efbb74aa01679f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773038"
---
# <a name="splineknottype-complextype-visio-xml"></a><span data-ttu-id="b7547-102">SplineKnot_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="b7547-102">SplineKnot_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b7547-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="b7547-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7547-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b7547-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b7547-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b7547-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b7547-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b7547-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b7547-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="b7547-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b7547-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="b7547-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7547-109">Definição</span><span class="sxs-lookup"><span data-stu-id="b7547-109">Definition</span></span>

```XML
          <xs:complexType name="SplineKnot_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b7547-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b7547-110">Elements and attributes</span></span>

<span data-ttu-id="b7547-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b7547-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b7547-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b7547-112">Child elements</span></span>

|<span data-ttu-id="b7547-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b7547-113">**Element**</span></span>|<span data-ttu-id="b7547-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b7547-114">**Type**</span></span>|<span data-ttu-id="b7547-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b7547-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7547-116">Célula</span><span class="sxs-lookup"><span data-stu-id="b7547-116">Cell</span></span>](cell-element-splineknot-rowvisio-xml.md) <br/> |[<span data-ttu-id="b7547-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b7547-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b7547-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b7547-118">Attributes</span></span>

<span data-ttu-id="b7547-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b7547-119">None.</span></span>
  

