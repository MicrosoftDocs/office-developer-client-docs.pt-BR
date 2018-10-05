---
title: PublishSettings_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cf14299e-8d21-0eed-bbd7-ad33d4f03533
ms.openlocfilehash: eaa4bba1c5772b11fdbd2ec1c975f475e1c5d57a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383496"
---
# <a name="publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="620f6-102">PublishSettings_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="620f6-102">PublishSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="620f6-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="620f6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="620f6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="620f6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="620f6-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="620f6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="620f6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="620f6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="620f6-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="620f6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="620f6-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="620f6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="620f6-109">Definição</span><span class="sxs-lookup"><span data-stu-id="620f6-109">Definition</span></span>

```XML
          <xs:complexType name="PublishSettings_Type">
          
          <xs:sequence>
    <xs:element name="PublishedPage"  type="PublishedPage_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshableData"  type="RefreshableData_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="620f6-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="620f6-110">Elements and attributes</span></span>

<span data-ttu-id="620f6-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="620f6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="620f6-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="620f6-112">Child elements</span></span>

|<span data-ttu-id="620f6-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="620f6-113">**Element**</span></span>|<span data-ttu-id="620f6-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="620f6-114">**Type**</span></span>|<span data-ttu-id="620f6-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="620f6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="620f6-116">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="620f6-116">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="620f6-117">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="620f6-117">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="620f6-118">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="620f6-118">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="620f6-119">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="620f6-119">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="620f6-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="620f6-120">Attributes</span></span>

<span data-ttu-id="620f6-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="620f6-121">None.</span></span>
  

