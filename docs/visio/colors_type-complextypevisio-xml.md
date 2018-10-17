---
title: Colors_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: e447ceb6fc0e6b79ec6e62b5f3b73a32cec589d9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400912"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="2f0ae-102">Colors_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="2f0ae-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2f0ae-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="2f0ae-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f0ae-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2f0ae-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2f0ae-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2f0ae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2f0ae-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2f0ae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2f0ae-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="2f0ae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2f0ae-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2f0ae-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2f0ae-109">Definição</span><span class="sxs-lookup"><span data-stu-id="2f0ae-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2f0ae-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2f0ae-110">Elements and attributes</span></span>

<span data-ttu-id="2f0ae-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2f0ae-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2f0ae-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2f0ae-112">Child elements</span></span>

|<span data-ttu-id="2f0ae-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2f0ae-113">**Element**</span></span>|<span data-ttu-id="2f0ae-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2f0ae-114">**Type**</span></span>|<span data-ttu-id="2f0ae-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2f0ae-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2f0ae-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="2f0ae-116">ColorEntry element</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2f0ae-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="2f0ae-117">ColorEntry_Type complexType</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2f0ae-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="2f0ae-118">Attributes</span></span>

<span data-ttu-id="2f0ae-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2f0ae-119">None.</span></span>
  

