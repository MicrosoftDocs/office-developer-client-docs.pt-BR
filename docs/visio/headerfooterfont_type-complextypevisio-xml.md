---
title: HeaderFooterFont_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397244"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>HeaderFooterFont_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
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

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Escape  <br/> |XSD:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|FaceName  <br/> |XSD: String  <br/> |opcional  <br/> ||Valores do tipo xsd: String.  <br/> |
|Altura  <br/> |XSD:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|Itálico  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Orientation  <br/> |XSD:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|OutPrecision  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Quality  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Riscado  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Sublinhado  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedByte.  <br/> |
|Peso  <br/> |XSD:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|Largura  <br/> |XSD:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
   

