---
title: PolylineTo_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e0b87cc0-397d-7640-34ea-2a725d8f0999
ms.openlocfilehash: 051054b8ad95438392a006814331d75e4721d0e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772515"
---
# <a name="polylinetotype-complextype-visio-xml"></a><span data-ttu-id="f9318-102">PolylineTo_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f9318-102">PolylineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f9318-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="f9318-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9318-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f9318-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f9318-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f9318-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f9318-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f9318-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f9318-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="f9318-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f9318-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="f9318-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f9318-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f9318-109">Definition</span></span>

```XML
          <xs:complexType name="PolylineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="f9318-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f9318-110">Elements and attributes</span></span>

<span data-ttu-id="f9318-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f9318-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f9318-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f9318-112">Child elements</span></span>

|<span data-ttu-id="f9318-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f9318-113">**Element**</span></span>|<span data-ttu-id="f9318-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f9318-114">**Type**</span></span>|<span data-ttu-id="f9318-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f9318-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f9318-116">Célula</span><span class="sxs-lookup"><span data-stu-id="f9318-116">Cell</span></span>](cell-element-polylineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="f9318-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f9318-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f9318-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9318-118">Attributes</span></span>

<span data-ttu-id="f9318-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f9318-119">None.</span></span>
  

