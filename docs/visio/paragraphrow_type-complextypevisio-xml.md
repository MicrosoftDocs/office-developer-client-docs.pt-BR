---
title: ParagraphRow_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32bb67e1-8db8-fe28-f173-028a20bb136c
ms.openlocfilehash: cec77978cf2f54e497f34a4619bea78f46402e1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772480"
---
# <a name="paragraphrowtype-complextype-visio-xml"></a><span data-ttu-id="775d4-102">ParagraphRow_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="775d4-102">ParagraphRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="775d4-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="775d4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="775d4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="775d4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="775d4-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="775d4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="775d4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="775d4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="775d4-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="775d4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="775d4-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="775d4-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="775d4-109">Definição</span><span class="sxs-lookup"><span data-stu-id="775d4-109">Definition</span></span>

```XML
          <xs:complexType name="ParagraphRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="775d4-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="775d4-110">Elements and attributes</span></span>

<span data-ttu-id="775d4-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="775d4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="775d4-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="775d4-112">Child elements</span></span>

|<span data-ttu-id="775d4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="775d4-113">**Element**</span></span>|<span data-ttu-id="775d4-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="775d4-114">**Type**</span></span>|<span data-ttu-id="775d4-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="775d4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="775d4-116">Célula</span><span class="sxs-lookup"><span data-stu-id="775d4-116">Cell</span></span>](cell-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="775d4-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="775d4-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="775d4-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="775d4-118">Attributes</span></span>

<span data-ttu-id="775d4-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="775d4-119">None.</span></span>
  

