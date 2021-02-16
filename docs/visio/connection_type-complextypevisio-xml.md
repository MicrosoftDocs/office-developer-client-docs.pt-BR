---
title: Connection_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c0ac13b-70cc-398b-a1a3-e7d8080c8f7b
ms.openlocfilehash: c079a7b1b12dec66d589adc1c6eb869cef0a1ed0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542503"
---
# <a name="connection_type-complextype-visio-xml"></a><span data-ttu-id="d9dc4-102">Connection_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="d9dc4-102">Connection_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d9dc4-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="d9dc4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9dc4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d9dc4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d9dc4-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d9dc4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d9dc4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d9dc4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d9dc4-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="d9dc4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d9dc4-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d9dc4-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d9dc4-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d9dc4-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d9dc4-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d9dc4-110">Elements and attributes</span></span>

<span data-ttu-id="d9dc4-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d9dc4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d9dc4-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d9dc4-112">Child elements</span></span>

|<span data-ttu-id="d9dc4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d9dc4-113">**Element**</span></span>|<span data-ttu-id="d9dc4-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d9dc4-114">**Type**</span></span>|<span data-ttu-id="d9dc4-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d9dc4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d9dc4-116">Linha</span><span class="sxs-lookup"><span data-stu-id="d9dc4-116">Row</span></span>](row-element-connection-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d9dc4-117">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="d9dc4-117">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d9dc4-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d9dc4-118">Attributes</span></span>

<span data-ttu-id="d9dc4-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d9dc4-119">None.</span></span>
  

