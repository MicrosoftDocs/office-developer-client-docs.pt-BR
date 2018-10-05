---
title: Pages_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: a03c5df25a28da40724178cf1c7f917ee4e723c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400156"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="e0650-102">Pages_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e0650-102">Pages_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e0650-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="e0650-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0650-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e0650-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e0650-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e0650-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e0650-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e0650-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e0650-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="e0650-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e0650-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e0650-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0650-109">Definição</span><span class="sxs-lookup"><span data-stu-id="e0650-109">Definition</span></span>

```XML
          <xs:complexType name="Pages_Type">
          
          <xs:sequence>
    <xs:element name="Page"  type="Page_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e0650-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="e0650-110">Elements and attributes</span></span>

<span data-ttu-id="e0650-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="e0650-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e0650-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e0650-112">Child elements</span></span>

|<span data-ttu-id="e0650-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0650-113">**Element**</span></span>|<span data-ttu-id="e0650-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e0650-114">**Type**</span></span>|<span data-ttu-id="e0650-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e0650-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e0650-116">Page</span><span class="sxs-lookup"><span data-stu-id="e0650-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0650-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="e0650-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e0650-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0650-118">Attributes</span></span>

<span data-ttu-id="e0650-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e0650-119">None.</span></span>
  

