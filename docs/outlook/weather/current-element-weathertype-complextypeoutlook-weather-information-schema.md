---
title: Elemento current (weatherType complexType) (Esquema de informações sobre o clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Especifica as condições meteorológicas atuais.
ms.openlocfilehash: ce92bdd49ee37f939748586c2d63d8a664f664d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401087"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>Elemento current (weatherType complexType) (Esquema de informações sobre o clima do Outlook)

Especifica as condições meteorológicas atuais.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Arquivo de esquema** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="current"      type="currentType">
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
|data  <br/> |xs:date  <br/> |obrigatório  <br/> |Especifica a data de hoje.  <br/> |Um valor do tipo xs:date  <br/> |
|dia  <br/> |xs:string  <br/> |opcional  <br/> |Especifica um dia para a previsão.  <br/> |Um valor do tipo xs:string  <br/> |
|feelslike  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica a temperatura da sensação térmica.  <br/> |Um valor do tipo xs:integer  <br/> |
|humidity  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica o valor numérico de umidade atual.  <br/> |Um valor do tipo xs:integer  <br/> |
|observationpoint  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica de onde as informações meteorológicas atuais são observadas.  <br/> |Um valor do tipo xs:string  <br/> |
|observationtime  <br/> |xs:time  <br/> |obrigatório  <br/> |Especifica quando as informações meteorológicas atuais são observadas.  <br/> |Um valor do tipo xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |opcional  <br/> |Especifica um dia na forma abreviada.  <br/> |Um valor do tipo xs:string  <br/> |
|skycode  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica um código em número inteiro das condições meteorológicas atuais.  <br/> |Um valor do tipo xs:integer  <br/> |
|skytext  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica uma ou duas palavras que descrevem as condições meteorológicas atuais.  <br/> |Um valor do tipo xs:string  <br/> |
|temperature  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica a temperatura atual do local.  <br/> |Um valor do tipo xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |obrigatório  <br/> |Uma cadeia de caracteres que descreve as condições de vento atual.  <br/> |Um valor do tipo xs:string  <br/> |
|windspeed  <br/> |xs:integer  <br/> |obrigatório  <br/> |Especifica o valor numérico da velocidade do vento atual.  <br/> |Um valor do tipo xs:integer  <br/> |
   

