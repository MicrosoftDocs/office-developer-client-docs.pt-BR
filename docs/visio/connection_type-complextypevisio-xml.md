---
title: Connection_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c0ac13b-70cc-398b-a1a3-e7d8080c8f7b
ms.openlocfilehash: a63f3b22dc7020cd25326fc24ae5cb770f23285b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400440"
---
# <a name="connectiontype-complextype-visio-xml"></a><span data-ttu-id="00ab2-102">Connection_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="00ab2-102">Connection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="00ab2-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="00ab2-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00ab2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="00ab2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="00ab2-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="00ab2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="00ab2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="00ab2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="00ab2-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="00ab2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="00ab2-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="00ab2-108">Section_Type complexType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="00ab2-109">Definição</span><span class="sxs-lookup"><span data-stu-id="00ab2-109">Definition</span></span>

```XML
          <xs:complexType name="Connection_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ConnectionRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="00ab2-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="00ab2-110">Elements and attributes</span></span>

<span data-ttu-id="00ab2-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="00ab2-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="00ab2-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="00ab2-112">Child elements</span></span>

|<span data-ttu-id="00ab2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="00ab2-113">**Element**</span></span>|<span data-ttu-id="00ab2-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="00ab2-114">**Type**</span></span>|<span data-ttu-id="00ab2-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="00ab2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="00ab2-116">Linha</span><span class="sxs-lookup"><span data-stu-id="00ab2-116">Row</span></span>](row-element-connection-sectionvisio-xml.md) <br/> |[<span data-ttu-id="00ab2-117">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="00ab2-117">ConnectionRow_Type complexType</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="00ab2-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="00ab2-118">Attributes</span></span>

<span data-ttu-id="00ab2-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="00ab2-119">None.</span></span>
  

