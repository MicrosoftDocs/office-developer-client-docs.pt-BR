---
title: Property_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: ada20c601fcd42bf551a0aea63787aac96062816
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383769"
---
# <a name="propertytype-complextype-visio-xml"></a><span data-ttu-id="5ffc1-102">Property_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="5ffc1-102">Property_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5ffc1-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="5ffc1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ffc1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5ffc1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5ffc1-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5ffc1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5ffc1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5ffc1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5ffc1-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="5ffc1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5ffc1-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="5ffc1-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5ffc1-109">Definição</span><span class="sxs-lookup"><span data-stu-id="5ffc1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5ffc1-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5ffc1-110">Elements and attributes</span></span>

<span data-ttu-id="5ffc1-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5ffc1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5ffc1-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5ffc1-112">Child elements</span></span>

|<span data-ttu-id="5ffc1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5ffc1-113">**Element**</span></span>|<span data-ttu-id="5ffc1-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5ffc1-114">**Type**</span></span>|<span data-ttu-id="5ffc1-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5ffc1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5ffc1-116">Row</span><span class="sxs-lookup"><span data-stu-id="5ffc1-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="5ffc1-117">PropertyRow_Type</span><span class="sxs-lookup"><span data-stu-id="5ffc1-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5ffc1-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="5ffc1-118">Attributes</span></span>

<span data-ttu-id="5ffc1-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5ffc1-119">None.</span></span>
  

