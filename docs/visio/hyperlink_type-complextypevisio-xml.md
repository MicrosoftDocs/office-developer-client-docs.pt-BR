---
title: Hyperlink_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: 226af4fee615b0dc6ddc4d92d13aff6dd1fd4b19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772024"
---
# <a name="hyperlinktype-complextype-visio-xml"></a>Hyperlink_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Section_Type  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="Hyperlink_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="HyperlinkRow_Type"
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
|[Row](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

Nenhum.
  

