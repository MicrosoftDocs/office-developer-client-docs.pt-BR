---
title: RelCubBezTo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 004dc563-d089-230f-0055-038b72eebbed
ms.openlocfilehash: 6ec426ef2c7afd913d904c8ceba938549727c799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319961"
---
# <a name="relcubbeztotype-complextype-visio-xml"></a><span data-ttu-id="3eb46-102">RelCubBezTo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3eb46-102">RelCubBezTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3eb46-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="3eb46-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3eb46-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3eb46-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3eb46-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3eb46-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3eb46-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3eb46-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3eb46-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="3eb46-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3eb46-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="3eb46-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3eb46-109">Definição</span><span class="sxs-lookup"><span data-stu-id="3eb46-109">Definition</span></span>

```XML
          <xs:complexType name="RelCubBezTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="3eb46-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3eb46-110">Elements and attributes</span></span>

<span data-ttu-id="3eb46-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3eb46-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3eb46-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3eb46-112">Child elements</span></span>

|<span data-ttu-id="3eb46-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3eb46-113">**Element**</span></span>|<span data-ttu-id="3eb46-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3eb46-114">**Type**</span></span>|<span data-ttu-id="3eb46-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3eb46-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3eb46-116">Cell</span><span class="sxs-lookup"><span data-stu-id="3eb46-116">Cell</span></span>](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="3eb46-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="3eb46-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3eb46-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="3eb46-118">Attributes</span></span>

<span data-ttu-id="3eb46-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="3eb46-119">None.</span></span>
  

