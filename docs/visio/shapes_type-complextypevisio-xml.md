---
title: Shapes_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 798af3d68df6c430fffb318e5e19c83aea441ca0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542083"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="71ce1-102">Shapes_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="71ce1-102">Shapes_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="71ce1-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="71ce1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71ce1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="71ce1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="71ce1-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="71ce1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="71ce1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="71ce1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="71ce1-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="71ce1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="71ce1-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="71ce1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="71ce1-109">Definição</span><span class="sxs-lookup"><span data-stu-id="71ce1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="71ce1-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="71ce1-110">Elements and attributes</span></span>

<span data-ttu-id="71ce1-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="71ce1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="71ce1-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="71ce1-112">Child elements</span></span>

|<span data-ttu-id="71ce1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="71ce1-113">**Element**</span></span>|<span data-ttu-id="71ce1-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="71ce1-114">**Type**</span></span>|<span data-ttu-id="71ce1-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="71ce1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71ce1-116">Forma</span><span class="sxs-lookup"><span data-stu-id="71ce1-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="71ce1-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="71ce1-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="71ce1-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="71ce1-118">Attributes</span></span>

<span data-ttu-id="71ce1-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="71ce1-119">None.</span></span>
  

