---
title: forecastType complexType (Esquema de informações sobre o clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Define os parâmetros sobre as condições meteorológicas previstas para um local.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540949"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="9d3b7-103">forecastType complexType (Esquema de informações sobre o clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="9d3b7-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="9d3b7-104">Define os parâmetros sobre as condições meteorológicas previstas para um local.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="9d3b7-105">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="9d3b7-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d3b7-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9d3b7-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="9d3b7-107">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9d3b7-107">**Schema file**</span></span> <br/> |<span data-ttu-id="9d3b7-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="9d3b7-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="9d3b7-109">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="9d3b7-109">**Extension base**</span></span> <br/> |<span data-ttu-id="9d3b7-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9d3b7-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9d3b7-111">Definição</span><span class="sxs-lookup"><span data-stu-id="9d3b7-111">Definition</span></span>

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="9d3b7-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9d3b7-112">Elements and attributes</span></span>

<span data-ttu-id="9d3b7-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9d3b7-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9d3b7-114">Child elements</span></span>

<span data-ttu-id="9d3b7-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d3b7-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d3b7-116">Attributes</span></span>

|<span data-ttu-id="9d3b7-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9d3b7-117">**Attribute**</span></span>|<span data-ttu-id="9d3b7-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d3b7-118">**Type**</span></span>|<span data-ttu-id="9d3b7-119">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9d3b7-119">**Required**</span></span>|<span data-ttu-id="9d3b7-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9d3b7-120">**Description**</span></span>|<span data-ttu-id="9d3b7-121">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9d3b7-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9d3b7-122">data</span><span class="sxs-lookup"><span data-stu-id="9d3b7-122">date</span></span>  <br/> |<span data-ttu-id="9d3b7-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="9d3b7-123">xs:date</span></span>  <br/> |<span data-ttu-id="9d3b7-124">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d3b7-124">required</span></span>  <br/> |<span data-ttu-id="9d3b7-125">Especifica a data da previsão.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="9d3b7-126">Um valor do tipo xs:date</span><span class="sxs-lookup"><span data-stu-id="9d3b7-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="9d3b7-127">dia</span><span class="sxs-lookup"><span data-stu-id="9d3b7-127">day</span></span>  <br/> |<span data-ttu-id="9d3b7-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d3b7-128">xs:string</span></span>  <br/> |<span data-ttu-id="9d3b7-129">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d3b7-129">required</span></span>  <br/> |<span data-ttu-id="9d3b7-130">Especifica um dia para a previsão.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="9d3b7-131">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="9d3b7-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9d3b7-132">high</span><span class="sxs-lookup"><span data-stu-id="9d3b7-132">high</span></span>  <br/> |<span data-ttu-id="9d3b7-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9d3b7-133">xs:integer</span></span>  <br/> |<span data-ttu-id="9d3b7-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d3b7-134">required</span></span>  <br/> |<span data-ttu-id="9d3b7-135">Especifica a maior temperatura prevista.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="9d3b7-136">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="9d3b7-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9d3b7-137">low</span><span class="sxs-lookup"><span data-stu-id="9d3b7-137">low</span></span>  <br/> |<span data-ttu-id="9d3b7-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9d3b7-138">xs:integer</span></span>  <br/> |<span data-ttu-id="9d3b7-139">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d3b7-139">required</span></span>  <br/> |<span data-ttu-id="9d3b7-140">Especifica a menor temperatura prevista.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="9d3b7-141">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="9d3b7-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9d3b7-142">precip</span><span class="sxs-lookup"><span data-stu-id="9d3b7-142">precip</span></span>  <br/> |<span data-ttu-id="9d3b7-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9d3b7-143">xs:integer</span></span>  <br/> |<span data-ttu-id="9d3b7-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d3b7-144">required</span></span>  <br/> |<span data-ttu-id="9d3b7-145">Especifica a porcentagem de possibilidade de precipitação.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="9d3b7-146">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="9d3b7-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9d3b7-147">shortday</span><span class="sxs-lookup"><span data-stu-id="9d3b7-147">shortday</span></span>  <br/> |<span data-ttu-id="9d3b7-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d3b7-148">xs:string</span></span>  <br/> |<span data-ttu-id="9d3b7-149">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d3b7-149">required</span></span>  <br/> |<span data-ttu-id="9d3b7-150">Especifica um dia na forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="9d3b7-151">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="9d3b7-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9d3b7-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="9d3b7-152">skycodeday</span></span>  <br/> |<span data-ttu-id="9d3b7-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9d3b7-153">xs:integer</span></span>  <br/> |<span data-ttu-id="9d3b7-154">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d3b7-154">required</span></span>  <br/> |<span data-ttu-id="9d3b7-155">Especifica um código para as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="9d3b7-156">Um valor do tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="9d3b7-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9d3b7-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="9d3b7-157">skytextday</span></span>  <br/> |<span data-ttu-id="9d3b7-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d3b7-158">xs:string</span></span>  <br/> |<span data-ttu-id="9d3b7-159">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d3b7-159">required</span></span>  <br/> |<span data-ttu-id="9d3b7-160">Especifica uma ou duas palavras que descrevam as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="9d3b7-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="9d3b7-161">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="9d3b7-161">A value of the type xs:string</span></span>  <br/> |
   

