---
title: NURBSTo_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7ae8a1d-5bb7-a92f-79d6-5a358d879c32
ms.openlocfilehash: 090df2487eb6fabfba4b3917c7d938fe4f841147
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540914"
---
# <a name="nurbstotype-complextype-visio-xml"></a><span data-ttu-id="1e1ed-102">NURBSTo_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="1e1ed-102">NURBSTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1e1ed-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="1e1ed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e1ed-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e1ed-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1e1ed-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1e1ed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1e1ed-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1e1ed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1e1ed-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="1e1ed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1e1ed-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="1e1ed-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e1ed-109">Definição</span><span class="sxs-lookup"><span data-stu-id="1e1ed-109">Definition</span></span>

```XML
          <xs:complexType name="NURBSTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="1e1ed-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1e1ed-110">Elements and attributes</span></span>

<span data-ttu-id="1e1ed-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1e1ed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1e1ed-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1e1ed-112">Child elements</span></span>

|<span data-ttu-id="1e1ed-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1e1ed-113">**Element**</span></span>|<span data-ttu-id="1e1ed-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1e1ed-114">**Type**</span></span>|<span data-ttu-id="1e1ed-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1e1ed-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1e1ed-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1e1ed-116">Cell</span></span>](cell-element-nurbsto-rowvisio-xml.md) <br/> |[<span data-ttu-id="1e1ed-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1e1ed-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1e1ed-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1e1ed-118">Attributes</span></span>

<span data-ttu-id="1e1ed-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1e1ed-119">None.</span></span>
  

