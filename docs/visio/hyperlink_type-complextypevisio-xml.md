---
title: Hyperlink_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: 226af4fee615b0dc6ddc4d92d13aff6dd1fd4b19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772024"
---
# <a name="hyperlinktype-complextype-visio-xml"></a><span data-ttu-id="36b9f-102">Hyperlink_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="36b9f-102">Hyperlink_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="36b9f-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="36b9f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36b9f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="36b9f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="36b9f-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="36b9f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="36b9f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="36b9f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="36b9f-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="36b9f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="36b9f-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="36b9f-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36b9f-109">Definição</span><span class="sxs-lookup"><span data-stu-id="36b9f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="36b9f-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="36b9f-110">Elements and attributes</span></span>

<span data-ttu-id="36b9f-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="36b9f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="36b9f-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="36b9f-112">Child elements</span></span>

|<span data-ttu-id="36b9f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="36b9f-113">**Element**</span></span>|<span data-ttu-id="36b9f-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="36b9f-114">**Type**</span></span>|<span data-ttu-id="36b9f-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36b9f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="36b9f-116">Row</span><span class="sxs-lookup"><span data-stu-id="36b9f-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="36b9f-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="36b9f-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="36b9f-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="36b9f-118">Attributes</span></span>

<span data-ttu-id="36b9f-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="36b9f-119">None.</span></span>
  

