---
title: StyleSheets_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: 845580f2842c098cfb16776b9ab1d5d513ef8e22
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538883"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="4992c-102">StyleSheets_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="4992c-102">StyleSheets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4992c-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="4992c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4992c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4992c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4992c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4992c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4992c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4992c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4992c-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="4992c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4992c-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4992c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4992c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4992c-109">Definition</span></span>

```XML
          <xs:complexType name="StyleSheets_Type">
          
          <xs:sequence>
    <xs:element name="StyleSheet"  type="StyleSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4992c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4992c-110">Elements and attributes</span></span>

<span data-ttu-id="4992c-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4992c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4992c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4992c-112">Child elements</span></span>

|<span data-ttu-id="4992c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4992c-113">**Element**</span></span>|<span data-ttu-id="4992c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4992c-114">**Type**</span></span>|<span data-ttu-id="4992c-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4992c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4992c-116">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="4992c-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4992c-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4992c-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4992c-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="4992c-118">Attributes</span></span>

<span data-ttu-id="4992c-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4992c-119">None.</span></span>
  

