---
title: AuthorList_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: e4cee87a5060580e8b7f1efc7970091d56fd310f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771263"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="08944-102">AuthorList_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="08944-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="08944-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="08944-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08944-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="08944-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="08944-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="08944-105">**Schema file**</span></span> <br/> |<span data-ttu-id="08944-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="08944-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="08944-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="08944-107">**Extension base**</span></span> <br/> |<span data-ttu-id="08944-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="08944-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="08944-109">Definição</span><span class="sxs-lookup"><span data-stu-id="08944-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="08944-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="08944-110">Elements and attributes</span></span>

<span data-ttu-id="08944-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="08944-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="08944-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="08944-112">Child elements</span></span>

|<span data-ttu-id="08944-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="08944-113">**Element**</span></span>|<span data-ttu-id="08944-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="08944-114">**Type**</span></span>|<span data-ttu-id="08944-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="08944-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08944-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="08944-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="08944-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="08944-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="08944-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="08944-118">Attributes</span></span>

<span data-ttu-id="08944-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="08944-119">None.</span></span>
  

