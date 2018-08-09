---
title: Issues_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 1ebec9e42c71b93637155037bd881c8ddf330367
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772124"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="1b050-102">Issues_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1b050-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1b050-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="1b050-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b050-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b050-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1b050-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1b050-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1b050-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1b050-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1b050-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="1b050-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1b050-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1b050-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b050-109">Definição</span><span class="sxs-lookup"><span data-stu-id="1b050-109">Definition</span></span>

```XML
          <xs:complexType name="Issues_Type">
          
          <xs:sequence>
    <xs:element name="Issue"  type="Issue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b050-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1b050-110">Elements and attributes</span></span>

<span data-ttu-id="1b050-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1b050-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1b050-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1b050-112">Child elements</span></span>

|<span data-ttu-id="1b050-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1b050-113">**Element**</span></span>|<span data-ttu-id="1b050-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1b050-114">**Type**</span></span>|<span data-ttu-id="1b050-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b050-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b050-116">Problema</span><span class="sxs-lookup"><span data-stu-id="1b050-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b050-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="1b050-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1b050-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b050-118">Attributes</span></span>

<span data-ttu-id="1b050-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1b050-119">None.</span></span>
  

