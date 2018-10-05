---
title: Masters_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398490"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="d78c0-102">Masters_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d78c0-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d78c0-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="d78c0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d78c0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d78c0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d78c0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d78c0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d78c0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d78c0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d78c0-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="d78c0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d78c0-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d78c0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d78c0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d78c0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d78c0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d78c0-110">Elements and attributes</span></span>

<span data-ttu-id="d78c0-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d78c0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d78c0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d78c0-112">Child elements</span></span>

|<span data-ttu-id="d78c0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d78c0-113">**Element**</span></span>|<span data-ttu-id="d78c0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d78c0-114">**Type**</span></span>|<span data-ttu-id="d78c0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d78c0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d78c0-116">Master</span><span class="sxs-lookup"><span data-stu-id="d78c0-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d78c0-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="d78c0-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d78c0-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="d78c0-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d78c0-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="d78c0-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d78c0-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="d78c0-120">Attributes</span></span>

<span data-ttu-id="d78c0-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d78c0-121">None.</span></span>
  

