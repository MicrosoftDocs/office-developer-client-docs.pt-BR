---
title: CommentList_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 640ba8825ffdfaa92c7a7ce43fb6bfb92e19ce12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771530"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="50360-102">CommentList_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="50360-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="50360-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="50360-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50360-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="50360-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="50360-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="50360-105">**Schema file**</span></span> <br/> |<span data-ttu-id="50360-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="50360-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="50360-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="50360-107">**Extension base**</span></span> <br/> |<span data-ttu-id="50360-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="50360-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="50360-109">Definição</span><span class="sxs-lookup"><span data-stu-id="50360-109">Definition</span></span>

```XML
          <xs:complexType name="CommentList_Type">
          
          <xs:sequence>
    <xs:element name="CommentEntry"  type="CommentEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="50360-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="50360-110">Elements and attributes</span></span>

<span data-ttu-id="50360-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="50360-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="50360-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="50360-112">Child elements</span></span>

|<span data-ttu-id="50360-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="50360-113">**Element**</span></span>|<span data-ttu-id="50360-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="50360-114">**Type**</span></span>|<span data-ttu-id="50360-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="50360-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="50360-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="50360-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50360-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="50360-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="50360-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="50360-118">Attributes</span></span>

<span data-ttu-id="50360-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="50360-119">None.</span></span>
  

