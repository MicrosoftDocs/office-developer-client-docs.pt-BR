---
title: AuthorList_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 80a0dd01b3628bc44ed469ff7c236753d7677f51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338742"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="7491b-102">AuthorList_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7491b-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7491b-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="7491b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7491b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7491b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7491b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7491b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7491b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7491b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7491b-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="7491b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7491b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7491b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7491b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="7491b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7491b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7491b-110">Elements and attributes</span></span>

<span data-ttu-id="7491b-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7491b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7491b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7491b-112">Child elements</span></span>

|<span data-ttu-id="7491b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7491b-113">**Element**</span></span>|<span data-ttu-id="7491b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7491b-114">**Type**</span></span>|<span data-ttu-id="7491b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7491b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7491b-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="7491b-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7491b-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="7491b-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7491b-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="7491b-118">Attributes</span></span>

<span data-ttu-id="7491b-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7491b-119">None.</span></span>
  

