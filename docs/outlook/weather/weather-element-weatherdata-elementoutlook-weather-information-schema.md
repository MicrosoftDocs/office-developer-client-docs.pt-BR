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
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390657"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="cc2b9-103">Elemento weather (elemento weatherdata) (Esquema de informações sobre o clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="cc2b9-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="cc2b9-104">Especifica as condições meteorológicas de um local.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc2b9-105">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cc2b9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc2b9-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cc2b9-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="cc2b9-107">weatherType complexType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="cc2b9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="cc2b9-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cc2b9-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="cc2b9-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc2b9-111">Definição</span><span class="sxs-lookup"><span data-stu-id="cc2b9-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc2b9-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cc2b9-112">Elements and attributes</span></span>

<span data-ttu-id="cc2b9-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-113">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cc2b9-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="cc2b9-114">Parent elements</span></span>

|<span data-ttu-id="cc2b9-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-115">**Element**</span></span>|<span data-ttu-id="cc2b9-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-116">**Type**</span></span>|<span data-ttu-id="cc2b9-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc2b9-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="cc2b9-118">weatherdata element</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="cc2b9-119">Define o elemento do clima.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cc2b9-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cc2b9-120">Child elements</span></span>

|<span data-ttu-id="cc2b9-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-121">**Element**</span></span>|<span data-ttu-id="cc2b9-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-122">**Type**</span></span>|<span data-ttu-id="cc2b9-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc2b9-124">current</span><span class="sxs-lookup"><span data-stu-id="cc2b9-124">Current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="cc2b9-125">currentType</span><span class="sxs-lookup"><span data-stu-id="cc2b9-125">currentType complexType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="cc2b9-126">Especifica as condições meteorológicas atuais.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="cc2b9-127">forecast</span><span class="sxs-lookup"><span data-stu-id="cc2b9-127">Forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="cc2b9-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="cc2b9-128">forecastType complexType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="cc2b9-129">Especifica as condições meteorológicas futuras para pelo menos três dias, incluindo hoje, amanhã, depois de amanhã.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cc2b9-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc2b9-130">Attributes</span></span>

|<span data-ttu-id="cc2b9-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-131">**Attribute**</span></span>|<span data-ttu-id="cc2b9-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-132">**Type**</span></span>|<span data-ttu-id="cc2b9-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-133">**Required**</span></span>|<span data-ttu-id="cc2b9-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-134">**Description**</span></span>|<span data-ttu-id="cc2b9-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="cc2b9-135">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cc2b9-136">attribution</span><span class="sxs-lookup"><span data-stu-id="cc2b9-136">attribution</span></span>  <br/> |<span data-ttu-id="cc2b9-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-137">xs:string</span></span>  <br/> |<span data-ttu-id="cc2b9-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc2b9-138">required</span></span>  <br/> |<span data-ttu-id="cc2b9-139">Especifica a origem das informações meteorológicas.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="cc2b9-140">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cc2b9-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="cc2b9-141">weadegreetype= degreetype</span></span>  <br/> |<span data-ttu-id="cc2b9-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-142">xs:string</span></span>  <br/> |<span data-ttu-id="cc2b9-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc2b9-143">required</span></span>  <br/> |<span data-ttu-id="cc2b9-144">Especifica a unidade de temperatura local, como Celsius.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="cc2b9-145">C, F</span><span class="sxs-lookup"><span data-stu-id="cc2b9-145">C, F</span></span>  <br/> |
|<span data-ttu-id="cc2b9-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="cc2b9-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="cc2b9-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-147">xs:string</span></span>  <br/> |<span data-ttu-id="cc2b9-148">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc2b9-148">required</span></span>  <br/> |<span data-ttu-id="cc2b9-149">Especifica a URL da imagem para o local.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-149">Specifies the URL of the home page for the dictionary.</span></span>  <br/> |<span data-ttu-id="cc2b9-150">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cc2b9-151">timezone</span><span class="sxs-lookup"><span data-stu-id="cc2b9-151">timeZone</span></span>  <br/> |<span data-ttu-id="cc2b9-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cc2b9-152">xs:integer</span></span>  <br/> |<span data-ttu-id="cc2b9-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc2b9-153">required</span></span>  <br/> |<span data-ttu-id="cc2b9-154">Especifica o deslocamento GMT.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="cc2b9-155">Um valor entre -11 e 12, inclusive</span><span class="sxs-lookup"><span data-stu-id="cc2b9-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="cc2b9-156">url</span><span class="sxs-lookup"><span data-stu-id="cc2b9-156">url</span></span>  <br/> |<span data-ttu-id="cc2b9-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-157">xs:string</span></span>  <br/> |<span data-ttu-id="cc2b9-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc2b9-158">required</span></span>  <br/> |<span data-ttu-id="cc2b9-159">Especifica a URL para a página da Web do serviço meteorológico que contém informações sobre o clima para o local especificado.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="cc2b9-160">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cc2b9-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="cc2b9-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="cc2b9-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-162">xs:string</span></span>  <br/> |<span data-ttu-id="cc2b9-163">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc2b9-163">required</span></span>  <br/> |<span data-ttu-id="cc2b9-164">Especifica o código associado ao local usado para distinguir vários locais que tenham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="cc2b9-165">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cc2b9-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="cc2b9-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="cc2b9-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-167">xs:string</span></span>  <br/> |<span data-ttu-id="cc2b9-168">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc2b9-168">required</span></span>  <br/> |<span data-ttu-id="cc2b9-169">Especifica o nome do local exibido no controle suspenso.</span><span class="sxs-lookup"><span data-stu-id="cc2b9-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="cc2b9-170">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cc2b9-170">A value of the type xs:string</span></span>  <br/> |
   

