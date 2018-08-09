---
title: Colors_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: 187d51c2102e9d13ffea15c6de2db849ef980fb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771508"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="ebe49-102">Colors_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ebe49-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ebe49-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="ebe49-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebe49-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ebe49-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ebe49-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ebe49-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ebe49-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ebe49-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ebe49-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="ebe49-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ebe49-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ebe49-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ebe49-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ebe49-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ebe49-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ebe49-110">Elements and attributes</span></span>

<span data-ttu-id="ebe49-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ebe49-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ebe49-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ebe49-112">Child elements</span></span>

|<span data-ttu-id="ebe49-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ebe49-113">**Element**</span></span>|<span data-ttu-id="ebe49-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ebe49-114">**Type**</span></span>|<span data-ttu-id="ebe49-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ebe49-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ebe49-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="ebe49-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ebe49-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="ebe49-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ebe49-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebe49-118">Attributes</span></span>

<span data-ttu-id="ebe49-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ebe49-119">None.</span></span>
  

