---
title: RelQuadBezTo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 558c7315-5025-484b-446e-333890bc1c3a
ms.openlocfilehash: d584891576967f3e452402667f0adaad5c87843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320164"
---
# <a name="relquadbeztotype-complextype-visio-xml"></a><span data-ttu-id="f7e13-102">RelQuadBezTo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f7e13-102">RelQuadBezTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f7e13-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="f7e13-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7e13-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f7e13-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f7e13-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f7e13-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f7e13-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f7e13-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f7e13-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="f7e13-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f7e13-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="f7e13-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f7e13-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f7e13-109">Definition</span></span>

```XML
          <xs:complexType name="RelQuadBezTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="f7e13-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f7e13-110">Elements and attributes</span></span>

<span data-ttu-id="f7e13-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f7e13-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f7e13-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f7e13-112">Child elements</span></span>

|<span data-ttu-id="f7e13-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f7e13-113">**Element**</span></span>|<span data-ttu-id="f7e13-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f7e13-114">**Type**</span></span>|<span data-ttu-id="f7e13-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f7e13-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f7e13-116">Cell</span><span class="sxs-lookup"><span data-stu-id="f7e13-116">Cell</span></span>](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="f7e13-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f7e13-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f7e13-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="f7e13-118">Attributes</span></span>

<span data-ttu-id="f7e13-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f7e13-119">None.</span></span>
  

