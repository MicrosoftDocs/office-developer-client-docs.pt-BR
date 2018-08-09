---
title: Trigger_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 38ba2800a32f4f1b4809a5e542fd6b79794bf369
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773177"
---
# <a name="triggertype-complextype-visio-xml"></a>Trigger_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |XSD: String  <br/> |obrigatório  <br/> ||Valores do tipo xsd: String.  <br/> |
   

