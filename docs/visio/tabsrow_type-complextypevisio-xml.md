---
title: TabsRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b9258a0-05fa-b0b0-90ed-dc1c4faa288a
ms.openlocfilehash: fed6c70119007164113ba76296bed5662e331c17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332428"
---
# <a name="tabsrowtype-complextype-visio-xml"></a><span data-ttu-id="f9857-102">TabsRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f9857-102">TabsRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f9857-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f9857-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9857-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f9857-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f9857-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f9857-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f9857-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f9857-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f9857-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f9857-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f9857-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="f9857-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f9857-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f9857-109">Definition</span></span>

```XML
          <xs:complexType name="TabsRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="f9857-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f9857-110">Elements and attributes</span></span>

<span data-ttu-id="f9857-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f9857-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f9857-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f9857-112">Child elements</span></span>

|<span data-ttu-id="f9857-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f9857-113">**Element**</span></span>|<span data-ttu-id="f9857-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f9857-114">**Type**</span></span>|<span data-ttu-id="f9857-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f9857-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f9857-116">Cell</span><span class="sxs-lookup"><span data-stu-id="f9857-116">Cell</span></span>](cell-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="f9857-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f9857-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f9857-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9857-118">Attributes</span></span>

<span data-ttu-id="f9857-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f9857-119">None.</span></span>
  

