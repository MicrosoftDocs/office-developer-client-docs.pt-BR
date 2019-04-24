---
title: NURBSTo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7ae8a1d-5bb7-a92f-79d6-5a358d879c32
ms.openlocfilehash: 47c8c552fb50c29ecf2f89325c1a818e61d60d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361002"
---
# <a name="nurbstotype-complextype-visio-xml"></a><span data-ttu-id="99c60-102">NURBSTo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="99c60-102">NURBSTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="99c60-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="99c60-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99c60-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="99c60-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="99c60-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="99c60-105">**Schema file**</span></span> <br/> |<span data-ttu-id="99c60-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="99c60-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="99c60-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="99c60-107">**Extension base**</span></span> <br/> |<span data-ttu-id="99c60-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="99c60-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="99c60-109">Definição</span><span class="sxs-lookup"><span data-stu-id="99c60-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="99c60-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="99c60-110">Elements and attributes</span></span>

<span data-ttu-id="99c60-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="99c60-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="99c60-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="99c60-112">Child elements</span></span>

|<span data-ttu-id="99c60-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99c60-113">**Element**</span></span>|<span data-ttu-id="99c60-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99c60-114">**Type**</span></span>|<span data-ttu-id="99c60-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="99c60-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99c60-116">Cell</span><span class="sxs-lookup"><span data-stu-id="99c60-116">Cell</span></span>](cell-element-nurbsto-rowvisio-xml.md) <br/> |[<span data-ttu-id="99c60-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="99c60-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="99c60-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="99c60-118">Attributes</span></span>

<span data-ttu-id="99c60-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="99c60-119">None.</span></span>
  

