---
title: weatherType complexType (esquema de informações de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Especifica as condições de clima de um local.
ms.openlocfilehash: b333bb6ce60dd1613bceda0a57e7e34c9819bd84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771036"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="07611-103">weatherType complexType (esquema de informações de clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="07611-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="07611-104">Especifica as condições de clima de um local.</span><span class="sxs-lookup"><span data-stu-id="07611-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="07611-105">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="07611-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07611-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="07611-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="07611-107">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="07611-107">**Schema file**</span></span> <br/> |<span data-ttu-id="07611-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="07611-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="07611-109">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="07611-109">**Extension base**</span></span> <br/> |<span data-ttu-id="07611-110">None</span><span class="sxs-lookup"><span data-stu-id="07611-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="07611-111">Definição</span><span class="sxs-lookup"><span data-stu-id="07611-111">Definition</span></span>

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="07611-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="07611-112">Elements and attributes</span></span>

<span data-ttu-id="07611-113">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="07611-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="07611-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="07611-114">Child elements</span></span>

|<span data-ttu-id="07611-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="07611-115">**Element**</span></span>|<span data-ttu-id="07611-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="07611-116">**Type**</span></span>|<span data-ttu-id="07611-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="07611-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="07611-118">atual</span><span class="sxs-lookup"><span data-stu-id="07611-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="07611-119">currentType</span><span class="sxs-lookup"><span data-stu-id="07611-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="07611-120">Especifica as condições de clima atual.</span><span class="sxs-lookup"><span data-stu-id="07611-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="07611-121">previsão</span><span class="sxs-lookup"><span data-stu-id="07611-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="07611-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="07611-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="07611-123">Especifica as condições de clima futuras de pelo menos três dias com antecedência incluindo hoje: hoje, amanhã, de depois de amanhã.</span><span class="sxs-lookup"><span data-stu-id="07611-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="07611-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="07611-124">Attributes</span></span>

|<span data-ttu-id="07611-125">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="07611-125">**Attribute**</span></span>|<span data-ttu-id="07611-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="07611-126">**Type**</span></span>|<span data-ttu-id="07611-127">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="07611-127">**Required**</span></span>|<span data-ttu-id="07611-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="07611-128">**Description**</span></span>|<span data-ttu-id="07611-129">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="07611-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="07611-130">atribuição</span><span class="sxs-lookup"><span data-stu-id="07611-130">attribution</span></span>  <br/> |<span data-ttu-id="07611-131">xs: String</span><span class="sxs-lookup"><span data-stu-id="07611-131">xs:string</span></span>  <br/> |<span data-ttu-id="07611-132">obrigatório</span><span class="sxs-lookup"><span data-stu-id="07611-132">required</span></span>  <br/> |<span data-ttu-id="07611-133">Especifica a fonte das informações de clima.</span><span class="sxs-lookup"><span data-stu-id="07611-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="07611-134">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="07611-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="07611-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="07611-135">degreetype</span></span>  <br/> |<span data-ttu-id="07611-136">xs: String</span><span class="sxs-lookup"><span data-stu-id="07611-136">xs:string</span></span>  <br/> |<span data-ttu-id="07611-137">obrigatório</span><span class="sxs-lookup"><span data-stu-id="07611-137">required</span></span>  <br/> |<span data-ttu-id="07611-138">Especifica a unidade para a temperatura da localidade, por exemplo, Celsius.</span><span class="sxs-lookup"><span data-stu-id="07611-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="07611-139">C, F</span><span class="sxs-lookup"><span data-stu-id="07611-139">C, F</span></span>  <br/> |
|<span data-ttu-id="07611-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="07611-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="07611-141">xs: String</span><span class="sxs-lookup"><span data-stu-id="07611-141">xs:string</span></span>  <br/> |<span data-ttu-id="07611-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="07611-142">required</span></span>  <br/> |<span data-ttu-id="07611-143">Especifica a URL da imagem para o local.</span><span class="sxs-lookup"><span data-stu-id="07611-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="07611-144">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="07611-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="07611-145">fuso horário</span><span class="sxs-lookup"><span data-stu-id="07611-145">timezone</span></span>  <br/> |<span data-ttu-id="07611-146">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="07611-146">xs:integer</span></span>  <br/> |<span data-ttu-id="07611-147">obrigatório</span><span class="sxs-lookup"><span data-stu-id="07611-147">required</span></span>  <br/> |<span data-ttu-id="07611-148">Especifica o deslocamento de GMT.</span><span class="sxs-lookup"><span data-stu-id="07611-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="07611-149">Um valor entre -11 e 12 inclusive</span><span class="sxs-lookup"><span data-stu-id="07611-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="07611-150">url</span><span class="sxs-lookup"><span data-stu-id="07611-150">url</span></span>  <br/> |<span data-ttu-id="07611-151">xs: String</span><span class="sxs-lookup"><span data-stu-id="07611-151">xs:string</span></span>  <br/> |<span data-ttu-id="07611-152">obrigatório</span><span class="sxs-lookup"><span data-stu-id="07611-152">required</span></span>  <br/> |<span data-ttu-id="07611-153">Especifica a URL da página da web do serviço clima que contém informações de clima para o local especificado.</span><span class="sxs-lookup"><span data-stu-id="07611-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="07611-154">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="07611-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="07611-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="07611-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="07611-156">xs: String</span><span class="sxs-lookup"><span data-stu-id="07611-156">xs:string</span></span>  <br/> |<span data-ttu-id="07611-157">obrigatório</span><span class="sxs-lookup"><span data-stu-id="07611-157">required</span></span>  <br/> |<span data-ttu-id="07611-158">Especifica o código que está associado com o local usado para distinguir vários local que tiverem o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="07611-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="07611-159">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="07611-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="07611-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="07611-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="07611-161">xs: String</span><span class="sxs-lookup"><span data-stu-id="07611-161">xs:string</span></span>  <br/> |<span data-ttu-id="07611-162">obrigatório</span><span class="sxs-lookup"><span data-stu-id="07611-162">required</span></span>  <br/> |<span data-ttu-id="07611-163">Especifica o nome do local que aparece no controle de lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="07611-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="07611-164">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="07611-164">A value of the type xs:string</span></span>  <br/> |
   
