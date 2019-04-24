---
title: Solutions_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: bf43b971399ec69c6f73cbfaaa6cade8c583d3c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334423"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="834f3-102">Solutions_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="834f3-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="834f3-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="834f3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="834f3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="834f3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="834f3-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="834f3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="834f3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="834f3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="834f3-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="834f3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="834f3-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="834f3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="834f3-109">Definição</span><span class="sxs-lookup"><span data-stu-id="834f3-109">Definition</span></span>

```XML
          <xs:complexType name="Solutions_Type">
          
          <xs:sequence>
    <xs:element name="Solution"  type="Solution_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="834f3-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="834f3-110">Elements and attributes</span></span>

<span data-ttu-id="834f3-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="834f3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="834f3-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="834f3-112">Child elements</span></span>

|<span data-ttu-id="834f3-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="834f3-113">**Element**</span></span>|<span data-ttu-id="834f3-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="834f3-114">**Type**</span></span>|<span data-ttu-id="834f3-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="834f3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="834f3-116">Solution</span><span class="sxs-lookup"><span data-stu-id="834f3-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="834f3-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="834f3-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="834f3-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="834f3-118">Attributes</span></span>

<span data-ttu-id="834f3-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="834f3-119">None.</span></span>
  

