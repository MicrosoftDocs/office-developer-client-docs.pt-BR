---
title: Connect_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9a321a3ff910afb183e1a697eaad9dfb51125524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771572"
---
# <a name="connecttype-complextype-visio-xml"></a>Connect_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
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
|FromCell  <br/> |XSD: String  <br/> |opcional  <br/> ||Valores do tipo xsd: String.  <br/> |
|FromPart  <br/> |XSD:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|FromSheet  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|ToCell  <br/> |XSD: String  <br/> |opcional  <br/> ||Valores do tipo xsd: String.  <br/> |
|ToPart  <br/> |XSD:int  <br/> |opcional  <br/> ||Valores do tipo xsd:int.  <br/> |
|ToSheet  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
   

