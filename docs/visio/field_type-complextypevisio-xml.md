---
title: Field_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c346fb8d-f247-4a14-19cd-9368ec86ce3f
ms.openlocfilehash: d711209ce1663f657b9a22fc6d4837ab51909647
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388508"
---
# <a name="fieldtype-complextype-visio-xml"></a><span data-ttu-id="effb4-102">Field_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="effb4-102">Field_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="effb4-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="effb4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="effb4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="effb4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="effb4-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="effb4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="effb4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="effb4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="effb4-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="effb4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="effb4-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="effb4-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="effb4-109">Definição</span><span class="sxs-lookup"><span data-stu-id="effb4-109">Definition</span></span>

```XML
          <xs:complexType name="Field_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FieldRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="effb4-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="effb4-110">Elements and attributes</span></span>

<span data-ttu-id="effb4-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="effb4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="effb4-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="effb4-112">Child elements</span></span>

|<span data-ttu-id="effb4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="effb4-113">**Element**</span></span>|<span data-ttu-id="effb4-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="effb4-114">**Type**</span></span>|<span data-ttu-id="effb4-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="effb4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="effb4-116">Row</span><span class="sxs-lookup"><span data-stu-id="effb4-116">Row</span></span>](row-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="effb4-117">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="effb4-117">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="effb4-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="effb4-118">Attributes</span></span>

<span data-ttu-id="effb4-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="effb4-119">None.</span></span>
  

