---
title: ArcTo_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c30c80eb-6327-ebc3-7ea4-8b2fc7525cc0
ms.openlocfilehash: 73a89d7535a81700a875f68905de844f876a6181
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390146"
---
# <a name="arctotype-complextype-visio-xml"></a><span data-ttu-id="acd4c-102">ArcTo_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="acd4c-102">ArcTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="acd4c-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="acd4c-103">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acd4c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="acd4c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="acd4c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="acd4c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="acd4c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="acd4c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="acd4c-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="acd4c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="acd4c-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="acd4c-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="acd4c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="acd4c-109">Definition</span></span>

```XML
          <xs:complexType name="ArcTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="acd4c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="acd4c-110">Elements and attributes</span></span>

<span data-ttu-id="acd4c-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="acd4c-111">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="acd4c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="acd4c-112">Child elements</span></span>

|<span data-ttu-id="acd4c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="acd4c-113">**Element**</span></span>|<span data-ttu-id="acd4c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="acd4c-114">**Type**</span></span>|<span data-ttu-id="acd4c-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="acd4c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="acd4c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="acd4c-116">Cell</span></span>](cell-element-arcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="acd4c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="acd4c-117">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="acd4c-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="acd4c-118">Attributes</span></span>

<span data-ttu-id="acd4c-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="acd4c-119">None.</span></span>
  

