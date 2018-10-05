---
title: Hyperlink_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: 6c966447c13d90b05918138aeeafb11133e7bb5e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392029"
---
# <a name="hyperlinktype-complextype-visio-xml"></a><span data-ttu-id="d1848-102">Hyperlink_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d1848-102">Hyperlink_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d1848-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="d1848-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1848-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d1848-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d1848-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d1848-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d1848-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d1848-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d1848-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="d1848-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d1848-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d1848-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d1848-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d1848-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d1848-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d1848-110">Elements and attributes</span></span>

<span data-ttu-id="d1848-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d1848-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d1848-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d1848-112">Child elements</span></span>

|<span data-ttu-id="d1848-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d1848-113">**Element**</span></span>|<span data-ttu-id="d1848-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d1848-114">**Type**</span></span>|<span data-ttu-id="d1848-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d1848-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d1848-116">Row</span><span class="sxs-lookup"><span data-stu-id="d1848-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d1848-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="d1848-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d1848-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d1848-118">Attributes</span></span>

<span data-ttu-id="d1848-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d1848-119">None.</span></span>
  

