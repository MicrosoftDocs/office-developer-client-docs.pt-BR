---
title: RelEllipticalArcTo_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 45b2ff30-bca1-fbaa-cc9f-fe9b52b631c4
ms.openlocfilehash: 701676adcb82c2aeee63a975c2a35fc6c5256635
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542714"
---
# <a name="relellipticalarcto_type-complextype-visio-xml"></a><span data-ttu-id="67b53-102">RelEllipticalArcTo_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="67b53-102">RelEllipticalArcTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="67b53-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="67b53-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67b53-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="67b53-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="67b53-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="67b53-105">**Schema file**</span></span> <br/> |<span data-ttu-id="67b53-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="67b53-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="67b53-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="67b53-107">**Extension base**</span></span> <br/> |<span data-ttu-id="67b53-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="67b53-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67b53-109">Definição</span><span class="sxs-lookup"><span data-stu-id="67b53-109">Definition</span></span>

```XML
          <xs:complexType name="RelEllipticalArcTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="67b53-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="67b53-110">Elements and attributes</span></span>

<span data-ttu-id="67b53-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="67b53-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="67b53-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="67b53-112">Child elements</span></span>

|<span data-ttu-id="67b53-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="67b53-113">**Element**</span></span>|<span data-ttu-id="67b53-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67b53-114">**Type**</span></span>|<span data-ttu-id="67b53-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="67b53-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67b53-116">Cell</span><span class="sxs-lookup"><span data-stu-id="67b53-116">Cell</span></span>](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="67b53-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="67b53-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="67b53-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="67b53-118">Attributes</span></span>

<span data-ttu-id="67b53-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="67b53-119">None.</span></span>
  

