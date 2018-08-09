---
title: ForeignData_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771934"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>ForeignData_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD:Double  <br/> |opcional  <br/> ||Valores do tipo xsd:double.  <br/> |
|CompressionType  <br/> |XSD:token  <br/> |opcional  <br/> ||Valores do tipo xsd:token.  <br/> |
|ExtentX  <br/> |XSD:Double  <br/> |opcional  <br/> ||Valores do tipo xsd:double.  <br/> |
|ExtentY  <br/> |XSD:Double  <br/> |opcional  <br/> ||Valores do tipo xsd:double.  <br/> |
|ForeignType  <br/> |XSD:token  <br/> |obrigatório  <br/> ||Valores do tipo xsd:token.  <br/> |
|MappingMode  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |XSD:Double  <br/> |opcional  <br/> ||Valores do tipo xsd:double.  <br/> |
|ObjectType  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |XSD:Double  <br/> |opcional  <br/> ||Valores do tipo xsd:double.  <br/> |
|ShowAsIcon  <br/> |XSD:Boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
   

