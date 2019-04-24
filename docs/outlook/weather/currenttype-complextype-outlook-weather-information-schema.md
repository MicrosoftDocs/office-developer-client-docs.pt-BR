---
title: currentType complexType (Esquema de informações sobre o clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Define os parâmetros sobre as condições meteorológicas atuais para um local.
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338448"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="31702-103">currentType complexType (Esquema de informações sobre o clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="31702-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="31702-104">Define os parâmetros sobre as condições meteorológicas atuais para um local.</span><span class="sxs-lookup"><span data-stu-id="31702-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="31702-105">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="31702-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31702-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="31702-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="31702-107">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="31702-107">**Schema file**</span></span> <br/> |<span data-ttu-id="31702-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="31702-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="31702-109">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="31702-109">**Extension base**</span></span> <br/> |<span data-ttu-id="31702-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="31702-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="31702-111">Definição</span><span class="sxs-lookup"><span data-stu-id="31702-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="31702-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="31702-112">Elements and attributes</span></span>

<span data-ttu-id="31702-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="31702-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="31702-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="31702-114">Child elements</span></span>

<span data-ttu-id="31702-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="31702-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31702-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="31702-116">Attributes</span></span>

|<span data-ttu-id="31702-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="31702-117">**Attribute**</span></span>|<span data-ttu-id="31702-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="31702-118">**Type**</span></span>|<span data-ttu-id="31702-119">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="31702-119">**Required**</span></span>|<span data-ttu-id="31702-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="31702-120">**Description**</span></span>|<span data-ttu-id="31702-121">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="31702-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="31702-122">data</span><span class="sxs-lookup"><span data-stu-id="31702-122">date</span></span>  <br/> |<span data-ttu-id="31702-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="31702-123">xs:date</span></span>  <br/> |<span data-ttu-id="31702-124">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-124">required</span></span>  <br/> |<span data-ttu-id="31702-125">Especifica a data de hoje.</span><span class="sxs-lookup"><span data-stu-id="31702-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="31702-126">Um valor do tipo xs:date</span><span class="sxs-lookup"><span data-stu-id="31702-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="31702-127">dia</span><span class="sxs-lookup"><span data-stu-id="31702-127">day</span></span>  <br/> |<span data-ttu-id="31702-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-128">xs:string</span></span>  <br/> |<span data-ttu-id="31702-129">opcional</span><span class="sxs-lookup"><span data-stu-id="31702-129">optional</span></span>  <br/> |<span data-ttu-id="31702-130">Especifica um dia para a previsão.</span><span class="sxs-lookup"><span data-stu-id="31702-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="31702-131">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="31702-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="31702-132">feelslike</span></span>  <br/> |<span data-ttu-id="31702-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-133">xs:integer</span></span>  <br/> |<span data-ttu-id="31702-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-134">required</span></span>  <br/> |<span data-ttu-id="31702-135">Especifica a temperatura da sensação térmica.</span><span class="sxs-lookup"><span data-stu-id="31702-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="31702-136">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="31702-137">humidity</span><span class="sxs-lookup"><span data-stu-id="31702-137">humidity</span></span>  <br/> |<span data-ttu-id="31702-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-138">xs:integer</span></span>  <br/> |<span data-ttu-id="31702-139">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-139">required</span></span>  <br/> |<span data-ttu-id="31702-140">Especifica o valor numérico de umidade atual.</span><span class="sxs-lookup"><span data-stu-id="31702-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="31702-141">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="31702-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="31702-142">observationpoint</span></span>  <br/> |<span data-ttu-id="31702-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-143">xs:string</span></span>  <br/> |<span data-ttu-id="31702-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-144">required</span></span>  <br/> |<span data-ttu-id="31702-145">Especifica de onde as informações meteorológicas atuais são observadas.</span><span class="sxs-lookup"><span data-stu-id="31702-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="31702-146">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="31702-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="31702-147">observationtime</span></span>  <br/> |<span data-ttu-id="31702-148">xs:time</span><span class="sxs-lookup"><span data-stu-id="31702-148">xs:time</span></span>  <br/> |<span data-ttu-id="31702-149">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-149">required</span></span>  <br/> |<span data-ttu-id="31702-150">Especifica quando as informações meteorológicas atuais são observadas.</span><span class="sxs-lookup"><span data-stu-id="31702-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="31702-151">Um valor do tipo xs:time</span><span class="sxs-lookup"><span data-stu-id="31702-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="31702-152">shortday</span><span class="sxs-lookup"><span data-stu-id="31702-152">shortday</span></span>  <br/> |<span data-ttu-id="31702-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-153">xs:string</span></span>  <br/> |<span data-ttu-id="31702-154">opcional</span><span class="sxs-lookup"><span data-stu-id="31702-154">optional</span></span>  <br/> |<span data-ttu-id="31702-155">Especifica um dia na forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="31702-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="31702-156">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="31702-157">skycode</span><span class="sxs-lookup"><span data-stu-id="31702-157">skycode</span></span>  <br/> |<span data-ttu-id="31702-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-158">xs:integer</span></span>  <br/> |<span data-ttu-id="31702-159">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-159">required</span></span>  <br/> |<span data-ttu-id="31702-160">Especifica um código em número inteiro das condições meteorológicas atuais.</span><span class="sxs-lookup"><span data-stu-id="31702-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="31702-161">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="31702-162">skytext</span><span class="sxs-lookup"><span data-stu-id="31702-162">skytext</span></span>  <br/> |<span data-ttu-id="31702-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-163">xs:string</span></span>  <br/> |<span data-ttu-id="31702-164">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-164">required</span></span>  <br/> |<span data-ttu-id="31702-165">Especifica uma ou duas palavras que descrevem as condições meteorológicas atuais.</span><span class="sxs-lookup"><span data-stu-id="31702-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="31702-166">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="31702-167">temperature</span><span class="sxs-lookup"><span data-stu-id="31702-167">temperature</span></span>  <br/> |<span data-ttu-id="31702-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-168">xs:integer</span></span>  <br/> |<span data-ttu-id="31702-169">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-169">required</span></span>  <br/> |<span data-ttu-id="31702-170">Especifica a temperatura atual do local.</span><span class="sxs-lookup"><span data-stu-id="31702-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="31702-171">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="31702-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="31702-172">winddisplay</span></span>  <br/> |<span data-ttu-id="31702-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-173">xs:string</span></span>  <br/> |<span data-ttu-id="31702-174">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-174">required</span></span>  <br/> |<span data-ttu-id="31702-175">Uma cadeia de caracteres que descreve as condições de vento atual.</span><span class="sxs-lookup"><span data-stu-id="31702-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="31702-176">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="31702-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="31702-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="31702-177">windspeed</span></span>  <br/> |<span data-ttu-id="31702-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-178">xs:integer</span></span>  <br/> |<span data-ttu-id="31702-179">obrigatório</span><span class="sxs-lookup"><span data-stu-id="31702-179">required</span></span>  <br/> |<span data-ttu-id="31702-180">Especifica o valor numérico da velocidade do vento atual.</span><span class="sxs-lookup"><span data-stu-id="31702-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="31702-181">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="31702-181">A value of the type xs:integer</span></span>  <br/> |
   

