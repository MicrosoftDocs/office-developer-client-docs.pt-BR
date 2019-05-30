---
title: CharacterRow_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61c99712-d451-408a-de15-fb088605b07c
ms.openlocfilehash: 3d54921ca571ff3ba4643b2e1d18ee9d7d1bc8c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540193"
---
# <a name="characterrowtype-complextype-visio-xml"></a><span data-ttu-id="2d119-102">CharacterRow_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="2d119-102">CharacterRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2d119-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="2d119-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d119-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2d119-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2d119-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2d119-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2d119-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2d119-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2d119-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="2d119-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2d119-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="2d119-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2d119-109">Definição</span><span class="sxs-lookup"><span data-stu-id="2d119-109">Definition</span></span>

```XML
          <xs:complexType name="CharacterRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="2d119-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2d119-110">Elements and attributes</span></span>

<span data-ttu-id="2d119-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2d119-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2d119-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2d119-112">Child elements</span></span>

|<span data-ttu-id="2d119-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2d119-113">**Element**</span></span>|<span data-ttu-id="2d119-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2d119-114">**Type**</span></span>|<span data-ttu-id="2d119-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2d119-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2d119-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2d119-116">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2d119-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2d119-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2d119-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="2d119-118">Attributes</span></span>

<span data-ttu-id="2d119-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2d119-119">None.</span></span>
  

