---
title: PageSheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 70cd45ad803f9342b582f324b31f12ac5dff54c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772463"
---
# <a name="pagesheettype-complextype-visio-xml"></a>PageSheet_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Sheet_Type  <br/> |
   
## <a name="definition"></a>Definição

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|UniqueID  <br/> |XSD: String  <br/> |opcional  <br/> ||Valores do tipo xsd: String.  <br/> |
   

