---
title: EventList_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 7bbb8d1074d869a9171a188118c920260b3a903d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771827"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="05772-102">EventList_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="05772-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="05772-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="05772-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05772-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="05772-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="05772-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="05772-105">**Schema file**</span></span> <br/> |<span data-ttu-id="05772-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="05772-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="05772-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="05772-107">**Extension base**</span></span> <br/> |<span data-ttu-id="05772-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="05772-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="05772-109">Definição</span><span class="sxs-lookup"><span data-stu-id="05772-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="05772-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="05772-110">Elements and attributes</span></span>

<span data-ttu-id="05772-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="05772-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="05772-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="05772-112">Child elements</span></span>

|<span data-ttu-id="05772-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="05772-113">**Element**</span></span>|<span data-ttu-id="05772-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="05772-114">**Type**</span></span>|<span data-ttu-id="05772-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="05772-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="05772-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="05772-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05772-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="05772-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="05772-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="05772-118">Attributes</span></span>

<span data-ttu-id="05772-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="05772-119">None.</span></span>
  

