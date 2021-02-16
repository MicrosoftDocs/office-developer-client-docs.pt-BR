---
title: Hyperlink_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: ce9a1f5b9a6e402ec157d641f81a82c6df4b92e1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541551"
---
# <a name="hyperlink_type-complextype-visio-xml"></a><span data-ttu-id="387b5-102">Hyperlink_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="387b5-102">Hyperlink_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="387b5-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="387b5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="387b5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="387b5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="387b5-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="387b5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="387b5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="387b5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="387b5-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="387b5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="387b5-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="387b5-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="387b5-109">Definição</span><span class="sxs-lookup"><span data-stu-id="387b5-109">Definition</span></span>

```XML
          <xs:complexType name="Hyperlink_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="HyperlinkRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="387b5-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="387b5-110">Elements and attributes</span></span>

<span data-ttu-id="387b5-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="387b5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="387b5-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="387b5-112">Child elements</span></span>

|<span data-ttu-id="387b5-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="387b5-113">**Element**</span></span>|<span data-ttu-id="387b5-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="387b5-114">**Type**</span></span>|<span data-ttu-id="387b5-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="387b5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="387b5-116">Row</span><span class="sxs-lookup"><span data-stu-id="387b5-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="387b5-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="387b5-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="387b5-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="387b5-118">Attributes</span></span>

<span data-ttu-id="387b5-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="387b5-119">None.</span></span>
  

