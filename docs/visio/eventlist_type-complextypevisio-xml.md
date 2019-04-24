---
title: EventList_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 454a54749e9f72cacc3e7359041705d3487b9e79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351020"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="97973-102">EventList_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="97973-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="97973-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="97973-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97973-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="97973-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="97973-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="97973-105">**Schema file**</span></span> <br/> |<span data-ttu-id="97973-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="97973-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="97973-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="97973-107">**Extension base**</span></span> <br/> |<span data-ttu-id="97973-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="97973-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="97973-109">Definição</span><span class="sxs-lookup"><span data-stu-id="97973-109">Definition</span></span>

```XML
          <xs:complexType name="EventList_Type">
          
          <xs:sequence>
    <xs:element name="EventItem"  type="EventItem_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="97973-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="97973-110">Elements and attributes</span></span>

<span data-ttu-id="97973-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="97973-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="97973-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="97973-112">Child elements</span></span>

|<span data-ttu-id="97973-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="97973-113">**Element**</span></span>|<span data-ttu-id="97973-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="97973-114">**Type**</span></span>|<span data-ttu-id="97973-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="97973-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="97973-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="97973-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="97973-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="97973-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="97973-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="97973-118">Attributes</span></span>

<span data-ttu-id="97973-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="97973-119">None.</span></span>
  

