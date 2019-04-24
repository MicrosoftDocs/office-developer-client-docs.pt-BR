---
title: ScratchRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 35ed6fc0-d737-a931-fddb-7bbb770c8d37
ms.openlocfilehash: 74f106f34596ca4ff2c200e0127155f4df54da28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326996"
---
# <a name="scratchrowtype-complextype-visio-xml"></a><span data-ttu-id="5e3cf-102">ScratchRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5e3cf-102">ScratchRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5e3cf-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="5e3cf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e3cf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5e3cf-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5e3cf-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5e3cf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5e3cf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5e3cf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5e3cf-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="5e3cf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5e3cf-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="5e3cf-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5e3cf-109">Definição</span><span class="sxs-lookup"><span data-stu-id="5e3cf-109">Definition</span></span>

```XML
          <xs:complexType name="ScratchRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="5e3cf-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5e3cf-110">Elements and attributes</span></span>

<span data-ttu-id="5e3cf-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5e3cf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5e3cf-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5e3cf-112">Child elements</span></span>

|<span data-ttu-id="5e3cf-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5e3cf-113">**Element**</span></span>|<span data-ttu-id="5e3cf-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5e3cf-114">**Type**</span></span>|<span data-ttu-id="5e3cf-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5e3cf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5e3cf-116">Cell</span><span class="sxs-lookup"><span data-stu-id="5e3cf-116">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="5e3cf-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5e3cf-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5e3cf-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e3cf-118">Attributes</span></span>

<span data-ttu-id="5e3cf-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5e3cf-119">None.</span></span>
  

