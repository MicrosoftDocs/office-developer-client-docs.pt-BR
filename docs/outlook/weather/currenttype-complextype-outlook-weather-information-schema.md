---
title: currentType complexType (esquema de informações de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Define os parâmetros sobre as condições de clima atual de um local.
ms.openlocfilehash: 55ea2cfa6904d88c695268675bc7a893fa643010
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770965"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (esquema de informações de clima do Outlook)

Define os parâmetros sobre as condições de clima atual de um local.
  
## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Arquivo de esquema** <br/> |GetWeatherInfo.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
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

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|data  <br/> |Date  <br/> |obrigatório  <br/> |Especifica a data de hoje.  <br/> |Um valor de Date o tipo  <br/> |
|dia  <br/> |xs: String  <br/> |opcional  <br/> |Especifica um dia para a previsão.  <br/> |Um valor do xs: string tipo  <br/> |
|feelslike  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica a temperatura de como o clima atual se parece com.  <br/> |Um valor de xs:integer do tipo  <br/> |
|Umidade  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica o valor numérico umidade atual.  <br/> |Um valor de xs:integer do tipo  <br/> |
|observationpoint  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica onde as informações atuais de clima observadas de.  <br/> |Um valor do xs: string tipo  <br/> |
|observationtime  <br/> |xs: time  <br/> |obrigatório  <br/> |Especifica quando as informações atuais de clima são observadas em.  <br/> |Um valor do xs: time do tipo  <br/> |
|shortday  <br/> |xs: String  <br/> |opcional  <br/> |Especifica um dia na forma abreviada.  <br/> |Um valor do xs: string tipo  <br/> |
|skycode  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica um código de inteiro para as condições de clima atual.  <br/> |Um valor de xs:integer do tipo  <br/> |
|skytext  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica duas palavras descrevendo condições de clima atual.  <br/> |Um valor do xs: string tipo  <br/> |
|temperatura  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica a temperatura atual do local.  <br/> |Um valor de xs:integer do tipo  <br/> |
|winddisplay  <br/> |xs: String  <br/> |obrigatório  <br/> |Uma cadeia de caracteres que descreve as condições de vento atual.  <br/> |Um valor do xs: string tipo  <br/> |
|windspeed  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica o valor atual de velocidade de vento numérico.  <br/> |Um valor de xs:integer do tipo  <br/> |
   

