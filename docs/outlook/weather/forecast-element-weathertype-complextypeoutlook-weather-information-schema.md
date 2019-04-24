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
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339561"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="8524a-103">Elemento forecast (weatherType complexType) (Esquema de informações sobre o clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="8524a-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="8524a-104">Especifica as condições meteorológicas futuras para pelo menos três dias, incluindo hoje, amanhã, depois de amanhã.</span><span class="sxs-lookup"><span data-stu-id="8524a-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8524a-105">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8524a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8524a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8524a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8524a-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="8524a-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="8524a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8524a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="8524a-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8524a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8524a-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="8524a-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8524a-111">Definição</span><span class="sxs-lookup"><span data-stu-id="8524a-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="8524a-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="8524a-112">Elements and attributes</span></span>

<span data-ttu-id="8524a-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="8524a-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8524a-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8524a-114">Parent elements</span></span>

|<span data-ttu-id="8524a-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8524a-115">**Element**</span></span>|<span data-ttu-id="8524a-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8524a-116">**Type**</span></span>|<span data-ttu-id="8524a-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8524a-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8524a-118">clima</span><span class="sxs-lookup"><span data-stu-id="8524a-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="8524a-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="8524a-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="8524a-120">Especifica as condições meteorológicas de um local.</span><span class="sxs-lookup"><span data-stu-id="8524a-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8524a-121">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8524a-121">Child elements</span></span>

<span data-ttu-id="8524a-122">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8524a-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8524a-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="8524a-123">Attributes</span></span>

|<span data-ttu-id="8524a-124">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8524a-124">**Attribute**</span></span>|<span data-ttu-id="8524a-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8524a-125">**Type**</span></span>|<span data-ttu-id="8524a-126">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8524a-126">**Required**</span></span>|<span data-ttu-id="8524a-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8524a-127">**Description**</span></span>|<span data-ttu-id="8524a-128">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="8524a-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8524a-129">data</span><span class="sxs-lookup"><span data-stu-id="8524a-129">date</span></span>  <br/> |<span data-ttu-id="8524a-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="8524a-130">xs:date</span></span>  <br/> |<span data-ttu-id="8524a-131">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8524a-131">required</span></span>  <br/> |<span data-ttu-id="8524a-132">Especifica a data da previsão.</span><span class="sxs-lookup"><span data-stu-id="8524a-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="8524a-133">Um valor do tipo xs:date</span><span class="sxs-lookup"><span data-stu-id="8524a-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="8524a-134">dia</span><span class="sxs-lookup"><span data-stu-id="8524a-134">day</span></span>  <br/> |<span data-ttu-id="8524a-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="8524a-135">xs:string</span></span>  <br/> |<span data-ttu-id="8524a-136">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8524a-136">required</span></span>  <br/> |<span data-ttu-id="8524a-137">Especifica um dia para a previsão.</span><span class="sxs-lookup"><span data-stu-id="8524a-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="8524a-138">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="8524a-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="8524a-139">high</span><span class="sxs-lookup"><span data-stu-id="8524a-139">high</span></span>  <br/> |<span data-ttu-id="8524a-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8524a-140">xs:integer</span></span>  <br/> |<span data-ttu-id="8524a-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8524a-141">required</span></span>  <br/> |<span data-ttu-id="8524a-142">Especifica a maior temperatura prevista.</span><span class="sxs-lookup"><span data-stu-id="8524a-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="8524a-143">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="8524a-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="8524a-144">low</span><span class="sxs-lookup"><span data-stu-id="8524a-144">low</span></span>  <br/> |<span data-ttu-id="8524a-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8524a-145">xs:integer</span></span>  <br/> |<span data-ttu-id="8524a-146">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8524a-146">required</span></span>  <br/> |<span data-ttu-id="8524a-147">Especifica a menor temperatura prevista.</span><span class="sxs-lookup"><span data-stu-id="8524a-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="8524a-148">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="8524a-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="8524a-149">precip</span><span class="sxs-lookup"><span data-stu-id="8524a-149">precip</span></span>  <br/> |<span data-ttu-id="8524a-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8524a-150">xs:integer</span></span>  <br/> |<span data-ttu-id="8524a-151">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8524a-151">required</span></span>  <br/> |<span data-ttu-id="8524a-152">Especifica a porcentagem de possibilidade de precipitação.</span><span class="sxs-lookup"><span data-stu-id="8524a-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="8524a-153">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="8524a-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="8524a-154">shortday</span><span class="sxs-lookup"><span data-stu-id="8524a-154">shortday</span></span>  <br/> |<span data-ttu-id="8524a-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="8524a-155">xs:string</span></span>  <br/> |<span data-ttu-id="8524a-156">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8524a-156">required</span></span>  <br/> |<span data-ttu-id="8524a-157">Especifica um dia na forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="8524a-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="8524a-158">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="8524a-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="8524a-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="8524a-159">skycodeday</span></span>  <br/> |<span data-ttu-id="8524a-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8524a-160">xs:integer</span></span>  <br/> |<span data-ttu-id="8524a-161">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8524a-161">required</span></span>  <br/> |<span data-ttu-id="8524a-162">Especifica um código para as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="8524a-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="8524a-163">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="8524a-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="8524a-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="8524a-164">skytextday</span></span>  <br/> |<span data-ttu-id="8524a-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="8524a-165">xs:string</span></span>  <br/> |<span data-ttu-id="8524a-166">obrigatório</span><span class="sxs-lookup"><span data-stu-id="8524a-166">required</span></span>  <br/> |<span data-ttu-id="8524a-167">Especifica uma ou duas palavras que descrevam as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="8524a-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="8524a-168">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="8524a-168">A value of the type xs:string</span></span>  <br/> |
   

