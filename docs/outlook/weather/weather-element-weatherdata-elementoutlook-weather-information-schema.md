---
title: elemento de clima (weatherdata elemento) (esquema de informações de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Especifica as condições de clima de um local.
ms.openlocfilehash: c19db6657860dd35f90832aef0614f4fb88d87b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771038"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="99c0e-103">elemento de clima (weatherdata elemento) (esquema de informações de clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="99c0e-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="99c0e-104">Especifica as condições de clima de um local.</span><span class="sxs-lookup"><span data-stu-id="99c0e-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99c0e-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="99c0e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99c0e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="99c0e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="99c0e-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="99c0e-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="99c0e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="99c0e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="99c0e-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="99c0e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="99c0e-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="99c0e-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="99c0e-111">Definição</span><span class="sxs-lookup"><span data-stu-id="99c0e-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="99c0e-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="99c0e-112">Elements and attributes</span></span>

<span data-ttu-id="99c0e-113">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="99c0e-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="99c0e-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="99c0e-114">Parent elements</span></span>

|<span data-ttu-id="99c0e-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99c0e-115">**Element**</span></span>|<span data-ttu-id="99c0e-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99c0e-116">**Type**</span></span>|<span data-ttu-id="99c0e-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="99c0e-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99c0e-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="99c0e-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="99c0e-119">Define o elemento de clima.</span><span class="sxs-lookup"><span data-stu-id="99c0e-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="99c0e-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="99c0e-120">Child elements</span></span>

|<span data-ttu-id="99c0e-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99c0e-121">**Element**</span></span>|<span data-ttu-id="99c0e-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99c0e-122">**Type**</span></span>|<span data-ttu-id="99c0e-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="99c0e-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99c0e-124">atual</span><span class="sxs-lookup"><span data-stu-id="99c0e-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="99c0e-125">currentType</span><span class="sxs-lookup"><span data-stu-id="99c0e-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="99c0e-126">Especifica as condições de clima atual.</span><span class="sxs-lookup"><span data-stu-id="99c0e-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="99c0e-127">previsão</span><span class="sxs-lookup"><span data-stu-id="99c0e-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="99c0e-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="99c0e-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="99c0e-129">Especifica as condições de clima futuras de pelo menos três dias com antecedência incluindo hoje: hoje, amanhã, de depois de amanhã.</span><span class="sxs-lookup"><span data-stu-id="99c0e-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="99c0e-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="99c0e-130">Attributes</span></span>

|<span data-ttu-id="99c0e-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="99c0e-131">**Attribute**</span></span>|<span data-ttu-id="99c0e-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99c0e-132">**Type**</span></span>|<span data-ttu-id="99c0e-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="99c0e-133">**Required**</span></span>|<span data-ttu-id="99c0e-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="99c0e-134">**Description**</span></span>|<span data-ttu-id="99c0e-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="99c0e-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="99c0e-136">atribuição</span><span class="sxs-lookup"><span data-stu-id="99c0e-136">attribution</span></span>  <br/> |<span data-ttu-id="99c0e-137">xs: String</span><span class="sxs-lookup"><span data-stu-id="99c0e-137">xs:string</span></span>  <br/> |<span data-ttu-id="99c0e-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="99c0e-138">required</span></span>  <br/> |<span data-ttu-id="99c0e-139">Especifica a fonte das informações de clima.</span><span class="sxs-lookup"><span data-stu-id="99c0e-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="99c0e-140">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="99c0e-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="99c0e-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="99c0e-141">degreetype</span></span>  <br/> |<span data-ttu-id="99c0e-142">xs: String</span><span class="sxs-lookup"><span data-stu-id="99c0e-142">xs:string</span></span>  <br/> |<span data-ttu-id="99c0e-143">obrigatório</span><span class="sxs-lookup"><span data-stu-id="99c0e-143">required</span></span>  <br/> |<span data-ttu-id="99c0e-144">Especifica a unidade para a temperatura da localidade, por exemplo, Celsius.</span><span class="sxs-lookup"><span data-stu-id="99c0e-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="99c0e-145">C, F</span><span class="sxs-lookup"><span data-stu-id="99c0e-145">C, F</span></span>  <br/> |
|<span data-ttu-id="99c0e-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="99c0e-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="99c0e-147">xs: String</span><span class="sxs-lookup"><span data-stu-id="99c0e-147">xs:string</span></span>  <br/> |<span data-ttu-id="99c0e-148">obrigatório</span><span class="sxs-lookup"><span data-stu-id="99c0e-148">required</span></span>  <br/> |<span data-ttu-id="99c0e-149">Especifica a URL da imagem para o local.</span><span class="sxs-lookup"><span data-stu-id="99c0e-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="99c0e-150">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="99c0e-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="99c0e-151">fuso horário</span><span class="sxs-lookup"><span data-stu-id="99c0e-151">timezone</span></span>  <br/> |<span data-ttu-id="99c0e-152">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="99c0e-152">xs:integer</span></span>  <br/> |<span data-ttu-id="99c0e-153">obrigatório</span><span class="sxs-lookup"><span data-stu-id="99c0e-153">required</span></span>  <br/> |<span data-ttu-id="99c0e-154">Especifica o deslocamento de GMT.</span><span class="sxs-lookup"><span data-stu-id="99c0e-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="99c0e-155">Um valor entre -11 e 12 inclusive</span><span class="sxs-lookup"><span data-stu-id="99c0e-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="99c0e-156">url</span><span class="sxs-lookup"><span data-stu-id="99c0e-156">url</span></span>  <br/> |<span data-ttu-id="99c0e-157">xs: String</span><span class="sxs-lookup"><span data-stu-id="99c0e-157">xs:string</span></span>  <br/> |<span data-ttu-id="99c0e-158">obrigatório</span><span class="sxs-lookup"><span data-stu-id="99c0e-158">required</span></span>  <br/> |<span data-ttu-id="99c0e-159">Especifica a URL da página da web do serviço clima que contém informações de clima para o local especificado.</span><span class="sxs-lookup"><span data-stu-id="99c0e-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="99c0e-160">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="99c0e-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="99c0e-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="99c0e-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="99c0e-162">xs: String</span><span class="sxs-lookup"><span data-stu-id="99c0e-162">xs:string</span></span>  <br/> |<span data-ttu-id="99c0e-163">obrigatório</span><span class="sxs-lookup"><span data-stu-id="99c0e-163">required</span></span>  <br/> |<span data-ttu-id="99c0e-164">Especifica o código que está associado com o local usado para distinguir vários local que tiverem o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="99c0e-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="99c0e-165">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="99c0e-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="99c0e-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="99c0e-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="99c0e-167">xs: String</span><span class="sxs-lookup"><span data-stu-id="99c0e-167">xs:string</span></span>  <br/> |<span data-ttu-id="99c0e-168">obrigatório</span><span class="sxs-lookup"><span data-stu-id="99c0e-168">required</span></span>  <br/> |<span data-ttu-id="99c0e-169">Especifica o nome do local que aparece no controle de lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="99c0e-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="99c0e-170">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="99c0e-170">A value of the type xs:string</span></span>  <br/> |
   

