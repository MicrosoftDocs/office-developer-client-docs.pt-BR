---
title: FillGradient_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82545cdc-890d-1b2f-9c8f-4740f32d0ed7
ms.openlocfilehash: 83e8eef809f566bb2a69e5b2da1d1c5d932ce54c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539639"
---
# <a name="fillgradient_type-complextype-visio-xml"></a><span data-ttu-id="e54e1-102">FillGradient_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="e54e1-102">FillGradient_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e54e1-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="e54e1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e54e1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e54e1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e54e1-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e54e1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e54e1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e54e1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e54e1-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="e54e1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e54e1-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="e54e1-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e54e1-109">Definição</span><span class="sxs-lookup"><span data-stu-id="e54e1-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FillGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e54e1-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="e54e1-110">Elements and attributes</span></span>

<span data-ttu-id="e54e1-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="e54e1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e54e1-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e54e1-112">Child elements</span></span>

|<span data-ttu-id="e54e1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e54e1-113">**Element**</span></span>|<span data-ttu-id="e54e1-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e54e1-114">**Type**</span></span>|<span data-ttu-id="e54e1-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e54e1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e54e1-116">Row</span><span class="sxs-lookup"><span data-stu-id="e54e1-116">Row</span></span>](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e54e1-117">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="e54e1-117">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e54e1-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="e54e1-118">Attributes</span></span>

<span data-ttu-id="e54e1-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e54e1-119">None.</span></span>
  

