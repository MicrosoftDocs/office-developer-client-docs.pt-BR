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
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>previsão de elemento (weatherType complexType) (esquema de informações de clima do Outlook)

Especifica as condições de clima futuras de pelo menos três dias com antecedência incluindo hoje: hoje, amanhã, de depois de amanhã.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Arquivo de esquema** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[clima](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Especifica as condições de clima de um local.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|data  <br/> |Date  <br/> |obrigatório  <br/> |Especifica a data para a previsão.  <br/> |Um valor de Date o tipo  <br/> |
|dia  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica um dia para a previsão.  <br/> |Um valor do xs: string tipo  <br/> |
|alta  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica a temperatura mais alta prevista.  <br/> |Um valor de xs:integer do tipo  <br/> |
|baixa  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica a temperatura mais baixa prevista.  <br/> |Um valor de xs:integer do tipo  <br/> |
|precip  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica a possibilidade de porcentagem de Precipitação.  <br/> |Um valor de xs:integer do tipo  <br/> |
|shortday  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica um dia na forma abreviada.  <br/> |Um valor do xs: string tipo  <br/> |
|skycodeday  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica um código para as condições previstas.  <br/> |Um valor de xs:integer do tipo  <br/> |
|skytextday  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica uma ou duas palavras que descrevem as condições previstas.  <br/> |Um valor do xs: string tipo  <br/> |
   

