---
title: Colors_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: bddcb93451bfb6d1b519720040a9e3875dc2ec5c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540137"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="0b28b-102">Colors_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="0b28b-102">Colors_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0b28b-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="0b28b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b28b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0b28b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0b28b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0b28b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0b28b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0b28b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0b28b-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="0b28b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0b28b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0b28b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0b28b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="0b28b-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0b28b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="0b28b-110">Elements and attributes</span></span>

<span data-ttu-id="0b28b-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="0b28b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0b28b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0b28b-112">Child elements</span></span>

|<span data-ttu-id="0b28b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0b28b-113">**Element**</span></span>|<span data-ttu-id="0b28b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0b28b-114">**Type**</span></span>|<span data-ttu-id="0b28b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0b28b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0b28b-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="0b28b-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0b28b-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="0b28b-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0b28b-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="0b28b-118">Attributes</span></span>

<span data-ttu-id="0b28b-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0b28b-119">None.</span></span>
  

