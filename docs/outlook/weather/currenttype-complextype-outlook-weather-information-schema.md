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
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540984"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="cda47-103">currentType complexType (Esquema de informações sobre o clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="cda47-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="cda47-104">Define os parâmetros sobre as condições meteorológicas atuais para um local.</span><span class="sxs-lookup"><span data-stu-id="cda47-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="cda47-105">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="cda47-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cda47-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cda47-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="cda47-107">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cda47-107">**Schema file**</span></span> <br/> |<span data-ttu-id="cda47-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="cda47-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="cda47-109">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="cda47-109">**Extension base**</span></span> <br/> |<span data-ttu-id="cda47-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cda47-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cda47-111">Definição</span><span class="sxs-lookup"><span data-stu-id="cda47-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cda47-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cda47-112">Elements and attributes</span></span>

<span data-ttu-id="cda47-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cda47-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cda47-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cda47-114">Child elements</span></span>

<span data-ttu-id="cda47-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="cda47-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cda47-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="cda47-116">Attributes</span></span>

|<span data-ttu-id="cda47-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cda47-117">**Attribute**</span></span>|<span data-ttu-id="cda47-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cda47-118">**Type**</span></span>|<span data-ttu-id="cda47-119">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="cda47-119">**Required**</span></span>|<span data-ttu-id="cda47-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cda47-120">**Description**</span></span>|<span data-ttu-id="cda47-121">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="cda47-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cda47-122">data</span><span class="sxs-lookup"><span data-stu-id="cda47-122">date</span></span>  <br/> |<span data-ttu-id="cda47-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="cda47-123">xs:date</span></span>  <br/> |<span data-ttu-id="cda47-124">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-124">required</span></span>  <br/> |<span data-ttu-id="cda47-125">Especifica a data de hoje.</span><span class="sxs-lookup"><span data-stu-id="cda47-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="cda47-126">Um valor do tipo xs:date</span><span class="sxs-lookup"><span data-stu-id="cda47-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="cda47-127">dia</span><span class="sxs-lookup"><span data-stu-id="cda47-127">day</span></span>  <br/> |<span data-ttu-id="cda47-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-128">xs:string</span></span>  <br/> |<span data-ttu-id="cda47-129">opcional</span><span class="sxs-lookup"><span data-stu-id="cda47-129">optional</span></span>  <br/> |<span data-ttu-id="cda47-130">Especifica um dia para a previsão.</span><span class="sxs-lookup"><span data-stu-id="cda47-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="cda47-131">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cda47-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="cda47-132">feelslike</span></span>  <br/> |<span data-ttu-id="cda47-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-133">xs:integer</span></span>  <br/> |<span data-ttu-id="cda47-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-134">required</span></span>  <br/> |<span data-ttu-id="cda47-135">Especifica a temperatura da sensação térmica.</span><span class="sxs-lookup"><span data-stu-id="cda47-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="cda47-136">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="cda47-137">humidity</span><span class="sxs-lookup"><span data-stu-id="cda47-137">humidity</span></span>  <br/> |<span data-ttu-id="cda47-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-138">xs:integer</span></span>  <br/> |<span data-ttu-id="cda47-139">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-139">required</span></span>  <br/> |<span data-ttu-id="cda47-140">Especifica o valor numérico de umidade atual.</span><span class="sxs-lookup"><span data-stu-id="cda47-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="cda47-141">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="cda47-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="cda47-142">observationpoint</span></span>  <br/> |<span data-ttu-id="cda47-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-143">xs:string</span></span>  <br/> |<span data-ttu-id="cda47-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-144">required</span></span>  <br/> |<span data-ttu-id="cda47-145">Especifica de onde as informações meteorológicas atuais são observadas.</span><span class="sxs-lookup"><span data-stu-id="cda47-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="cda47-146">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cda47-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="cda47-147">observationtime</span></span>  <br/> |<span data-ttu-id="cda47-148">xs:time</span><span class="sxs-lookup"><span data-stu-id="cda47-148">xs:time</span></span>  <br/> |<span data-ttu-id="cda47-149">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-149">required</span></span>  <br/> |<span data-ttu-id="cda47-150">Especifica quando as informações meteorológicas atuais são observadas.</span><span class="sxs-lookup"><span data-stu-id="cda47-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="cda47-151">Um valor do tipo xs:time</span><span class="sxs-lookup"><span data-stu-id="cda47-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="cda47-152">shortday</span><span class="sxs-lookup"><span data-stu-id="cda47-152">shortday</span></span>  <br/> |<span data-ttu-id="cda47-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-153">xs:string</span></span>  <br/> |<span data-ttu-id="cda47-154">opcional</span><span class="sxs-lookup"><span data-stu-id="cda47-154">optional</span></span>  <br/> |<span data-ttu-id="cda47-155">Especifica um dia na forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="cda47-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="cda47-156">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cda47-157">skycode</span><span class="sxs-lookup"><span data-stu-id="cda47-157">skycode</span></span>  <br/> |<span data-ttu-id="cda47-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-158">xs:integer</span></span>  <br/> |<span data-ttu-id="cda47-159">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-159">required</span></span>  <br/> |<span data-ttu-id="cda47-160">Especifica um código em número inteiro das condições meteorológicas atuais.</span><span class="sxs-lookup"><span data-stu-id="cda47-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="cda47-161">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="cda47-162">skytext</span><span class="sxs-lookup"><span data-stu-id="cda47-162">skytext</span></span>  <br/> |<span data-ttu-id="cda47-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-163">xs:string</span></span>  <br/> |<span data-ttu-id="cda47-164">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-164">required</span></span>  <br/> |<span data-ttu-id="cda47-165">Especifica uma ou duas palavras que descrevem as condições meteorológicas atuais.</span><span class="sxs-lookup"><span data-stu-id="cda47-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="cda47-166">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cda47-167">temperature</span><span class="sxs-lookup"><span data-stu-id="cda47-167">temperature</span></span>  <br/> |<span data-ttu-id="cda47-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-168">xs:integer</span></span>  <br/> |<span data-ttu-id="cda47-169">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-169">required</span></span>  <br/> |<span data-ttu-id="cda47-170">Especifica a temperatura atual do local.</span><span class="sxs-lookup"><span data-stu-id="cda47-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="cda47-171">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="cda47-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="cda47-172">winddisplay</span></span>  <br/> |<span data-ttu-id="cda47-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-173">xs:string</span></span>  <br/> |<span data-ttu-id="cda47-174">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-174">required</span></span>  <br/> |<span data-ttu-id="cda47-175">Uma cadeia de caracteres que descreve as condições de vento atual.</span><span class="sxs-lookup"><span data-stu-id="cda47-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="cda47-176">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cda47-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cda47-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="cda47-177">windspeed</span></span>  <br/> |<span data-ttu-id="cda47-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-178">xs:integer</span></span>  <br/> |<span data-ttu-id="cda47-179">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cda47-179">required</span></span>  <br/> |<span data-ttu-id="cda47-180">Especifica o valor numérico da velocidade do vento atual.</span><span class="sxs-lookup"><span data-stu-id="cda47-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="cda47-181">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="cda47-181">A value of the type xs:integer</span></span>  <br/> |
   

