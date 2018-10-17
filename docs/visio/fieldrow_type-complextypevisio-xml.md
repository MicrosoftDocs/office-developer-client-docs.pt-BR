---
title: FieldRow_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3474d268-4435-cb4d-9c66-a30924635e20
ms.openlocfilehash: 5f59ca23fa83d98622624cc20544f9b482ce5378
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400779"
---
# <a name="fieldrowtype-complextype-visio-xml"></a><span data-ttu-id="ac777-102">FieldRow_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ac777-102">FieldRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ac777-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="ac777-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac777-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ac777-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ac777-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ac777-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ac777-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ac777-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ac777-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="ac777-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ac777-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="ac777-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ac777-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ac777-109">Definition</span></span>

```XML
          <xs:complexType name="FieldRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="ac777-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ac777-110">Elements and attributes</span></span>

<span data-ttu-id="ac777-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ac777-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ac777-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ac777-112">Child elements</span></span>

|<span data-ttu-id="ac777-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ac777-113">**Element**</span></span>|<span data-ttu-id="ac777-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ac777-114">**Type**</span></span>|<span data-ttu-id="ac777-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ac777-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac777-116">Cell</span><span class="sxs-lookup"><span data-stu-id="ac777-116">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ac777-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ac777-117">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ac777-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac777-118">Attributes</span></span>

<span data-ttu-id="ac777-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac777-119">None.</span></span>
  

