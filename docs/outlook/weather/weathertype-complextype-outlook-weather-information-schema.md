---
title: weatherType complexType (Esquema de informações sobre o clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Especifica as condições meteorológicas de um local.
ms.openlocfilehash: ac7b8f37e71da203db0f6aefc8e20b29e810c3cf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542944"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="cd753-103">weatherType complexType (Esquema de informações sobre o clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="cd753-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="cd753-104">Especifica as condições meteorológicas de um local.</span><span class="sxs-lookup"><span data-stu-id="cd753-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="cd753-105">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="cd753-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd753-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cd753-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="cd753-107">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cd753-107">**Schema file**</span></span> <br/> |<span data-ttu-id="cd753-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="cd753-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="cd753-109">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="cd753-109">**Extension base**</span></span> <br/> |<span data-ttu-id="cd753-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cd753-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cd753-111">Definição</span><span class="sxs-lookup"><span data-stu-id="cd753-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cd753-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cd753-112">Elements and attributes</span></span>

<span data-ttu-id="cd753-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cd753-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cd753-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cd753-114">Child elements</span></span>

|<span data-ttu-id="cd753-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cd753-115">**Element**</span></span>|<span data-ttu-id="cd753-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cd753-116">**Type**</span></span>|<span data-ttu-id="cd753-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cd753-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cd753-118">current</span><span class="sxs-lookup"><span data-stu-id="cd753-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="cd753-119">currentType</span><span class="sxs-lookup"><span data-stu-id="cd753-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="cd753-120">Especifica as condições meteorológicas atuais.</span><span class="sxs-lookup"><span data-stu-id="cd753-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="cd753-121">forecast</span><span class="sxs-lookup"><span data-stu-id="cd753-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="cd753-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="cd753-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="cd753-123">Especifica as condições meteorológicas futuras para pelo menos três dias, incluindo hoje, amanhã, depois de amanhã.</span><span class="sxs-lookup"><span data-stu-id="cd753-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cd753-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="cd753-124">Attributes</span></span>

|<span data-ttu-id="cd753-125">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cd753-125">**Attribute**</span></span>|<span data-ttu-id="cd753-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cd753-126">**Type**</span></span>|<span data-ttu-id="cd753-127">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="cd753-127">**Required**</span></span>|<span data-ttu-id="cd753-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cd753-128">**Description**</span></span>|<span data-ttu-id="cd753-129">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="cd753-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cd753-130">attribution</span><span class="sxs-lookup"><span data-stu-id="cd753-130">attribution</span></span>  <br/> |<span data-ttu-id="cd753-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-131">xs:string</span></span>  <br/> |<span data-ttu-id="cd753-132">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd753-132">required</span></span>  <br/> |<span data-ttu-id="cd753-133">Especifica a origem das informações meteorológicas.</span><span class="sxs-lookup"><span data-stu-id="cd753-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="cd753-134">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cd753-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="cd753-135">degreetype</span></span>  <br/> |<span data-ttu-id="cd753-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-136">xs:string</span></span>  <br/> |<span data-ttu-id="cd753-137">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd753-137">required</span></span>  <br/> |<span data-ttu-id="cd753-138">Especifica a unidade de temperatura local, como Celsius.</span><span class="sxs-lookup"><span data-stu-id="cd753-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="cd753-139">C, F</span><span class="sxs-lookup"><span data-stu-id="cd753-139">C, F</span></span>  <br/> |
|<span data-ttu-id="cd753-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="cd753-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="cd753-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-141">xs:string</span></span>  <br/> |<span data-ttu-id="cd753-142">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd753-142">required</span></span>  <br/> |<span data-ttu-id="cd753-143">Especifica a URL da imagem para o local.</span><span class="sxs-lookup"><span data-stu-id="cd753-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="cd753-144">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cd753-145">timezone</span><span class="sxs-lookup"><span data-stu-id="cd753-145">timezone</span></span>  <br/> |<span data-ttu-id="cd753-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cd753-146">xs:integer</span></span>  <br/> |<span data-ttu-id="cd753-147">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd753-147">required</span></span>  <br/> |<span data-ttu-id="cd753-148">Especifica o deslocamento GMT.</span><span class="sxs-lookup"><span data-stu-id="cd753-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="cd753-149">Um valor entre -11 e 12, inclusive</span><span class="sxs-lookup"><span data-stu-id="cd753-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="cd753-150">url</span><span class="sxs-lookup"><span data-stu-id="cd753-150">url</span></span>  <br/> |<span data-ttu-id="cd753-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-151">xs:string</span></span>  <br/> |<span data-ttu-id="cd753-152">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd753-152">required</span></span>  <br/> |<span data-ttu-id="cd753-153">Especifica a URL para a página da Web do serviço meteorológico que contém informações sobre o clima para o local especificado.</span><span class="sxs-lookup"><span data-stu-id="cd753-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="cd753-154">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cd753-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="cd753-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="cd753-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-156">xs:string</span></span>  <br/> |<span data-ttu-id="cd753-157">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd753-157">required</span></span>  <br/> |<span data-ttu-id="cd753-158">Especifica o código associado ao local usado para distinguir vários locais que tenham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="cd753-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="cd753-159">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cd753-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="cd753-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="cd753-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-161">xs:string</span></span>  <br/> |<span data-ttu-id="cd753-162">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd753-162">required</span></span>  <br/> |<span data-ttu-id="cd753-163">Especifica o nome do local exibido no controle suspenso.</span><span class="sxs-lookup"><span data-stu-id="cd753-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="cd753-164">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="cd753-164">A value of the type xs:string</span></span>  <br/> |
   

