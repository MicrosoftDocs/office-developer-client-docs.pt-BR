---
title: EventList_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: bcee61ba9347dc77dd704d0221a9362843bf9858
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540760"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="02d69-102">EventList_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="02d69-102">EventList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="02d69-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="02d69-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02d69-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="02d69-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="02d69-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="02d69-105">**Schema file**</span></span> <br/> |<span data-ttu-id="02d69-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="02d69-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="02d69-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="02d69-107">**Extension base**</span></span> <br/> |<span data-ttu-id="02d69-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="02d69-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02d69-109">Definição</span><span class="sxs-lookup"><span data-stu-id="02d69-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="02d69-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="02d69-110">Elements and attributes</span></span>

<span data-ttu-id="02d69-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="02d69-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="02d69-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="02d69-112">Child elements</span></span>

|<span data-ttu-id="02d69-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02d69-113">**Element**</span></span>|<span data-ttu-id="02d69-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="02d69-114">**Type**</span></span>|<span data-ttu-id="02d69-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="02d69-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02d69-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="02d69-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02d69-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="02d69-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="02d69-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="02d69-118">Attributes</span></span>

<span data-ttu-id="02d69-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="02d69-119">None.</span></span>
  

