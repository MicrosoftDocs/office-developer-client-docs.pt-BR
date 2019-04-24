---
title: Scratch_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e3dd8c8-e84c-61ff-bfff-57d97545e441
ms.openlocfilehash: 4002466eb98beac889fb27b2aec07aa6a5e31ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335543"
---
# <a name="scratchtype-complextype-visio-xml"></a><span data-ttu-id="b5501-102">Scratch_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b5501-102">Scratch_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b5501-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="b5501-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5501-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5501-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b5501-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b5501-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b5501-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b5501-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b5501-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="b5501-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b5501-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="b5501-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5501-109">Definição</span><span class="sxs-lookup"><span data-stu-id="b5501-109">Definition</span></span>

```XML
          <xs:complexType name="Scratch_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ScratchRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5501-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b5501-110">Elements and attributes</span></span>

<span data-ttu-id="b5501-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b5501-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b5501-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b5501-112">Child elements</span></span>

|<span data-ttu-id="b5501-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b5501-113">**Element**</span></span>|<span data-ttu-id="b5501-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5501-114">**Type**</span></span>|<span data-ttu-id="b5501-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b5501-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5501-116">Row</span><span class="sxs-lookup"><span data-stu-id="b5501-116">Row</span></span>](row-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="b5501-117">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="b5501-117">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b5501-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5501-118">Attributes</span></span>

<span data-ttu-id="b5501-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b5501-119">None.</span></span>
  

