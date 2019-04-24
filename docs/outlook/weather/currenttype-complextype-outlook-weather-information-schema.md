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
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (Esquema de informações sobre o clima do Outlook)

Define os parâmetros sobre as condições meteorológicas atuais para um local.
  
## <a name="type-information"></a>Informação de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Arquivo de esquema** <br/> |getweatherinfo.xsd  <br/> |
|**Base da extensão** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

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

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
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
   

