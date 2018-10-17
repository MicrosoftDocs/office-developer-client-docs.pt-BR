---
title: weatherType complexType (Esquema de localização do clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Define os parâmetros sobre as condições meteorológicas para um local.
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387710"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>weatherType complexType (Esquema de localização do clima do Outlook)

Define os parâmetros sobre as condições meteorológicas para um local.
  
## <a name="type-information"></a>Informação de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Arquivo de esquema** <br/> |getweatherlocation.xsd  <br/> |
|**Base da extensão** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica um código associado ao local para distinguir vários locais com o mesmo nome.  <br/> |Um valor do tipo xs:string  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |obrigatório  <br/> |Especifica o nome do local.  <br/> |Um valor do tipo xs:string  <br/> |
   

