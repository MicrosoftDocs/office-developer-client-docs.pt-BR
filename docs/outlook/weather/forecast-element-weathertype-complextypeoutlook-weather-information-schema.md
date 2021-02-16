---
title: Elemento forecast (weatherType complexType) (Esquema de informações sobre o clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: Especifica as condições meteorológicas futuras para pelo menos três dias, incluindo hoje, amanhã, depois de amanhã.
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540977"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="afe79-103">Elemento forecast (weatherType complexType) (Esquema de informações sobre o clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="afe79-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="afe79-104">Especifica as condições meteorológicas futuras para pelo menos três dias, incluindo hoje, amanhã, depois de amanhã.</span><span class="sxs-lookup"><span data-stu-id="afe79-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afe79-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="afe79-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afe79-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="afe79-106">**Element type**</span></span> <br/> |[<span data-ttu-id="afe79-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="afe79-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="afe79-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="afe79-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="afe79-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="afe79-109">**Schema file**</span></span> <br/> |<span data-ttu-id="afe79-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="afe79-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="afe79-111">Definição</span><span class="sxs-lookup"><span data-stu-id="afe79-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="afe79-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="afe79-112">Elements and attributes</span></span>

<span data-ttu-id="afe79-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="afe79-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="afe79-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="afe79-114">Parent elements</span></span>

|<span data-ttu-id="afe79-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="afe79-115">**Element**</span></span>|<span data-ttu-id="afe79-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="afe79-116">**Type**</span></span>|<span data-ttu-id="afe79-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="afe79-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="afe79-118">clima</span><span class="sxs-lookup"><span data-stu-id="afe79-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="afe79-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="afe79-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="afe79-120">Especifica as condições meteorológicas de um local.</span><span class="sxs-lookup"><span data-stu-id="afe79-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="afe79-121">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="afe79-121">Child elements</span></span>

<span data-ttu-id="afe79-122">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="afe79-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afe79-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="afe79-123">Attributes</span></span>

|<span data-ttu-id="afe79-124">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="afe79-124">**Attribute**</span></span>|<span data-ttu-id="afe79-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="afe79-125">**Type**</span></span>|<span data-ttu-id="afe79-126">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="afe79-126">**Required**</span></span>|<span data-ttu-id="afe79-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="afe79-127">**Description**</span></span>|<span data-ttu-id="afe79-128">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="afe79-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="afe79-129">data</span><span class="sxs-lookup"><span data-stu-id="afe79-129">date</span></span>  <br/> |<span data-ttu-id="afe79-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="afe79-130">xs:date</span></span>  <br/> |<span data-ttu-id="afe79-131">obrigatório</span><span class="sxs-lookup"><span data-stu-id="afe79-131">required</span></span>  <br/> |<span data-ttu-id="afe79-132">Especifica a data da previsão.</span><span class="sxs-lookup"><span data-stu-id="afe79-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="afe79-133">Um valor do tipo xs:date</span><span class="sxs-lookup"><span data-stu-id="afe79-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="afe79-134">dia</span><span class="sxs-lookup"><span data-stu-id="afe79-134">day</span></span>  <br/> |<span data-ttu-id="afe79-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="afe79-135">xs:string</span></span>  <br/> |<span data-ttu-id="afe79-136">obrigatório</span><span class="sxs-lookup"><span data-stu-id="afe79-136">required</span></span>  <br/> |<span data-ttu-id="afe79-137">Especifica um dia para a previsão.</span><span class="sxs-lookup"><span data-stu-id="afe79-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="afe79-138">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="afe79-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="afe79-139">high</span><span class="sxs-lookup"><span data-stu-id="afe79-139">high</span></span>  <br/> |<span data-ttu-id="afe79-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="afe79-140">xs:integer</span></span>  <br/> |<span data-ttu-id="afe79-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="afe79-141">required</span></span>  <br/> |<span data-ttu-id="afe79-142">Especifica a maior temperatura prevista.</span><span class="sxs-lookup"><span data-stu-id="afe79-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="afe79-143">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="afe79-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="afe79-144">low</span><span class="sxs-lookup"><span data-stu-id="afe79-144">low</span></span>  <br/> |<span data-ttu-id="afe79-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="afe79-145">xs:integer</span></span>  <br/> |<span data-ttu-id="afe79-146">obrigatório</span><span class="sxs-lookup"><span data-stu-id="afe79-146">required</span></span>  <br/> |<span data-ttu-id="afe79-147">Especifica a menor temperatura prevista.</span><span class="sxs-lookup"><span data-stu-id="afe79-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="afe79-148">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="afe79-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="afe79-149">precip</span><span class="sxs-lookup"><span data-stu-id="afe79-149">precip</span></span>  <br/> |<span data-ttu-id="afe79-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="afe79-150">xs:integer</span></span>  <br/> |<span data-ttu-id="afe79-151">obrigatório</span><span class="sxs-lookup"><span data-stu-id="afe79-151">required</span></span>  <br/> |<span data-ttu-id="afe79-152">Especifica a porcentagem de possibilidade de precipitação.</span><span class="sxs-lookup"><span data-stu-id="afe79-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="afe79-153">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="afe79-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="afe79-154">shortday</span><span class="sxs-lookup"><span data-stu-id="afe79-154">shortday</span></span>  <br/> |<span data-ttu-id="afe79-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="afe79-155">xs:string</span></span>  <br/> |<span data-ttu-id="afe79-156">obrigatório</span><span class="sxs-lookup"><span data-stu-id="afe79-156">required</span></span>  <br/> |<span data-ttu-id="afe79-157">Especifica um dia na forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="afe79-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="afe79-158">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="afe79-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="afe79-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="afe79-159">skycodeday</span></span>  <br/> |<span data-ttu-id="afe79-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="afe79-160">xs:integer</span></span>  <br/> |<span data-ttu-id="afe79-161">obrigatório</span><span class="sxs-lookup"><span data-stu-id="afe79-161">required</span></span>  <br/> |<span data-ttu-id="afe79-162">Especifica um código para as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="afe79-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="afe79-163">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="afe79-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="afe79-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="afe79-164">skytextday</span></span>  <br/> |<span data-ttu-id="afe79-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="afe79-165">xs:string</span></span>  <br/> |<span data-ttu-id="afe79-166">obrigatório</span><span class="sxs-lookup"><span data-stu-id="afe79-166">required</span></span>  <br/> |<span data-ttu-id="afe79-167">Especifica uma ou duas palavras que descrevam as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="afe79-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="afe79-168">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="afe79-168">A value of the type xs:string</span></span>  <br/> |
   

