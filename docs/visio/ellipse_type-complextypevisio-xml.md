---
title: Ellipse_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67dc78e-6639-e32f-4909-945001659d30
ms.openlocfilehash: f9b82e9c34ee4a520f318e7c8fa1ffd8b0797d6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345658"
---
# <a name="ellipsetype-complextype-visio-xml"></a><span data-ttu-id="babbf-102">Ellipse_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="babbf-102">Ellipse_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="babbf-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="babbf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="babbf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="babbf-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="babbf-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="babbf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="babbf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="babbf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="babbf-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="babbf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="babbf-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="babbf-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="babbf-109">Definição</span><span class="sxs-lookup"><span data-stu-id="babbf-109">Definition</span></span>

```XML
          <xs:complexType name="Ellipse_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="babbf-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="babbf-110">Elements and attributes</span></span>

<span data-ttu-id="babbf-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="babbf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="babbf-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="babbf-112">Child elements</span></span>

|<span data-ttu-id="babbf-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="babbf-113">**Element**</span></span>|<span data-ttu-id="babbf-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="babbf-114">**Type**</span></span>|<span data-ttu-id="babbf-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="babbf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="babbf-116">Cell</span><span class="sxs-lookup"><span data-stu-id="babbf-116">Cell</span></span>](cell-element-ellipse-rowvisio-xml.md) <br/> |[<span data-ttu-id="babbf-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="babbf-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="babbf-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="babbf-118">Attributes</span></span>

<span data-ttu-id="babbf-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="babbf-119">None.</span></span>
  

