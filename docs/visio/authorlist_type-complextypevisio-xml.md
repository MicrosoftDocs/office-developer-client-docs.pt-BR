---
title: AuthorList_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 5df48bcc69f0bd4aa818f265d0c7db1986165b3e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537896"
---
# <a name="authorlist_type-complextype-visio-xml"></a><span data-ttu-id="d5964-102">AuthorList_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="d5964-102">AuthorList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d5964-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="d5964-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5964-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d5964-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d5964-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d5964-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d5964-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d5964-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d5964-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="d5964-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d5964-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d5964-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5964-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d5964-109">Definition</span></span>

```XML
          <xs:complexType name="AuthorList_Type">
          
          <xs:sequence>
    <xs:element name="AuthorEntry"  type="AuthorEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d5964-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d5964-110">Elements and attributes</span></span>

<span data-ttu-id="d5964-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d5964-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d5964-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d5964-112">Child elements</span></span>

|<span data-ttu-id="d5964-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d5964-113">**Element**</span></span>|<span data-ttu-id="d5964-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d5964-114">**Type**</span></span>|<span data-ttu-id="d5964-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d5964-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5964-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="d5964-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5964-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="d5964-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d5964-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5964-118">Attributes</span></span>

<span data-ttu-id="d5964-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d5964-119">None.</span></span>
  

