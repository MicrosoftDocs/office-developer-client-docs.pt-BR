---
title: forecastType complexType (esquema de informações de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Define os parâmetros sobre as condições de clima previsão de um local.
ms.openlocfilehash: 886c6cdbbeb9f07564854dc6a62cbcdad9703b62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770960"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="21730-103">forecastType complexType (esquema de informações de clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="21730-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="21730-104">Define os parâmetros sobre as condições de clima previsão de um local.</span><span class="sxs-lookup"><span data-stu-id="21730-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="21730-105">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="21730-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21730-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="21730-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="21730-107">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="21730-107">**Schema file**</span></span> <br/> |<span data-ttu-id="21730-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="21730-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="21730-109">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="21730-109">**Extension base**</span></span> <br/> |<span data-ttu-id="21730-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="21730-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="21730-111">Definição</span><span class="sxs-lookup"><span data-stu-id="21730-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="21730-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="21730-112">Elements and attributes</span></span>

<span data-ttu-id="21730-113">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="21730-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="21730-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="21730-114">Child elements</span></span>

<span data-ttu-id="21730-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="21730-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21730-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="21730-116">Attributes</span></span>

|<span data-ttu-id="21730-117">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="21730-117">**Attribute**</span></span>|<span data-ttu-id="21730-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="21730-118">**Type**</span></span>|<span data-ttu-id="21730-119">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="21730-119">**Required**</span></span>|<span data-ttu-id="21730-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="21730-120">**Description**</span></span>|<span data-ttu-id="21730-121">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="21730-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="21730-122">data</span><span class="sxs-lookup"><span data-stu-id="21730-122">date</span></span>  <br/> |<span data-ttu-id="21730-123">Date</span><span class="sxs-lookup"><span data-stu-id="21730-123">xs:date</span></span>  <br/> |<span data-ttu-id="21730-124">obrigatório</span><span class="sxs-lookup"><span data-stu-id="21730-124">required</span></span>  <br/> |<span data-ttu-id="21730-125">Especifica a data para a previsão.</span><span class="sxs-lookup"><span data-stu-id="21730-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="21730-126">Um valor de Date o tipo</span><span class="sxs-lookup"><span data-stu-id="21730-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="21730-127">dia</span><span class="sxs-lookup"><span data-stu-id="21730-127">day</span></span>  <br/> |<span data-ttu-id="21730-128">xs: String</span><span class="sxs-lookup"><span data-stu-id="21730-128">xs:string</span></span>  <br/> |<span data-ttu-id="21730-129">obrigatório</span><span class="sxs-lookup"><span data-stu-id="21730-129">required</span></span>  <br/> |<span data-ttu-id="21730-130">Especifica um dia para a previsão.</span><span class="sxs-lookup"><span data-stu-id="21730-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="21730-131">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="21730-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="21730-132">alta</span><span class="sxs-lookup"><span data-stu-id="21730-132">high</span></span>  <br/> |<span data-ttu-id="21730-133">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="21730-133">xs:integer</span></span>  <br/> |<span data-ttu-id="21730-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="21730-134">required</span></span>  <br/> |<span data-ttu-id="21730-135">Especifica a temperatura mais alta prevista.</span><span class="sxs-lookup"><span data-stu-id="21730-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="21730-136">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="21730-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="21730-137">baixa</span><span class="sxs-lookup"><span data-stu-id="21730-137">low</span></span>  <br/> |<span data-ttu-id="21730-138">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="21730-138">xs:integer</span></span>  <br/> |<span data-ttu-id="21730-139">obrigatório</span><span class="sxs-lookup"><span data-stu-id="21730-139">required</span></span>  <br/> |<span data-ttu-id="21730-140">Especifica a temperatura mais baixa prevista.</span><span class="sxs-lookup"><span data-stu-id="21730-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="21730-141">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="21730-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="21730-142">precip</span><span class="sxs-lookup"><span data-stu-id="21730-142">precip</span></span>  <br/> |<span data-ttu-id="21730-143">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="21730-143">xs:integer</span></span>  <br/> |<span data-ttu-id="21730-144">obrigatório</span><span class="sxs-lookup"><span data-stu-id="21730-144">required</span></span>  <br/> |<span data-ttu-id="21730-145">Especifica a possibilidade de porcentagem de Precipitação.</span><span class="sxs-lookup"><span data-stu-id="21730-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="21730-146">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="21730-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="21730-147">shortday</span><span class="sxs-lookup"><span data-stu-id="21730-147">shortday</span></span>  <br/> |<span data-ttu-id="21730-148">xs: String</span><span class="sxs-lookup"><span data-stu-id="21730-148">xs:string</span></span>  <br/> |<span data-ttu-id="21730-149">obrigatório</span><span class="sxs-lookup"><span data-stu-id="21730-149">required</span></span>  <br/> |<span data-ttu-id="21730-150">Especifica um dia na forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="21730-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="21730-151">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="21730-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="21730-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="21730-152">skycodeday</span></span>  <br/> |<span data-ttu-id="21730-153">xs:Integer</span><span class="sxs-lookup"><span data-stu-id="21730-153">xs:integer</span></span>  <br/> |<span data-ttu-id="21730-154">obrigatório</span><span class="sxs-lookup"><span data-stu-id="21730-154">required</span></span>  <br/> |<span data-ttu-id="21730-155">Especifica um código para as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="21730-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="21730-156">Um valor de xs:integer do tipo</span><span class="sxs-lookup"><span data-stu-id="21730-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="21730-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="21730-157">skytextday</span></span>  <br/> |<span data-ttu-id="21730-158">xs: String</span><span class="sxs-lookup"><span data-stu-id="21730-158">xs:string</span></span>  <br/> |<span data-ttu-id="21730-159">obrigatório</span><span class="sxs-lookup"><span data-stu-id="21730-159">required</span></span>  <br/> |<span data-ttu-id="21730-160">Especifica uma ou duas palavras que descrevem as condições previstas.</span><span class="sxs-lookup"><span data-stu-id="21730-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="21730-161">Um valor do xs: string tipo</span><span class="sxs-lookup"><span data-stu-id="21730-161">A value of the type xs:string</span></span>  <br/> |
   

