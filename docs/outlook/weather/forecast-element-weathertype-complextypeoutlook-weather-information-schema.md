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
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540977"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>Elemento forecast (weatherType complexType) (Esquema de informações sobre o clima do Outlook)

Especifica as condições meteorológicas futuras para pelo menos três dias, incluindo hoje, amanhã, depois de amanhã.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Arquivo de esquema** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[clima](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Especifica as condições meteorológicas de um local.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|data  <br/> |xs:date  <br/> |obrigatório  <br/> |Especifica a data da previsão.  <br/> |Um valor do tipo xs:date  <br/> |
|dia  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica um dia para a previsão.  <br/> |Um valor do tipo xs:string  <br/> |
|high  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica a maior temperatura prevista.  <br/> |Um valor do tipo xs:integer  <br/> |
|low  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica a menor temperatura prevista.  <br/> |Um valor do tipo xs:integer  <br/> |
|precip  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica a porcentagem de possibilidade de precipitação.  <br/> |Um valor do tipo xs:integer  <br/> |
|shortday  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica um dia na forma abreviada.  <br/> |Um valor do tipo xs:string  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica um código para as condições previstas.  <br/> |Um valor do tipo xs:integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica uma ou duas palavras que descrevam as condições previstas.  <br/> |Um valor do tipo xs:string  <br/> |
   

