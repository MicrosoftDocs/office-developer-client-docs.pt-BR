---
title: RelMoveTo_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3759d7cc-061b-0c0b-c372-b7d60effbfd0
ms.openlocfilehash: ff1a822b749fcddb2f3712a5eb82f12aabec0144
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395774"
---
# <a name="relmovetotype-complextype-visio-xml"></a><span data-ttu-id="1ff8b-102">RelMoveTo_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1ff8b-102">RelMoveTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1ff8b-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="1ff8b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ff8b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1ff8b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1ff8b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1ff8b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1ff8b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1ff8b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1ff8b-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="1ff8b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1ff8b-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="1ff8b-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ff8b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="1ff8b-109">Definition</span></span>

```XML
          <xs:complexType name="RelMoveTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="1ff8b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1ff8b-110">Elements and attributes</span></span>

<span data-ttu-id="1ff8b-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1ff8b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1ff8b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1ff8b-112">Child elements</span></span>

|<span data-ttu-id="1ff8b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1ff8b-113">**Element**</span></span>|<span data-ttu-id="1ff8b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ff8b-114">**Type**</span></span>|<span data-ttu-id="1ff8b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1ff8b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ff8b-116">Célula</span><span class="sxs-lookup"><span data-stu-id="1ff8b-116">Cell</span></span>](cell-element-relmoveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="1ff8b-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1ff8b-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1ff8b-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ff8b-118">Attributes</span></span>

<span data-ttu-id="1ff8b-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1ff8b-119">None.</span></span>
  

