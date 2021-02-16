---
title: Elemento weather (elemento weatherdata) (Esquema de informações sobre o clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Especifica as condições meteorológicas de um local.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541264"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="3df45-103">Elemento weather (elemento weatherdata) (Esquema de informações sobre o clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="3df45-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="3df45-104">Especifica as condições meteorológicas de um local.</span><span class="sxs-lookup"><span data-stu-id="3df45-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3df45-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="3df45-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3df45-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3df45-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3df45-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="3df45-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="3df45-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3df45-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="3df45-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3df45-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3df45-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="3df45-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3df45-111">Definição</span><span class="sxs-lookup"><span data-stu-id="3df45-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="3df45-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3df45-112">Elements and attributes</span></span>

<span data-ttu-id="3df45-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3df45-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3df45-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3df45-114">Parent elements</span></span>

|<span data-ttu-id="3df45-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3df45-115">**Element**</span></span>|<span data-ttu-id="3df45-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3df45-116">**Type**</span></span>|<span data-ttu-id="3df45-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3df45-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3df45-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="3df45-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="3df45-119">Define o elemento do clima.</span><span class="sxs-lookup"><span data-stu-id="3df45-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3df45-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3df45-120">Child elements</span></span>

|<span data-ttu-id="3df45-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3df45-121">**Element**</span></span>|<span data-ttu-id="3df45-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3df45-122">**Type**</span></span>|<span data-ttu-id="3df45-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3df45-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3df45-124">current</span><span class="sxs-lookup"><span data-stu-id="3df45-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="3df45-125">currentType</span><span class="sxs-lookup"><span data-stu-id="3df45-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="3df45-126">Especifica as condições meteorológicas atuais.</span><span class="sxs-lookup"><span data-stu-id="3df45-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="3df45-127">forecast</span><span class="sxs-lookup"><span data-stu-id="3df45-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="3df45-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="3df45-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="3df45-129">Especifica as condições meteorológicas futuras para pelo menos três dias, incluindo hoje, amanhã, depois de amanhã.</span><span class="sxs-lookup"><span data-stu-id="3df45-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3df45-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="3df45-130">Attributes</span></span>

|<span data-ttu-id="3df45-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3df45-131">**Attribute**</span></span>|<span data-ttu-id="3df45-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3df45-132">**Type**</span></span>|<span data-ttu-id="3df45-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3df45-133">**Required**</span></span>|<span data-ttu-id="3df45-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3df45-134">**Description**</span></span>|<span data-ttu-id="3df45-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3df45-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3df45-136">attribution</span><span class="sxs-lookup"><span data-stu-id="3df45-136">attribution</span></span>  <br/> |<span data-ttu-id="3df45-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-137">xs:string</span></span>  <br/> |<span data-ttu-id="3df45-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3df45-138">required</span></span>  <br/> |<span data-ttu-id="3df45-139">Especifica a origem das informações meteorológicas.</span><span class="sxs-lookup"><span data-stu-id="3df45-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="3df45-140">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="3df45-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="3df45-141">degreetype</span></span>  <br/> |<span data-ttu-id="3df45-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-142">xs:string</span></span>  <br/> |<span data-ttu-id="3df45-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3df45-143">required</span></span>  <br/> |<span data-ttu-id="3df45-144">Especifica a unidade de temperatura local, como Celsius.</span><span class="sxs-lookup"><span data-stu-id="3df45-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="3df45-145">C, F</span><span class="sxs-lookup"><span data-stu-id="3df45-145">C, F</span></span>  <br/> |
|<span data-ttu-id="3df45-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="3df45-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="3df45-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-147">xs:string</span></span>  <br/> |<span data-ttu-id="3df45-148">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3df45-148">required</span></span>  <br/> |<span data-ttu-id="3df45-149">Especifica a URL da imagem para o local.</span><span class="sxs-lookup"><span data-stu-id="3df45-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="3df45-150">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="3df45-151">timezone</span><span class="sxs-lookup"><span data-stu-id="3df45-151">timezone</span></span>  <br/> |<span data-ttu-id="3df45-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3df45-152">xs:integer</span></span>  <br/> |<span data-ttu-id="3df45-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3df45-153">required</span></span>  <br/> |<span data-ttu-id="3df45-154">Especifica o deslocamento GMT.</span><span class="sxs-lookup"><span data-stu-id="3df45-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="3df45-155">Um valor entre -11 e 12, inclusive</span><span class="sxs-lookup"><span data-stu-id="3df45-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="3df45-156">url</span><span class="sxs-lookup"><span data-stu-id="3df45-156">url</span></span>  <br/> |<span data-ttu-id="3df45-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-157">xs:string</span></span>  <br/> |<span data-ttu-id="3df45-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3df45-158">required</span></span>  <br/> |<span data-ttu-id="3df45-159">Especifica a URL para a página da Web do serviço meteorológico que contém informações sobre o clima para o local especificado.</span><span class="sxs-lookup"><span data-stu-id="3df45-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="3df45-160">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="3df45-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="3df45-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="3df45-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-162">xs:string</span></span>  <br/> |<span data-ttu-id="3df45-163">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3df45-163">required</span></span>  <br/> |<span data-ttu-id="3df45-164">Especifica o código associado ao local usado para distinguir vários locais que tenham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="3df45-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="3df45-165">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="3df45-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="3df45-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="3df45-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-167">xs:string</span></span>  <br/> |<span data-ttu-id="3df45-168">obrigatório</span><span class="sxs-lookup"><span data-stu-id="3df45-168">required</span></span>  <br/> |<span data-ttu-id="3df45-169">Especifica o nome do local exibido no controle suspenso.</span><span class="sxs-lookup"><span data-stu-id="3df45-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="3df45-170">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="3df45-170">A value of the type xs:string</span></span>  <br/> |
   

