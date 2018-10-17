---
title: Elemento EventList (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contém um elemento EventItem para cada evento ao qual um objeto deve responder.
ms.openlocfilehash: 5331f1b4a510b05b862f8c7c6306c89c6be4d9f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383972"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="6291c-103">Elemento EventList (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="6291c-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6291c-104">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="6291c-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6291c-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="6291c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6291c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6291c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6291c-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="6291c-107">EventList_Type complexType</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6291c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6291c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6291c-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6291c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6291c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6291c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6291c-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6291c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6291c-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="6291c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6291c-113">Definição</span><span class="sxs-lookup"><span data-stu-id="6291c-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6291c-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6291c-114">Elements and attributes</span></span>

<span data-ttu-id="6291c-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6291c-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6291c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6291c-116">Parent elements</span></span>

|<span data-ttu-id="6291c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6291c-117">**Element**</span></span>|<span data-ttu-id="6291c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6291c-118">**Type**</span></span>|<span data-ttu-id="6291c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6291c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6291c-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="6291c-120">VisioDocument element</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="6291c-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="6291c-121">VisioDocument_Type complexType</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6291c-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="6291c-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6291c-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6291c-123">Child elements</span></span>

|<span data-ttu-id="6291c-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6291c-124">**Element**</span></span>|<span data-ttu-id="6291c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6291c-125">**Type**</span></span>|<span data-ttu-id="6291c-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6291c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6291c-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="6291c-127">EventItem element</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6291c-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="6291c-128">EventItem_Type complexType</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6291c-129">Encapsula um código de evento.</span><span class="sxs-lookup"><span data-stu-id="6291c-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6291c-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="6291c-130">Attributes</span></span>

<span data-ttu-id="6291c-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6291c-131">None.</span></span>
  

