---
title: StyleSheets_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: a48dc8d4c8327cffc53469a8c6d8a81d021a4500
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773078"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="940a8-102">StyleSheets_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="940a8-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="940a8-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="940a8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="940a8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="940a8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="940a8-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="940a8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="940a8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="940a8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="940a8-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="940a8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="940a8-108">None</span><span class="sxs-lookup"><span data-stu-id="940a8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="940a8-109">Definição</span><span class="sxs-lookup"><span data-stu-id="940a8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="940a8-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="940a8-110">Elements and attributes</span></span>

<span data-ttu-id="940a8-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="940a8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="940a8-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="940a8-112">Child elements</span></span>

|<span data-ttu-id="940a8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="940a8-113">**Element**</span></span>|<span data-ttu-id="940a8-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="940a8-114">**Type**</span></span>|<span data-ttu-id="940a8-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="940a8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="940a8-116">Folha de estilos</span><span class="sxs-lookup"><span data-stu-id="940a8-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="940a8-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="940a8-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="940a8-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="940a8-118">Attributes</span></span>

<span data-ttu-id="940a8-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="940a8-119">None.</span></span>
  

