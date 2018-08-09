---
title: Paragraph_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: 4d15d262d66a2d247aa432d08b22e6fe3a460e2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772481"
---
# <a name="paragraphtype-complextype-visio-xml"></a>Paragraph_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Section_Type  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="Paragraph_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ParagraphRow_Type"
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
|[Row](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

Nenhum.
  

