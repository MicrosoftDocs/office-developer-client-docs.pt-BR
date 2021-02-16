---
title: Paragraph_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: fd7c5233b89bc92ed449d3d8d2767daa23ea8071
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540592"
---
# <a name="paragraph_type-complextype-visio-xml"></a><span data-ttu-id="ac214-102">Paragraph_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="ac214-102">Paragraph_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ac214-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="ac214-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac214-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ac214-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ac214-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ac214-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ac214-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ac214-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ac214-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="ac214-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ac214-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ac214-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ac214-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ac214-109">Definition</span></span>

```XML
          <xs:complexType name="Paragraph_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ParagraphRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ac214-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ac214-110">Elements and attributes</span></span>

<span data-ttu-id="ac214-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ac214-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ac214-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ac214-112">Child elements</span></span>

|<span data-ttu-id="ac214-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ac214-113">**Element**</span></span>|<span data-ttu-id="ac214-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ac214-114">**Type**</span></span>|<span data-ttu-id="ac214-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ac214-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac214-116">Row</span><span class="sxs-lookup"><span data-stu-id="ac214-116">Row</span></span>](row-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ac214-117">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="ac214-117">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ac214-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac214-118">Attributes</span></span>

<span data-ttu-id="ac214-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac214-119">None.</span></span>
  

