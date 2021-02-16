---
title: VisioDocument_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: 8c0a5976139aee2f3aee41b3709ce5fd1ac5c00d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538470"
---
# <a name="visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="5881a-102">VisioDocument_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="5881a-102">VisioDocument_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5881a-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="5881a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5881a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5881a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5881a-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5881a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5881a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5881a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5881a-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="5881a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5881a-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5881a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5881a-109">Definição</span><span class="sxs-lookup"><span data-stu-id="5881a-109">Definition</span></span>

```XML
          <xs:complexType name="VisioDocument_Type">
          
          <xs:sequence>
    <xs:element name="DocumentSettings"  type="DocumentSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Colors"  type="Colors_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FaceNames"  type="FaceNames_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StyleSheets"  type="StyleSheets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DocumentSheet"  type="DocumentSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="EventList"  type="EventList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooter"  type="HeaderFooter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PublishSettings"  type="PublishSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5881a-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5881a-110">Elements and attributes</span></span>

<span data-ttu-id="5881a-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5881a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5881a-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5881a-112">Child elements</span></span>

|<span data-ttu-id="5881a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5881a-113">**Element**</span></span>|<span data-ttu-id="5881a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5881a-114">**Type**</span></span>|<span data-ttu-id="5881a-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5881a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5881a-116">Colors</span><span class="sxs-lookup"><span data-stu-id="5881a-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5881a-117">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="5881a-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5881a-118">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="5881a-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5881a-119">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5881a-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5881a-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="5881a-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5881a-121">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="5881a-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5881a-122">EventList</span><span class="sxs-lookup"><span data-stu-id="5881a-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5881a-123">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="5881a-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5881a-124">FaceNames</span><span class="sxs-lookup"><span data-stu-id="5881a-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5881a-125">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="5881a-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5881a-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="5881a-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5881a-127">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="5881a-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5881a-128">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="5881a-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5881a-129">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5881a-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5881a-130">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="5881a-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5881a-131">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="5881a-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5881a-132">Atributos</span><span class="sxs-lookup"><span data-stu-id="5881a-132">Attributes</span></span>

<span data-ttu-id="5881a-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5881a-133">None.</span></span>
  

