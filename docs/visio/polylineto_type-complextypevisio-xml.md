---
title: PolylineTo_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e0b87cc0-397d-7640-34ea-2a725d8f0999
ms.openlocfilehash: 71948dc1cab853c00fa993e26acef108def8aa1c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397349"
---
# <a name="polylinetotype-complextype-visio-xml"></a><span data-ttu-id="d1f64-102">PolylineTo_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d1f64-102">PolylineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d1f64-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="d1f64-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1f64-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d1f64-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d1f64-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d1f64-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d1f64-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d1f64-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d1f64-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="d1f64-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d1f64-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="d1f64-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d1f64-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d1f64-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d1f64-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d1f64-110">Elements and attributes</span></span>

<span data-ttu-id="d1f64-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d1f64-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d1f64-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d1f64-112">Child elements</span></span>

|<span data-ttu-id="d1f64-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d1f64-113">**Element**</span></span>|<span data-ttu-id="d1f64-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d1f64-114">**Type**</span></span>|<span data-ttu-id="d1f64-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d1f64-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d1f64-116">Célula</span><span class="sxs-lookup"><span data-stu-id="d1f64-116">Cell</span></span>](cell-element-polylineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="d1f64-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d1f64-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d1f64-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d1f64-118">Attributes</span></span>

<span data-ttu-id="d1f64-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d1f64-119">None.</span></span>
  

