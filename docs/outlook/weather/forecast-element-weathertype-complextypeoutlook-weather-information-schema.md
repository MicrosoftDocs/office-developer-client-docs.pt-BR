---
title: previsão de elemento (weatherType complexType) (esquema de informações de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Especifica as condições de clima futuras de pelo menos três dias com antecedência incluindo hoje: hoje, amanhã, de depois de amanhã.'
ms.openlocfilehash: c618b753ddf8a72fce270800675982f1a7f7af5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770966"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="ac219-103">previsão de elemento (weatherType complexType) (esquema de informações de clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="ac219-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="ac219-104">Especifica as condições de clima futuras de pelo menos três dias com antecedência incluindo hoje: hoje, amanhã, de depois de amanhã.</span><span class="sxs-lookup"><span data-stu-id="ac219-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac219-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="ac219-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac219-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ac219-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ac219-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="ac219-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="ac219-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ac219-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="ac219-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ac219-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ac219-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="ac219-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ac219-111">Definição</span><span class="sxs-lookup"><span data-stu-id="ac219-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="ac219-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ac219-112">Elements and attributes</span></span>

<span data-ttu-id="ac219-113">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ac219-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ac219-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ac219-114">Parent elements</span></span>

|<span data-ttu-id="ac219-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ac219-115">**Element**</span></span>|<span data-ttu-id="ac219-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ac219-116">**Type**</span></span>|<span data-ttu-id="ac219-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ac219-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac219-118">clima</span><span class="sxs-lookup"><span data-stu-id="ac219-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="ac219-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="ac219-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="ac219-120">Especifica as condições de clima de um local.</span><span class="sxs-lookup"><span data-stu-id="ac219-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ac219-121">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ac219-121">Child elements</span></span>

<span data-ttu-id="ac219-122">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ac219-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac219-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac219-123">Attributes</span></span>

|<span data-ttu-id="ac219-124">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ac219-124">**Attribute**</span></span>|<span data-ttu-id="ac219-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ac219-125">**Type**</span></span>|<span data-ttu-id="ac219-126">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ac219-126">**Required**</span></span>|<span data-ttu-id="ac219-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ac219-127">**Description**</span></span>|<span data-ttu-id="ac219-128">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ac219-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ac219-129">data</span><span class="sxs-lookup"><span data-stu-id="ac219-129">date</span></span>  <br/> |<span data-ttu-id="ac219-130">Date</span><span class="sxs-lookup"><span data-stu-id="ac219-130">xs:date</span></span>  <br/> |<span data-ttu-id="ac219-131">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ac219-131">required</span></span>  <br/> |<span data-ttu-id="ac219-132">Especifica a data para a previsão.</span><span class="sxs-lookup"><span data-stu-id="ac219-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="ac219-133">Um valor de Date o tipo</span><span class="sxs-lookup"><span data-stu-id="ac219-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="ac219-134">dia</span><span class="sxs-lookup"><span data-stu-id="ac219-134">day</span></span>  <br/> |<span data-ttu-id="ac219-135">xs: String</span><span class="sxs-lookup"><span data-stu-id="ac219-135">xs:string</span></span>  <br/> |<span data-ttu-id="ac219-136">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ac219-136">required</span></span>  <br/> |<span data-ttu-id="ac219-137">Especifica um dia para a previsão.</span><span class="sxs-lookup"><span data-stu-id="ac219-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="ac219-138">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="ac219-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ac219-139">alta</span><span class="sxs-lookup"><span data-stu-id="ac219-139">high</span></span>  <br/> |<span data-ttu-id="ac219-140">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="ac219-140">xs:integer</span></span>  <br/> |<span data-ttu-id="ac219-141">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ac219-141">required</span></span>  <br/> |<span data-ttu-id="ac219-142">Especifica a temperatura mais alta prevista.</span><span class="sxs-lookup"><span data-stu-id="ac219-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="ac219-143">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="ac219-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ac219-144">baixa</span><span class="sxs-lookup"><span data-stu-id="ac219-144">low</span></span>  <br/> |<span data-ttu-id="ac219-145">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="ac219-145">xs:integer</span></span>  <br/> |<span data-ttu-id="ac219-146">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ac219-146">required</span></span>  <br/> |<span data-ttu-id="ac219-147">Especifica a temperatura mais baixa prevista.</span><span class="sxs-lookup"><span data-stu-id="ac219-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="ac219-148">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="ac219-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ac219-149">precip</span><span class="sxs-lookup"><span data-stu-id="ac219-149">precip</span></span>  <br/> |<span data-ttu-id="ac219-150">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="ac219-150">xs:integer</span></span>  <br/> |<span data-ttu-id="ac219-151">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ac219-151">required</span></span>  <br/> |<span data-ttu-id="ac219-152">Especifica a possibilidade de porcentagem de Precipitação.</span><span class="sxs-lookup"><span data-stu-id="ac219-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="ac219-153">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="ac219-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ac219-154">shortday</span><span class="sxs-lookup"><span data-stu-id="ac219-154">shortday</span></span>  <br/> |<span data-ttu-id="ac219-155">xs: String</span><span class="sxs-lookup"><span data-stu-id="ac219-155">xs:string</span></span>  <br/> |<span data-ttu-id="ac219-156">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ac219-156">required</span></span>  <br/> |<span data-ttu-id="ac219-157">Especifica um dia na forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="ac219-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="ac219-158">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="ac219-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ac219-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="ac219-159">skycodeday</span></span>  <br/> |<span data-ttu-id="ac219-160">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="ac219-160">xs:integer</span></span>  <br/> |<span data-ttu-id="ac219-161">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ac219-161">required</span></span>  <br/> |<span data-ttu-id="ac219-162">Especifica um código para as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="ac219-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="ac219-163">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="ac219-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ac219-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="ac219-164">skytextday</span></span>  <br/> |<span data-ttu-id="ac219-165">xs: String</span><span class="sxs-lookup"><span data-stu-id="ac219-165">xs:string</span></span>  <br/> |<span data-ttu-id="ac219-166">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ac219-166">required</span></span>  <br/> |<span data-ttu-id="ac219-167">Especifica uma ou duas palavras que descrevem as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="ac219-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="ac219-168">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="ac219-168">A value of the type xs:string</span></span>  <br/> |
   

