---
title: PublishSettings_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cf14299e-8d21-0eed-bbd7-ad33d4f03533
ms.openlocfilehash: 6e9974d35b904581d43f481a02b8a3adee811730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772622"
---
# <a name="publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="b172e-102">PublishSettings_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="b172e-102">PublishSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b172e-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="b172e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b172e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b172e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b172e-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b172e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b172e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b172e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b172e-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="b172e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b172e-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b172e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b172e-109">Definição</span><span class="sxs-lookup"><span data-stu-id="b172e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b172e-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b172e-110">Elements and attributes</span></span>

<span data-ttu-id="b172e-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b172e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b172e-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b172e-112">Child elements</span></span>

|<span data-ttu-id="b172e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b172e-113">**Element**</span></span>|<span data-ttu-id="b172e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b172e-114">**Type**</span></span>|<span data-ttu-id="b172e-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b172e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b172e-116">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="b172e-116">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b172e-117">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="b172e-117">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b172e-118">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="b172e-118">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b172e-119">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="b172e-119">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b172e-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="b172e-120">Attributes</span></span>

<span data-ttu-id="b172e-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b172e-121">None.</span></span>
  

