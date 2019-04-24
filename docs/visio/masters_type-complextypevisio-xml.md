---
title: Masters_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341654"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="1bd29-102">Masters_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1bd29-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1bd29-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="1bd29-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bd29-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1bd29-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1bd29-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1bd29-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1bd29-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1bd29-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1bd29-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="1bd29-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1bd29-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1bd29-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1bd29-109">Definição</span><span class="sxs-lookup"><span data-stu-id="1bd29-109">Definition</span></span>

```XML
          <xs:complexType name="Masters_Type">
          
          <xs:sequence>
    <xs:element name="Master"  type="Master_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="MasterShortcut"  type="MasterShortcut_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1bd29-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1bd29-110">Elements and attributes</span></span>

<span data-ttu-id="1bd29-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1bd29-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1bd29-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1bd29-112">Child elements</span></span>

|<span data-ttu-id="1bd29-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1bd29-113">**Element**</span></span>|<span data-ttu-id="1bd29-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1bd29-114">**Type**</span></span>|<span data-ttu-id="1bd29-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1bd29-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1bd29-116">Master</span><span class="sxs-lookup"><span data-stu-id="1bd29-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1bd29-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="1bd29-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1bd29-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="1bd29-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1bd29-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="1bd29-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1bd29-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="1bd29-120">Attributes</span></span>

<span data-ttu-id="1bd29-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1bd29-121">None.</span></span>
  

