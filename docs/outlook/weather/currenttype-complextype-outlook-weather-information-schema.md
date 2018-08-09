---
title: currentType complexType (esquema de informações de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Define os parâmetros sobre as condições de clima atual de um local.
ms.openlocfilehash: 55ea2cfa6904d88c695268675bc7a893fa643010
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770965"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="60930-103">currentType complexType (esquema de informações de clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="60930-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="60930-104">Define os parâmetros sobre as condições de clima atual de um local.</span><span class="sxs-lookup"><span data-stu-id="60930-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="60930-105">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="60930-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60930-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="60930-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="60930-107">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="60930-107">**Schema file**</span></span> <br/> |<span data-ttu-id="60930-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="60930-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="60930-109">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="60930-109">**Extension base**</span></span> <br/> |<span data-ttu-id="60930-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="60930-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="60930-111">Definição</span><span class="sxs-lookup"><span data-stu-id="60930-111">Definition</span></span>

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="60930-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="60930-112">Elements and attributes</span></span>

<span data-ttu-id="60930-113">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="60930-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="60930-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="60930-114">Child elements</span></span>

<span data-ttu-id="60930-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="60930-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60930-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="60930-116">Attributes</span></span>

|<span data-ttu-id="60930-117">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="60930-117">**Attribute**</span></span>|<span data-ttu-id="60930-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="60930-118">**Type**</span></span>|<span data-ttu-id="60930-119">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="60930-119">**Required**</span></span>|<span data-ttu-id="60930-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="60930-120">**Description**</span></span>|<span data-ttu-id="60930-121">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="60930-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="60930-122">data</span><span class="sxs-lookup"><span data-stu-id="60930-122">date</span></span>  <br/> |<span data-ttu-id="60930-123">Date</span><span class="sxs-lookup"><span data-stu-id="60930-123">xs:date</span></span>  <br/> |<span data-ttu-id="60930-124">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-124">required</span></span>  <br/> |<span data-ttu-id="60930-125">Especifica a data de hoje.</span><span class="sxs-lookup"><span data-stu-id="60930-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="60930-126">Um valor de Date o tipo</span><span class="sxs-lookup"><span data-stu-id="60930-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="60930-127">dia</span><span class="sxs-lookup"><span data-stu-id="60930-127">day</span></span>  <br/> |<span data-ttu-id="60930-128">xs: String</span><span class="sxs-lookup"><span data-stu-id="60930-128">xs:string</span></span>  <br/> |<span data-ttu-id="60930-129">opcional</span><span class="sxs-lookup"><span data-stu-id="60930-129">optional</span></span>  <br/> |<span data-ttu-id="60930-130">Especifica um dia para a previsão.</span><span class="sxs-lookup"><span data-stu-id="60930-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="60930-131">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="60930-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="60930-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="60930-132">feelslike</span></span>  <br/> |<span data-ttu-id="60930-133">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="60930-133">xs:integer</span></span>  <br/> |<span data-ttu-id="60930-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-134">required</span></span>  <br/> |<span data-ttu-id="60930-135">Especifica a temperatura de como o clima atual se parece com.</span><span class="sxs-lookup"><span data-stu-id="60930-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="60930-136">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="60930-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="60930-137">Umidade</span><span class="sxs-lookup"><span data-stu-id="60930-137">humidity</span></span>  <br/> |<span data-ttu-id="60930-138">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="60930-138">xs:integer</span></span>  <br/> |<span data-ttu-id="60930-139">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-139">required</span></span>  <br/> |<span data-ttu-id="60930-140">Especifica o valor numérico umidade atual.</span><span class="sxs-lookup"><span data-stu-id="60930-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="60930-141">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="60930-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="60930-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="60930-142">observationpoint</span></span>  <br/> |<span data-ttu-id="60930-143">xs: String</span><span class="sxs-lookup"><span data-stu-id="60930-143">xs:string</span></span>  <br/> |<span data-ttu-id="60930-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-144">required</span></span>  <br/> |<span data-ttu-id="60930-145">Especifica onde as informações atuais de clima observadas de.</span><span class="sxs-lookup"><span data-stu-id="60930-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="60930-146">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="60930-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="60930-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="60930-147">observationtime</span></span>  <br/> |<span data-ttu-id="60930-148">xs: time</span><span class="sxs-lookup"><span data-stu-id="60930-148">xs:time</span></span>  <br/> |<span data-ttu-id="60930-149">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-149">required</span></span>  <br/> |<span data-ttu-id="60930-150">Especifica quando as informações atuais de clima são observadas em.</span><span class="sxs-lookup"><span data-stu-id="60930-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="60930-151">Um valor do xs: time do tipo</span><span class="sxs-lookup"><span data-stu-id="60930-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="60930-152">shortday</span><span class="sxs-lookup"><span data-stu-id="60930-152">shortday</span></span>  <br/> |<span data-ttu-id="60930-153">xs: String</span><span class="sxs-lookup"><span data-stu-id="60930-153">xs:string</span></span>  <br/> |<span data-ttu-id="60930-154">opcional</span><span class="sxs-lookup"><span data-stu-id="60930-154">optional</span></span>  <br/> |<span data-ttu-id="60930-155">Especifica um dia na forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="60930-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="60930-156">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="60930-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="60930-157">skycode</span><span class="sxs-lookup"><span data-stu-id="60930-157">skycode</span></span>  <br/> |<span data-ttu-id="60930-158">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="60930-158">xs:integer</span></span>  <br/> |<span data-ttu-id="60930-159">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-159">required</span></span>  <br/> |<span data-ttu-id="60930-160">Especifica um código de inteiro para as condições de clima atual.</span><span class="sxs-lookup"><span data-stu-id="60930-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="60930-161">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="60930-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="60930-162">skytext</span><span class="sxs-lookup"><span data-stu-id="60930-162">skytext</span></span>  <br/> |<span data-ttu-id="60930-163">xs: String</span><span class="sxs-lookup"><span data-stu-id="60930-163">xs:string</span></span>  <br/> |<span data-ttu-id="60930-164">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-164">required</span></span>  <br/> |<span data-ttu-id="60930-165">Especifica duas palavras descrevendo condições de clima atual.</span><span class="sxs-lookup"><span data-stu-id="60930-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="60930-166">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="60930-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="60930-167">temperatura</span><span class="sxs-lookup"><span data-stu-id="60930-167">temperature</span></span>  <br/> |<span data-ttu-id="60930-168">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="60930-168">xs:integer</span></span>  <br/> |<span data-ttu-id="60930-169">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-169">required</span></span>  <br/> |<span data-ttu-id="60930-170">Especifica a temperatura atual do local.</span><span class="sxs-lookup"><span data-stu-id="60930-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="60930-171">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="60930-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="60930-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="60930-172">winddisplay</span></span>  <br/> |<span data-ttu-id="60930-173">xs: String</span><span class="sxs-lookup"><span data-stu-id="60930-173">xs:string</span></span>  <br/> |<span data-ttu-id="60930-174">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-174">required</span></span>  <br/> |<span data-ttu-id="60930-175">Uma cadeia de caracteres que descreve as condições de vento atual.</span><span class="sxs-lookup"><span data-stu-id="60930-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="60930-176">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="60930-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="60930-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="60930-177">windspeed</span></span>  <br/> |<span data-ttu-id="60930-178">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="60930-178">xs:integer</span></span>  <br/> |<span data-ttu-id="60930-179">obrigatório</span><span class="sxs-lookup"><span data-stu-id="60930-179">required</span></span>  <br/> |<span data-ttu-id="60930-180">Especifica o valor atual de velocidade de vento numérico.</span><span class="sxs-lookup"><span data-stu-id="60930-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="60930-181">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="60930-181">A value of the type xs:integer</span></span>  <br/> |
   

