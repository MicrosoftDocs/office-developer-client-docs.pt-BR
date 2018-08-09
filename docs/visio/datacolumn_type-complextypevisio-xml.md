---
title: DataColumn_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 9d334190b686f3b2c5e25a31336c668c957e820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771648"
---
# <a name="datacolumntype-complextype-visio-xml"></a>DataColumn_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
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
|Calendário  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |XSD: String  <br/> |obrigatório  <br/> ||Valores do tipo xsd: String.  <br/> |
|Moeda  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedShort.  <br/> |
|DataType  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedShort.  <br/> |
|Degree  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|Hiperlink  <br/> |XSD:Boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
|Rótulo  <br/> |XSD: String  <br/> |obrigatório  <br/> ||Valores do tipo xsd: String.  <br/> |
|LangID  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|Mapeadas  <br/> |XSD:Boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
|Nome  <br/> |XSD: String  <br/> |obrigatório  <br/> ||Valores do tipo xsd: String.  <br/> |
|OrigLabel  <br/> |XSD: String  <br/> |opcional  <br/> ||Valores do tipo xsd: String.  <br/> |
|UnitType  <br/> |XSD: String  <br/> |opcional  <br/> ||Valores do tipo xsd: String.  <br/> |
   

