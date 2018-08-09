---
title: Solutions_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: 69c5bf92bb9f72e9969f9687b42b9d583eb2a523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773037"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="004bf-102">Solutions_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="004bf-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="004bf-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="004bf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="004bf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="004bf-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="004bf-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="004bf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="004bf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="004bf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="004bf-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="004bf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="004bf-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="004bf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="004bf-109">Definição</span><span class="sxs-lookup"><span data-stu-id="004bf-109">Definition</span></span>

```XML
          <xs:complexType name="Solutions_Type">
          
          <xs:sequence>
    <xs:element name="Solution"  type="Solution_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="004bf-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="004bf-110">Elements and attributes</span></span>

<span data-ttu-id="004bf-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="004bf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="004bf-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="004bf-112">Child elements</span></span>

|<span data-ttu-id="004bf-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="004bf-113">**Element**</span></span>|<span data-ttu-id="004bf-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="004bf-114">**Type**</span></span>|<span data-ttu-id="004bf-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="004bf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="004bf-116">Solution</span><span class="sxs-lookup"><span data-stu-id="004bf-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="004bf-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="004bf-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="004bf-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="004bf-118">Attributes</span></span>

<span data-ttu-id="004bf-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="004bf-119">None.</span></span>
  

