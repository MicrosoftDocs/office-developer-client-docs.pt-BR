---
title: CommentList_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: af23616556cecdbfa1157a8d4c49de1ca4b2fd88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359413"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="05ff7-102">CommentList_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="05ff7-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="05ff7-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="05ff7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05ff7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="05ff7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="05ff7-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="05ff7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="05ff7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="05ff7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="05ff7-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="05ff7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="05ff7-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="05ff7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="05ff7-109">Definição</span><span class="sxs-lookup"><span data-stu-id="05ff7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="05ff7-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="05ff7-110">Elements and attributes</span></span>

<span data-ttu-id="05ff7-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="05ff7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="05ff7-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="05ff7-112">Child elements</span></span>

|<span data-ttu-id="05ff7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="05ff7-113">**Element**</span></span>|<span data-ttu-id="05ff7-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="05ff7-114">**Type**</span></span>|<span data-ttu-id="05ff7-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="05ff7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="05ff7-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="05ff7-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05ff7-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="05ff7-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="05ff7-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="05ff7-118">Attributes</span></span>

<span data-ttu-id="05ff7-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="05ff7-119">None.</span></span>
  

