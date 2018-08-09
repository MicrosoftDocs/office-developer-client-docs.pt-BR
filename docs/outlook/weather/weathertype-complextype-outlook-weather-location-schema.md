---
title: weatherType complexType (esquema de local de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Define os parâmetros sobre as condições de clima de um local.
ms.openlocfilehash: 39dcc63dfc9b7a97b9643e804329fd1795d39201
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771050"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>weatherType complexType (esquema de local de clima do Outlook)

Define os parâmetros sobre as condições de clima de um local.
  
## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Arquivo de esquema** <br/> |getweatherlocation.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica um código que está associado ao local para distinguir vários locais com o mesmo nome.  <br/> |Um valor do xs: string tipo  <br/> |
|weatherlocationname  <br/> |xs: String  <br/> |obrigatório  <br/> |Especifica o nome do local.  <br/> |Um valor do xs: string tipo  <br/> |
   

