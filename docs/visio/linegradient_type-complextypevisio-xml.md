---
title: LineGradient_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 5918e306479b907760fb539c3e476708d28de5e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393890"
---
# <a name="linegradienttype-complextype-visio-xml"></a><span data-ttu-id="1df62-102">LineGradient_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1df62-102">LineGradient_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1df62-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="1df62-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1df62-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1df62-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1df62-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1df62-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1df62-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1df62-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1df62-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="1df62-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1df62-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1df62-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1df62-109">Definição</span><span class="sxs-lookup"><span data-stu-id="1df62-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LineGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1df62-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1df62-110">Elements and attributes</span></span>

<span data-ttu-id="1df62-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1df62-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1df62-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1df62-112">Child elements</span></span>

|<span data-ttu-id="1df62-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1df62-113">**Element**</span></span>|<span data-ttu-id="1df62-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1df62-114">**Type**</span></span>|<span data-ttu-id="1df62-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1df62-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1df62-116">Row</span><span class="sxs-lookup"><span data-stu-id="1df62-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1df62-117">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="1df62-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1df62-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1df62-118">Attributes</span></span>

<span data-ttu-id="1df62-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1df62-119">None.</span></span>
  

