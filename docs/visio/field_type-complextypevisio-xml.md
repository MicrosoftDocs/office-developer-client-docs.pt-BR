---
title: Field_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c346fb8d-f247-4a14-19cd-9368ec86ce3f
ms.openlocfilehash: e67ea9dd5eed1892888ccd59c2ade1d95bd5d79e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542363"
---
# <a name="field_type-complextype-visio-xml"></a><span data-ttu-id="2865b-102">Field_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="2865b-102">Field_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2865b-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="2865b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2865b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2865b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2865b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2865b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2865b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2865b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2865b-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="2865b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2865b-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="2865b-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2865b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="2865b-109">Definition</span></span>

```XML
          <xs:complexType name="Field_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FieldRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2865b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2865b-110">Elements and attributes</span></span>

<span data-ttu-id="2865b-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2865b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2865b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2865b-112">Child elements</span></span>

|<span data-ttu-id="2865b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2865b-113">**Element**</span></span>|<span data-ttu-id="2865b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2865b-114">**Type**</span></span>|<span data-ttu-id="2865b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2865b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2865b-116">Row</span><span class="sxs-lookup"><span data-stu-id="2865b-116">Row</span></span>](row-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2865b-117">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="2865b-117">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2865b-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="2865b-118">Attributes</span></span>

<span data-ttu-id="2865b-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2865b-119">None.</span></span>
  

