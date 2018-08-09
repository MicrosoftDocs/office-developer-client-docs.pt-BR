---
title: weatherType complexType (esquema de informações de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Especifica as condições de clima de um local.
ms.openlocfilehash: b333bb6ce60dd1613bceda0a57e7e34c9819bd84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771036"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a>weatherType complexType (esquema de informações de clima do Outlook)

Especifica as condições de clima de um local.
  
## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Arquivo de esquema** <br/> |GetWeatherInfo.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[atual](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica as condições de clima atual.  <br/> |
|[previsão](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Especifica as condições de clima futuras de pelo menos três dias com antecedência incluindo hoje: hoje, amanhã, de depois de amanhã.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|atribuição  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica a fonte das informações de clima.  <br/> |Um valor do xs: string tipo  <br/> |
|degreetype  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica a unidade para a temperatura da localidade, por exemplo, Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica a URL da imagem para o local.  <br/> |Um valor do xs: string tipo  <br/> |
|fuso horário  <br/> |xs:Integer  <br/> |obrigatório  <br/> |Especifica o deslocamento de GMT.  <br/> |Um valor entre -11 e 12 inclusive  <br/> |
|url  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica a URL da página da web do serviço clima que contém informações de clima para o local especificado.  <br/> |Um valor do xs: string tipo  <br/> |
|weatherlocationcode  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica o código que está associado com o local usado para distinguir vários local que tiverem o mesmo nome.  <br/> |Um valor do xs: string tipo  <br/> |
|weatherlocationname  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica o nome do local que aparece no controle de lista suspensa.  <br/> |Um valor do xs: string tipo  <br/> |
   

