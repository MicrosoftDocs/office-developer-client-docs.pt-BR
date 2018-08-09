---
title: EllipticalArcTo_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dc10f727-5243-2fdb-4042-3dfdfcd8504c
ms.openlocfilehash: da67df28a2081a52b9bcef39c06540b247a2a79e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771802"
---
# <a name="ellipticalarctotype-complextype-visio-xml"></a><span data-ttu-id="4b191-102">EllipticalArcTo_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4b191-102">EllipticalArcTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4b191-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="4b191-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b191-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4b191-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4b191-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4b191-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4b191-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4b191-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4b191-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="4b191-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4b191-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="4b191-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4b191-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4b191-109">Definition</span></span>

```XML
          <xs:complexType name="EllipticalArcTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="4b191-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4b191-110">Elements and attributes</span></span>

<span data-ttu-id="4b191-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4b191-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4b191-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4b191-112">Child elements</span></span>

|<span data-ttu-id="4b191-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4b191-113">**Element**</span></span>|<span data-ttu-id="4b191-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4b191-114">**Type**</span></span>|<span data-ttu-id="4b191-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4b191-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b191-116">Célula</span><span class="sxs-lookup"><span data-stu-id="4b191-116">Cell</span></span>](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="4b191-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4b191-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4b191-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="4b191-118">Attributes</span></span>

<span data-ttu-id="4b191-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4b191-119">None.</span></span>
  

