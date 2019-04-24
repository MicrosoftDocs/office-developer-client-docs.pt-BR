---
title: HeaderFooterFont_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335620"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (' Visio XML ')

## <a name="type-information"></a>Informação de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base da extensão** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Escape  <br/> |xsd:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|FaceName  <br/> |xsd:string  <br/> |opcional  <br/> ||Valores do tipo xsd:string.  <br/> |
|Altura  <br/> |xsd:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|Itálico  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Orientação  <br/> |xsd:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|Precisão  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Quality  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Risca  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Sublinhado  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Peso  <br/> |xsd:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|Largura  <br/> |xsd:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
   

