---
title: LineGradientRow_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b35d58b-ec6f-9b99-01fb-c665630e65d7
ms.openlocfilehash: 9c39ddd971f3089bb8b87026616c455e6a0524eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541138"
---
# <a name="linegradientrowtype-complextype-visio-xml"></a><span data-ttu-id="27109-102">LineGradientRow_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="27109-102">LineGradientRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="27109-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="27109-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27109-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="27109-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="27109-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="27109-105">**Schema file**</span></span> <br/> |<span data-ttu-id="27109-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="27109-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="27109-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="27109-107">**Extension base**</span></span> <br/> |<span data-ttu-id="27109-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="27109-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27109-109">Definição</span><span class="sxs-lookup"><span data-stu-id="27109-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradientRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="27109-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="27109-110">Elements and attributes</span></span>

<span data-ttu-id="27109-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="27109-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="27109-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="27109-112">Child elements</span></span>

|<span data-ttu-id="27109-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="27109-113">**Element**</span></span>|<span data-ttu-id="27109-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="27109-114">**Type**</span></span>|<span data-ttu-id="27109-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="27109-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27109-116">Cell</span><span class="sxs-lookup"><span data-stu-id="27109-116">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="27109-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="27109-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="27109-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="27109-118">Attributes</span></span>

<span data-ttu-id="27109-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="27109-119">None.</span></span>
  

