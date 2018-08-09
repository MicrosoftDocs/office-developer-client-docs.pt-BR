---
title: MoveTo_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4cd3e605-9ac1-14f5-f4e1-992c9100b1b2
ms.openlocfilehash: ea88f86ad9e38692408730b49ee2f3d6cbc35a54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772402"
---
# <a name="movetotype-complextype-visio-xml"></a><span data-ttu-id="aab73-102">MoveTo_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="aab73-102">MoveTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="aab73-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="aab73-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aab73-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aab73-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aab73-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="aab73-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aab73-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aab73-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aab73-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="aab73-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aab73-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="aab73-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aab73-109">Definição</span><span class="sxs-lookup"><span data-stu-id="aab73-109">Definition</span></span>

```XML
          <xs:complexType name="MoveTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="aab73-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="aab73-110">Elements and attributes</span></span>

<span data-ttu-id="aab73-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="aab73-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aab73-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="aab73-112">Child elements</span></span>

|<span data-ttu-id="aab73-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aab73-113">**Element**</span></span>|<span data-ttu-id="aab73-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aab73-114">**Type**</span></span>|<span data-ttu-id="aab73-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aab73-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aab73-116">Célula</span><span class="sxs-lookup"><span data-stu-id="aab73-116">Cell</span></span>](cell-element-moveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="aab73-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="aab73-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="aab73-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="aab73-118">Attributes</span></span>

<span data-ttu-id="aab73-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="aab73-119">None.</span></span>
  

