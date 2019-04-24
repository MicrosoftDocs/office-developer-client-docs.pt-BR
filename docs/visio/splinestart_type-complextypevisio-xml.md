---
title: SplineStart_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4395e39c-51bb-b232-bd8a-c5e53ae95169
ms.openlocfilehash: 963ef696e66861f6f67466446e0c1ea19933029e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329873"
---
# <a name="splinestarttype-complextype-visio-xml"></a><span data-ttu-id="c22c7-102">SplineStart_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c22c7-102">SplineStart_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c22c7-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="c22c7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c22c7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c22c7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c22c7-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c22c7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c22c7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c22c7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c22c7-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="c22c7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c22c7-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="c22c7-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c22c7-109">Definição</span><span class="sxs-lookup"><span data-stu-id="c22c7-109">Definition</span></span>

```XML
          <xs:complexType name="SplineStart_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="c22c7-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c22c7-110">Elements and attributes</span></span>

<span data-ttu-id="c22c7-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c22c7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c22c7-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c22c7-112">Child elements</span></span>

|<span data-ttu-id="c22c7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c22c7-113">**Element**</span></span>|<span data-ttu-id="c22c7-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c22c7-114">**Type**</span></span>|<span data-ttu-id="c22c7-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c22c7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c22c7-116">Cell</span><span class="sxs-lookup"><span data-stu-id="c22c7-116">Cell</span></span>](cell-element-splinestart-rowvisio-xml.md) <br/> |[<span data-ttu-id="c22c7-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c22c7-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c22c7-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="c22c7-118">Attributes</span></span>

<span data-ttu-id="c22c7-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c22c7-119">None.</span></span>
  

