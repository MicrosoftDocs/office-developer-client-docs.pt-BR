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
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361142"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (Esquema de informações sobre o clima do Outlook)

Define os parâmetros sobre as condições meteorológicas previstas para um local.
  
## <a name="type-information"></a>Informação de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Arquivo de esquema** <br/> |getweatherinfo.xsd  <br/> |
|**Base da extensão** <br/> |Nenhum  <br/> |
   
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

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
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
   

