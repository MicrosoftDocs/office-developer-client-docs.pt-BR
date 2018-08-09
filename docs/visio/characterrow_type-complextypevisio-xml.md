---
title: CharacterRow_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61c99712-d451-408a-de15-fb088605b07c
ms.openlocfilehash: b96d982798f17aaec12a79b659a0bbf462f566fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771501"
---
# <a name="characterrowtype-complextype-visio-xml"></a><span data-ttu-id="a69a5-102">CharacterRow_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a69a5-102">CharacterRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a69a5-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="a69a5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a69a5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a69a5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a69a5-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a69a5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a69a5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a69a5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a69a5-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="a69a5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a69a5-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="a69a5-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a69a5-109">Definição</span><span class="sxs-lookup"><span data-stu-id="a69a5-109">Definition</span></span>

```XML
          <xs:complexType name="CharacterRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="a69a5-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="a69a5-110">Elements and attributes</span></span>

<span data-ttu-id="a69a5-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="a69a5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a69a5-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a69a5-112">Child elements</span></span>

|<span data-ttu-id="a69a5-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a69a5-113">**Element**</span></span>|<span data-ttu-id="a69a5-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a69a5-114">**Type**</span></span>|<span data-ttu-id="a69a5-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a69a5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a69a5-116">Célula</span><span class="sxs-lookup"><span data-stu-id="a69a5-116">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a69a5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a69a5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a69a5-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="a69a5-118">Attributes</span></span>

<span data-ttu-id="a69a5-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a69a5-119">None.</span></span>
  

