---
title: PageContents_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d611c03f-6a4f-9de2-6714-87131cddce85
ms.openlocfilehash: 70f28182d8c82b9283e793856f7944c9a4823bc0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383426"
---
# <a name="pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="23a40-102">PageContents_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="23a40-102">PageContents_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="23a40-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="23a40-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23a40-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="23a40-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="23a40-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="23a40-105">**Schema file**</span></span> <br/> |<span data-ttu-id="23a40-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="23a40-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="23a40-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="23a40-107">**Extension base**</span></span> <br/> |<span data-ttu-id="23a40-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="23a40-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="23a40-109">Definição</span><span class="sxs-lookup"><span data-stu-id="23a40-109">Definition</span></span>

```XML
          <xs:complexType name="PageContents_Type">
          
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Connects"  type="Connects_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="23a40-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="23a40-110">Elements and attributes</span></span>

<span data-ttu-id="23a40-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="23a40-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="23a40-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="23a40-112">Child elements</span></span>

|<span data-ttu-id="23a40-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="23a40-113">**Element**</span></span>|<span data-ttu-id="23a40-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="23a40-114">**Type**</span></span>|<span data-ttu-id="23a40-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="23a40-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23a40-116">Connects</span><span class="sxs-lookup"><span data-stu-id="23a40-116">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23a40-117">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="23a40-117">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="23a40-118">Shapes</span><span class="sxs-lookup"><span data-stu-id="23a40-118">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23a40-119">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="23a40-119">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="23a40-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="23a40-120">Attributes</span></span>

<span data-ttu-id="23a40-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="23a40-121">None.</span></span>
  

