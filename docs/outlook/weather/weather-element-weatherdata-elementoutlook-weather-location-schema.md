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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355206"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="7a3dc-103">Elemento weather (elemento weatherdata) (Esquema de localização do clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="7a3dc-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="7a3dc-104">Especifica o local para o qual informar o clima.</span><span class="sxs-lookup"><span data-stu-id="7a3dc-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a3dc-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="7a3dc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a3dc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7a3dc-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="7a3dc-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="7a3dc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="7a3dc-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7a3dc-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="7a3dc-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7a3dc-111">Definição</span><span class="sxs-lookup"><span data-stu-id="7a3dc-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="7a3dc-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7a3dc-112">Elements and attributes</span></span>

<span data-ttu-id="7a3dc-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7a3dc-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7a3dc-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7a3dc-114">Parent elements</span></span>

|<span data-ttu-id="7a3dc-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-115">**Element**</span></span>|<span data-ttu-id="7a3dc-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-116">**Type**</span></span>|<span data-ttu-id="7a3dc-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7a3dc-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="7a3dc-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="7a3dc-119">Define o elemento do clima.</span><span class="sxs-lookup"><span data-stu-id="7a3dc-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7a3dc-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7a3dc-120">Child elements</span></span>

<span data-ttu-id="7a3dc-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7a3dc-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a3dc-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="7a3dc-122">Attributes</span></span>

|<span data-ttu-id="7a3dc-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-123">**Attribute**</span></span>|<span data-ttu-id="7a3dc-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-124">**Type**</span></span>|<span data-ttu-id="7a3dc-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-125">**Required**</span></span>|<span data-ttu-id="7a3dc-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-126">**Description**</span></span>|<span data-ttu-id="7a3dc-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7a3dc-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7a3dc-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="7a3dc-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="7a3dc-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="7a3dc-129">xs:string</span></span>  <br/> |<span data-ttu-id="7a3dc-130">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7a3dc-130">required</span></span>  <br/> |<span data-ttu-id="7a3dc-131">Especifica um código associado ao local para distinguir vários locais com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="7a3dc-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="7a3dc-132">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="7a3dc-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7a3dc-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="7a3dc-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="7a3dc-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="7a3dc-134">xs:string</span></span>  <br/> |<span data-ttu-id="7a3dc-135">obrigatório</span><span class="sxs-lookup"><span data-stu-id="7a3dc-135">required</span></span>  <br/> |<span data-ttu-id="7a3dc-136">Especifica o nome do local.</span><span class="sxs-lookup"><span data-stu-id="7a3dc-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="7a3dc-137">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="7a3dc-137">A value of the type xs:string</span></span>  <br/> |
   

