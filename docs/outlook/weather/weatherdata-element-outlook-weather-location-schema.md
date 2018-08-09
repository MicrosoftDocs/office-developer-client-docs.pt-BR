---
title: elemento WeatherData (esquema de local de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Define o elemento de clima.
ms.openlocfilehash: 5a3d0ed0fbf8d06472a6d9af727a41d97c0231cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771067"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a>elemento WeatherData (esquema de local de clima do Outlook)

Define o elemento de clima.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> ||
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Arquivo de esquema** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>Definição

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

Nenhum.
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[clima](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |Especifica o local de clima de relatório no.  <br/> |
   
### <a name="attributes"></a>Atributos

Nenhum.
  

