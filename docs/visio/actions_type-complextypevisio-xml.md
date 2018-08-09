---
title: Actions_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: e28b80e64865196fd6ba13035385b9523f6b1bc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771251"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="06b22-102">Actions_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="06b22-102">Actions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="06b22-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="06b22-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06b22-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="06b22-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="06b22-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="06b22-105">**Schema file**</span></span> <br/> |<span data-ttu-id="06b22-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="06b22-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="06b22-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="06b22-107">**Extension base**</span></span> <br/> |<span data-ttu-id="06b22-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="06b22-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="06b22-109">Definição</span><span class="sxs-lookup"><span data-stu-id="06b22-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="06b22-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="06b22-110">Elements and attributes</span></span>

<span data-ttu-id="06b22-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="06b22-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="06b22-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="06b22-112">Child elements</span></span>

|<span data-ttu-id="06b22-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="06b22-113">**Element**</span></span>|<span data-ttu-id="06b22-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="06b22-114">**Type**</span></span>|<span data-ttu-id="06b22-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="06b22-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="06b22-116">Row</span><span class="sxs-lookup"><span data-stu-id="06b22-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="06b22-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="06b22-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="06b22-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="06b22-118">Attributes</span></span>

<span data-ttu-id="06b22-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="06b22-119">None.</span></span>
  

