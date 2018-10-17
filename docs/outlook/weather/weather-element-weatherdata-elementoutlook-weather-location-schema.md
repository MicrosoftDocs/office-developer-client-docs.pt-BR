---
title: Elemento weather (elemento weatherdata) (Esquema de localização do clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Especifica o local para o qual informar o clima.
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398294"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="ad31e-103">Elemento weather (elemento weatherdata) (Esquema de localização do clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="ad31e-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="ad31e-104">Especifica o local para o qual informar o clima.</span><span class="sxs-lookup"><span data-stu-id="ad31e-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad31e-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="ad31e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad31e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ad31e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad31e-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="ad31e-107">weatherType complexType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="ad31e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad31e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="ad31e-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ad31e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad31e-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="ad31e-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad31e-111">Definição</span><span class="sxs-lookup"><span data-stu-id="ad31e-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad31e-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ad31e-112">Elements and attributes</span></span>

<span data-ttu-id="ad31e-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ad31e-113">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad31e-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ad31e-114">Parent elements</span></span>

|<span data-ttu-id="ad31e-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad31e-115">**Element**</span></span>|<span data-ttu-id="ad31e-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad31e-116">**Type**</span></span>|<span data-ttu-id="ad31e-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ad31e-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad31e-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="ad31e-118">weatherdata element</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="ad31e-119">Define o elemento do clima.</span><span class="sxs-lookup"><span data-stu-id="ad31e-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad31e-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ad31e-120">Child elements</span></span>

<span data-ttu-id="ad31e-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ad31e-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad31e-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad31e-122">Attributes</span></span>

|<span data-ttu-id="ad31e-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ad31e-123">**Attribute**</span></span>|<span data-ttu-id="ad31e-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad31e-124">**Type**</span></span>|<span data-ttu-id="ad31e-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ad31e-125">**Required**</span></span>|<span data-ttu-id="ad31e-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ad31e-126">**Description**</span></span>|<span data-ttu-id="ad31e-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ad31e-127">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad31e-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="ad31e-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="ad31e-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="ad31e-129">xs:string</span></span>  <br/> |<span data-ttu-id="ad31e-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ad31e-130">required</span></span>  <br/> |<span data-ttu-id="ad31e-131">Especifica um código associado ao local para distinguir vários locais com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ad31e-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="ad31e-132">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="ad31e-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ad31e-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="ad31e-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="ad31e-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="ad31e-134">xs:string</span></span>  <br/> |<span data-ttu-id="ad31e-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ad31e-135">required</span></span>  <br/> |<span data-ttu-id="ad31e-136">Especifica o nome do local.</span><span class="sxs-lookup"><span data-stu-id="ad31e-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="ad31e-137">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="ad31e-137">A value of the type xs:string</span></span>  <br/> |
   

