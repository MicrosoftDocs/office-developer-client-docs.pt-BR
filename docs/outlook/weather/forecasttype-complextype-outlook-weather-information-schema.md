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
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (esquema de informações de clima do Outlook)

Define os parâmetros sobre as condições de clima previsão de um local.
  
## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Arquivo de esquema** <br/> |GetWeatherInfo.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

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

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
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
   

