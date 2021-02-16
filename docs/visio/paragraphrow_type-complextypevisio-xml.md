---
title: ParagraphRow_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32bb67e1-8db8-fe28-f173-028a20bb136c
ms.openlocfilehash: 942d29516e5277fc9b0e68319118c309d9555648
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540578"
---
# <a name="paragraphrow_type-complextype-visio-xml"></a><span data-ttu-id="fc3d1-102">ParagraphRow_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="fc3d1-102">ParagraphRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fc3d1-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="fc3d1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc3d1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fc3d1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fc3d1-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fc3d1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fc3d1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fc3d1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fc3d1-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="fc3d1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fc3d1-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="fc3d1-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc3d1-109">Definição</span><span class="sxs-lookup"><span data-stu-id="fc3d1-109">Definition</span></span>

```XML
          <xs:complexType name="ParagraphRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="fc3d1-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fc3d1-110">Elements and attributes</span></span>

<span data-ttu-id="fc3d1-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fc3d1-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fc3d1-112">Child elements</span></span>

|<span data-ttu-id="fc3d1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fc3d1-113">**Element**</span></span>|<span data-ttu-id="fc3d1-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fc3d1-114">**Type**</span></span>|<span data-ttu-id="fc3d1-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fc3d1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc3d1-116">Cell</span><span class="sxs-lookup"><span data-stu-id="fc3d1-116">Cell</span></span>](cell-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="fc3d1-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fc3d1-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fc3d1-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc3d1-118">Attributes</span></span>

<span data-ttu-id="fc3d1-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fc3d1-119">None.</span></span>
  

