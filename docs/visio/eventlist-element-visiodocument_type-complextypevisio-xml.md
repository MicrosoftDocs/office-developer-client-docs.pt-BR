---
title: Elemento de EventList (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contém um elemento EventItem para cada evento ao qual um objeto deve responder.
ms.openlocfilehash: e1033ae93ca272b8ea1d9855d08ad13a444612db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771814"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="8e6da-103">Elemento de EventList (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8e6da-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8e6da-104">Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.</span><span class="sxs-lookup"><span data-stu-id="8e6da-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8e6da-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="8e6da-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e6da-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8e6da-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8e6da-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="8e6da-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8e6da-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8e6da-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8e6da-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8e6da-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8e6da-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8e6da-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8e6da-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="8e6da-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8e6da-112">Document</span><span class="sxs-lookup"><span data-stu-id="8e6da-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8e6da-113">Definição</span><span class="sxs-lookup"><span data-stu-id="8e6da-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8e6da-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8e6da-114">Elements and attributes</span></span>

<span data-ttu-id="8e6da-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8e6da-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8e6da-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8e6da-116">Parent elements</span></span>

|<span data-ttu-id="8e6da-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e6da-117">**Element**</span></span>|<span data-ttu-id="8e6da-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8e6da-118">**Type**</span></span>|<span data-ttu-id="8e6da-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e6da-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8e6da-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="8e6da-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="8e6da-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="8e6da-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8e6da-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="8e6da-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8e6da-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8e6da-123">Child elements</span></span>

|<span data-ttu-id="8e6da-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e6da-124">**Element**</span></span>|<span data-ttu-id="8e6da-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8e6da-125">**Type**</span></span>|<span data-ttu-id="8e6da-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e6da-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8e6da-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="8e6da-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8e6da-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="8e6da-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8e6da-129">Encapsula um código de evento.</span><span class="sxs-lookup"><span data-stu-id="8e6da-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8e6da-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e6da-130">Attributes</span></span>

<span data-ttu-id="8e6da-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8e6da-131">None.</span></span>
  

