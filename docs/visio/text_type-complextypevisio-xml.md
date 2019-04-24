---
title: Text_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: fe74af493983122c113e48ae5c0bb3b5b037ccef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332302"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="85a4e-102">Text_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="85a4e-102">Text_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="85a4e-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="85a4e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85a4e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85a4e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="85a4e-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="85a4e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="85a4e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="85a4e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="85a4e-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="85a4e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="85a4e-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="85a4e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85a4e-109">Definição</span><span class="sxs-lookup"><span data-stu-id="85a4e-109">Definition</span></span>

```XML
          <xs:complexType name="Text_Type">
          
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="cp"  type="cp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="pp"  type="pp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="tp"  type="tp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="fld"  type="fld_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="85a4e-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="85a4e-110">Elements and attributes</span></span>

<span data-ttu-id="85a4e-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="85a4e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="85a4e-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="85a4e-112">Child elements</span></span>

|<span data-ttu-id="85a4e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85a4e-113">**Element**</span></span>|<span data-ttu-id="85a4e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85a4e-114">**Type**</span></span>|<span data-ttu-id="85a4e-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85a4e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85a4e-116">CP</span><span class="sxs-lookup"><span data-stu-id="85a4e-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a4e-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="85a4e-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85a4e-118">FLD</span><span class="sxs-lookup"><span data-stu-id="85a4e-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a4e-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="85a4e-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85a4e-120">páginas</span><span class="sxs-lookup"><span data-stu-id="85a4e-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a4e-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="85a4e-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85a4e-122">par</span><span class="sxs-lookup"><span data-stu-id="85a4e-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a4e-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="85a4e-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="85a4e-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="85a4e-124">Attributes</span></span>

<span data-ttu-id="85a4e-125">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="85a4e-125">None.</span></span>
  

