---
title: DataColumns_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: f125bce02fab43b808608ef6b14d59dfc08a1179
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771650"
---
# <a name="datacolumnstype-complextype-visio-xml"></a>DataColumns_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="DataColumns_Type">
          
          <xs:sequence>
    <xs:element name="DataColumn"  type="DataColumn_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="SortColumn"
  type="xsd:string"
    />
    <xs:attribute name="SortAsc"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataColumn](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|SortAsc  <br/> |XSD:Boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
|SortColumn  <br/> |XSD: String  <br/> |opcional  <br/> ||Valores do tipo xsd: String.  <br/> |
   

