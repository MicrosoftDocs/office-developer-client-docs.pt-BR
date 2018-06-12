---
title: Shapes_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 707f20823d0413e0b064b2a367da803419889ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772915"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="ad5a0-102">Shapes_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ad5a0-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ad5a0-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="ad5a0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad5a0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad5a0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ad5a0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ad5a0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ad5a0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ad5a0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ad5a0-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="ad5a0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ad5a0-108">None</span><span class="sxs-lookup"><span data-stu-id="ad5a0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad5a0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ad5a0-109">Definition</span></span>

```XML
          <xs:complexType name="Shapes_Type">
          
          <xs:sequence>
    <xs:element name="Shape"  type="ShapeSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad5a0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ad5a0-110">Elements and attributes</span></span>

<span data-ttu-id="ad5a0-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ad5a0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ad5a0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ad5a0-112">Child elements</span></span>

|<span data-ttu-id="ad5a0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad5a0-113">**Element**</span></span>|<span data-ttu-id="ad5a0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad5a0-114">**Type**</span></span>|<span data-ttu-id="ad5a0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ad5a0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad5a0-116">Shape</span><span class="sxs-lookup"><span data-stu-id="ad5a0-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad5a0-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ad5a0-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ad5a0-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad5a0-118">Attributes</span></span>

<span data-ttu-id="ad5a0-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ad5a0-119">None.</span></span>
  

