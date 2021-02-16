---
title: Property_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: 1eb2d9f11a264138f5d1a325d31e17789d1c9483
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540732"
---
# <a name="property_type-complextype-visio-xml"></a><span data-ttu-id="1850d-102">Property_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="1850d-102">Property_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1850d-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="1850d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1850d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1850d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1850d-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1850d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1850d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1850d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1850d-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="1850d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1850d-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1850d-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1850d-109">Definição</span><span class="sxs-lookup"><span data-stu-id="1850d-109">Definition</span></span>

```XML
          <xs:complexType name="Property_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="PropertyRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1850d-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1850d-110">Elements and attributes</span></span>

<span data-ttu-id="1850d-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1850d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1850d-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1850d-112">Child elements</span></span>

|<span data-ttu-id="1850d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1850d-113">**Element**</span></span>|<span data-ttu-id="1850d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1850d-114">**Type**</span></span>|<span data-ttu-id="1850d-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1850d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1850d-116">Row</span><span class="sxs-lookup"><span data-stu-id="1850d-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1850d-117">PropertyRow_Type</span><span class="sxs-lookup"><span data-stu-id="1850d-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1850d-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1850d-118">Attributes</span></span>

<span data-ttu-id="1850d-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1850d-119">None.</span></span>
  

