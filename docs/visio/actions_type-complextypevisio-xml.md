---
title: Actions_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 158a0dfa31c2da3ac9e530c07edd075b4fabbd75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389558"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="1b1d0-102">Actions_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1b1d0-102">Actions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1b1d0-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="1b1d0-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b1d0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b1d0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1b1d0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1b1d0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1b1d0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1b1d0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1b1d0-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="1b1d0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1b1d0-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1b1d0-108">Section_Type complexType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b1d0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="1b1d0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1b1d0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1b1d0-110">Elements and attributes</span></span>

<span data-ttu-id="1b1d0-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1b1d0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1b1d0-112">Child elements</span></span>

|<span data-ttu-id="1b1d0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1b1d0-113">**Element**</span></span>|<span data-ttu-id="1b1d0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1b1d0-114">**Type**</span></span>|<span data-ttu-id="1b1d0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b1d0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b1d0-116">Linha</span><span class="sxs-lookup"><span data-stu-id="1b1d0-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1b1d0-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="1b1d0-117">ActionsRow_Type complexType</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1b1d0-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b1d0-118">Attributes</span></span>

<span data-ttu-id="1b1d0-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1b1d0-119">None.</span></span>
  

