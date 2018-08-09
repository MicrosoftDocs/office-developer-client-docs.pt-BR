---
title: elemento de clima (weatherdata elemento) (esquema de local de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Especifica o local de clima de relatório no.
ms.openlocfilehash: a95e207845a9e54f5cac58b64ce85ec17b59fa22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771041"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>elemento de clima (weatherdata elemento) (esquema de local de clima do Outlook)

Especifica o local de clima de relatório no.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Arquivo de esquema** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[WeatherData](weatherdata-element-outlook-weather-location-schema.md) <br/> ||Define o elemento de clima.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica um código que está associado ao local para distinguir vários locais com o mesmo nome.  <br/> |Um valor do xs: string tipo  <br/> |
|weatherlocationname  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica o nome do local.  <br/> |Um valor do xs: string tipo  <br/> |
   

