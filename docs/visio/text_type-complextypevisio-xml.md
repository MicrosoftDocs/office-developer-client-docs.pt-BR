---
title: Text_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: 3309184c47eaf6c6a8cb20d7c6485c21c5ec8c50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773100"
---
# <a name="texttype-complextype-visio-xml"></a>Text_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="Text_Type">
          
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="cp"  type="cp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="pp"  type="pp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="tp"  type="tp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="fld"  type="fld_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[CP](cp-element-text_type-complextypevisio-xml.md) <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> ||
|[fld](fld-element-text_type-complextypevisio-xml.md) <br/> |[fld_Type](fld_type-complextypevisio-xml.md) <br/> ||
|[PP](pp-element-text_type-complextypevisio-xml.md) <br/> |[pp_Type](pp_type-complextypevisio-xml.md) <br/> ||
|[PA](tp-element-text_type-complextypevisio-xml.md) <br/> |[tp_Type](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

Nenhum.
  

