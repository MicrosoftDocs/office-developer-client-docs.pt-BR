---
title: EllipticalArcTo_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dc10f727-5243-2fdb-4042-3dfdfcd8504c
ms.openlocfilehash: a6b10c60563a7923990cdb552b1d10fd5c43b97e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397251"
---
# <a name="ellipticalarctotype-complextype-visio-xml"></a><span data-ttu-id="a13b0-102">EllipticalArcTo_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a13b0-102">EllipticalArcTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a13b0-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="a13b0-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a13b0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a13b0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a13b0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a13b0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a13b0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a13b0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a13b0-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="a13b0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a13b0-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="a13b0-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a13b0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="a13b0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a13b0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a13b0-110">Elements and attributes</span></span>

<span data-ttu-id="a13b0-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a13b0-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a13b0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a13b0-112">Child elements</span></span>

|<span data-ttu-id="a13b0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a13b0-113">**Element**</span></span>|<span data-ttu-id="a13b0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a13b0-114">**Type**</span></span>|<span data-ttu-id="a13b0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a13b0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a13b0-116">Cell</span><span class="sxs-lookup"><span data-stu-id="a13b0-116">Cell</span></span>](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="a13b0-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a13b0-117">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a13b0-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="a13b0-118">Attributes</span></span>

<span data-ttu-id="a13b0-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a13b0-119">None.</span></span>
  

