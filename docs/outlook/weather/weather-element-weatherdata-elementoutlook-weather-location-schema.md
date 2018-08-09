---
title: elemento de clima (weatherdata elemento) (esquema de local de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Especifica o local de clima de relatório no.
ms.openlocfilehash: a95e207845a9e54f5cac58b64ce85ec17b59fa22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771041"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="95cfa-103">elemento de clima (weatherdata elemento) (esquema de local de clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="95cfa-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="95cfa-104">Especifica o local de clima de relatório no.</span><span class="sxs-lookup"><span data-stu-id="95cfa-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95cfa-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="95cfa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95cfa-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="95cfa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95cfa-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="95cfa-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="95cfa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="95cfa-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="95cfa-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="95cfa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95cfa-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="95cfa-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95cfa-111">Definição</span><span class="sxs-lookup"><span data-stu-id="95cfa-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="95cfa-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="95cfa-112">Elements and attributes</span></span>

<span data-ttu-id="95cfa-113">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="95cfa-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95cfa-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="95cfa-114">Parent elements</span></span>

|<span data-ttu-id="95cfa-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95cfa-115">**Element**</span></span>|<span data-ttu-id="95cfa-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95cfa-116">**Type**</span></span>|<span data-ttu-id="95cfa-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95cfa-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95cfa-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="95cfa-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="95cfa-119">Define o elemento de clima.</span><span class="sxs-lookup"><span data-stu-id="95cfa-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95cfa-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="95cfa-120">Child elements</span></span>

<span data-ttu-id="95cfa-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="95cfa-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95cfa-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="95cfa-122">Attributes</span></span>

|<span data-ttu-id="95cfa-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="95cfa-123">**Attribute**</span></span>|<span data-ttu-id="95cfa-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95cfa-124">**Type**</span></span>|<span data-ttu-id="95cfa-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="95cfa-125">**Required**</span></span>|<span data-ttu-id="95cfa-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95cfa-126">**Description**</span></span>|<span data-ttu-id="95cfa-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="95cfa-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95cfa-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="95cfa-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="95cfa-129">xs: String</span><span class="sxs-lookup"><span data-stu-id="95cfa-129">xs:string</span></span>  <br/> |<span data-ttu-id="95cfa-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="95cfa-130">required</span></span>  <br/> |<span data-ttu-id="95cfa-131">Especifica um código que está associado ao local para distinguir vários locais com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="95cfa-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="95cfa-132">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="95cfa-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="95cfa-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="95cfa-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="95cfa-134">xs: String</span><span class="sxs-lookup"><span data-stu-id="95cfa-134">xs:string</span></span>  <br/> |<span data-ttu-id="95cfa-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="95cfa-135">required</span></span>  <br/> |<span data-ttu-id="95cfa-136">Especifica o nome do local.</span><span class="sxs-lookup"><span data-stu-id="95cfa-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="95cfa-137">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="95cfa-137">A value of the type xs:string</span></span>  <br/> |
   

