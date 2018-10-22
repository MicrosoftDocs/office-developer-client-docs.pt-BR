---
title: Elemento weather (elemento weatherdata) (Esquema de informações sobre o clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Especifica as condições meteorológicas de um local.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390657"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>Elemento weather (elemento weatherdata) (Esquema de informações sobre o clima do Outlook)

Especifica as condições meteorológicas de um local.
  
## <a name="element-information"></a>Informações do elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Arquivo de esquema** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Define o elemento do clima.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[current](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica as condições meteorológicas atuais.  <br/> |
|[forecast](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica as condições meteorológicas futuras para pelo menos três dias, incluindo hoje, amanhã, depois de amanhã.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|attribution  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica a origem das informações meteorológicas.  <br/> |Um valor do tipo xs:string  <br/> |
|degreetype  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica a unidade de temperatura local, como Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica a URL da imagem para o local.  <br/> |Um valor do tipo xs:string  <br/> |
|timezone  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica o deslocamento GMT.  <br/> |Um valor entre -11 e 12, inclusive  <br/> |
|url  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica a URL para a página da Web do serviço meteorológico que contém informações sobre o clima para o local especificado.  <br/> |Um valor do tipo xs:string  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica o código associado ao local usado para distinguir vários locais que tenham o mesmo nome.  <br/> |Um valor do tipo xs:string  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica o nome do local exibido no controle suspenso.  <br/> |Um valor do tipo xs:string  <br/> |
   

