---
title: Connection_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c0ac13b-70cc-398b-a1a3-e7d8080c8f7b
ms.openlocfilehash: d927a70a887de93609755246e879381ab884e925
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771597"
---
# <a name="connectiontype-complextype-visio-xml"></a>Connection_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Section_Type  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="Connection_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ConnectionRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Row](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

Nenhum.
  

