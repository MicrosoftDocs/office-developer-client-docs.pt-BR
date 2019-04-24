---
title: Connection_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c0ac13b-70cc-398b-a1a3-e7d8080c8f7b
ms.openlocfilehash: a63f3b22dc7020cd25326fc24ae5cb770f23285b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319604"
---
# <a name="connectiontype-complextype-visio-xml"></a><span data-ttu-id="52fe7-102">Connection_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="52fe7-102">Connection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="52fe7-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="52fe7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52fe7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="52fe7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="52fe7-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="52fe7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="52fe7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="52fe7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="52fe7-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="52fe7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="52fe7-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="52fe7-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="52fe7-109">Definição</span><span class="sxs-lookup"><span data-stu-id="52fe7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="52fe7-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="52fe7-110">Elements and attributes</span></span>

<span data-ttu-id="52fe7-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="52fe7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="52fe7-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="52fe7-112">Child elements</span></span>

|<span data-ttu-id="52fe7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="52fe7-113">**Element**</span></span>|<span data-ttu-id="52fe7-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="52fe7-114">**Type**</span></span>|<span data-ttu-id="52fe7-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="52fe7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="52fe7-116">Linha</span><span class="sxs-lookup"><span data-stu-id="52fe7-116">Row</span></span>](row-element-connection-sectionvisio-xml.md) <br/> |[<span data-ttu-id="52fe7-117">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="52fe7-117">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="52fe7-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="52fe7-118">Attributes</span></span>

<span data-ttu-id="52fe7-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="52fe7-119">None.</span></span>
  

