---
title: Shapes_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 7d028939ad6c99ecf4160b95764c86779c399c8e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397608"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="81578-102">Shapes_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="81578-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="81578-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="81578-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81578-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="81578-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="81578-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="81578-105">**Schema file**</span></span> <br/> |<span data-ttu-id="81578-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="81578-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="81578-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="81578-107">**Extension base**</span></span> <br/> |<span data-ttu-id="81578-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="81578-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="81578-109">Definição</span><span class="sxs-lookup"><span data-stu-id="81578-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="81578-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="81578-110">Elements and attributes</span></span>

<span data-ttu-id="81578-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="81578-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="81578-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="81578-112">Child elements</span></span>

|<span data-ttu-id="81578-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="81578-113">**Element**</span></span>|<span data-ttu-id="81578-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="81578-114">**Type**</span></span>|<span data-ttu-id="81578-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="81578-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="81578-116">Shape</span><span class="sxs-lookup"><span data-stu-id="81578-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="81578-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="81578-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="81578-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="81578-118">Attributes</span></span>

<span data-ttu-id="81578-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="81578-119">None.</span></span>
  

