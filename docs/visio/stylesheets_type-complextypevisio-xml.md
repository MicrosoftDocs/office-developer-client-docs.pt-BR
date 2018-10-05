---
title: StyleSheets_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: 1992f0e31ae972320f80f99d94164fbd1dbc6d45
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395739"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="fee57-102">StyleSheets_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="fee57-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fee57-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="fee57-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fee57-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fee57-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fee57-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fee57-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fee57-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fee57-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fee57-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="fee57-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fee57-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fee57-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fee57-109">Definição</span><span class="sxs-lookup"><span data-stu-id="fee57-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fee57-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fee57-110">Elements and attributes</span></span>

<span data-ttu-id="fee57-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fee57-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fee57-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fee57-112">Child elements</span></span>

|<span data-ttu-id="fee57-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fee57-113">**Element**</span></span>|<span data-ttu-id="fee57-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fee57-114">**Type**</span></span>|<span data-ttu-id="fee57-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fee57-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fee57-116">Folha de estilos</span><span class="sxs-lookup"><span data-stu-id="fee57-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fee57-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="fee57-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fee57-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="fee57-118">Attributes</span></span>

<span data-ttu-id="fee57-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="fee57-119">None.</span></span>
  

