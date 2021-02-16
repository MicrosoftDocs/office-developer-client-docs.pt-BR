---
title: CommentList_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 9b85a3731cfde30307084c65da1d23aa86280afd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542048"
---
# <a name="commentlist_type-complextype-visio-xml"></a><span data-ttu-id="6a5fb-102">CommentList_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="6a5fb-102">CommentList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6a5fb-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="6a5fb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a5fb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6a5fb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6a5fb-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6a5fb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6a5fb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6a5fb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6a5fb-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="6a5fb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6a5fb-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6a5fb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6a5fb-109">Definição</span><span class="sxs-lookup"><span data-stu-id="6a5fb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6a5fb-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6a5fb-110">Elements and attributes</span></span>

<span data-ttu-id="6a5fb-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6a5fb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6a5fb-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6a5fb-112">Child elements</span></span>

|<span data-ttu-id="6a5fb-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6a5fb-113">**Element**</span></span>|<span data-ttu-id="6a5fb-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6a5fb-114">**Type**</span></span>|<span data-ttu-id="6a5fb-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6a5fb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6a5fb-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="6a5fb-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6a5fb-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="6a5fb-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6a5fb-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a5fb-118">Attributes</span></span>

<span data-ttu-id="6a5fb-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6a5fb-119">None.</span></span>
  

