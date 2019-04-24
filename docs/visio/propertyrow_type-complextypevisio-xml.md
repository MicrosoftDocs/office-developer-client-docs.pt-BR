---
title: PropertyRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 813d6dee-b113-c0c9-3f53-c5bfd05b92f2
ms.openlocfilehash: fc59e95c8bb95932dd181b40a2e60dc6a3dac485
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326842"
---
# <a name="propertyrowtype-complextype-visio-xml"></a><span data-ttu-id="9fb4e-102">PropertyRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9fb4e-102">PropertyRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9fb4e-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="9fb4e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fb4e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9fb4e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9fb4e-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9fb4e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9fb4e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9fb4e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9fb4e-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="9fb4e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9fb4e-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="9fb4e-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fb4e-109">Definição</span><span class="sxs-lookup"><span data-stu-id="9fb4e-109">Definition</span></span>

```XML
          <xs:complexType name="PropertyRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9fb4e-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9fb4e-110">Elements and attributes</span></span>

<span data-ttu-id="9fb4e-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9fb4e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9fb4e-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9fb4e-112">Child elements</span></span>

|<span data-ttu-id="9fb4e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9fb4e-113">**Element**</span></span>|<span data-ttu-id="9fb4e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9fb4e-114">**Type**</span></span>|<span data-ttu-id="9fb4e-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9fb4e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fb4e-116">Cell</span><span class="sxs-lookup"><span data-stu-id="9fb4e-116">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9fb4e-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9fb4e-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9fb4e-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="9fb4e-118">Attributes</span></span>

<span data-ttu-id="9fb4e-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9fb4e-119">None.</span></span>
  

