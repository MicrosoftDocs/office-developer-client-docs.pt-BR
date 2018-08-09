---
title: DataRecordSet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 79fe048c578e8b9d8095d3fe7cd456af8ce08549
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771665"
---
# <a name="datarecordsettype-complextype-visio-xml"></a>DataRecordSet_Type complexType ('Visio XML')

## <a name="type-information"></a>Informações de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Extensão de base** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="DataRecordSet_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DataColumns"  type="DataColumns_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PrimaryKey"  type="PrimaryKey_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowMap"  type="RowMap_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshConflict"  type="RefreshConflict_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="AutoLinkComparison"  type="AutoLinkComparison_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ConnectionID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="Options"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TimeRefreshed"
  type="xsd:dateTime"
    />
    <xs:attribute name="NextRowID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="RowOrder"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshOverwriteAll"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshNoReconciliationUI"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshInterval"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReplaceLinks"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Checksum"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> ||
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Soma de verificação  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|Command  <br/> |XSD: String  <br/> |opcional  <br/> ||Valores do tipo xsd: String.  <br/> |
|Conexão  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |XSD: String  <br/> |opcional  <br/> ||Valores do tipo xsd: String.  <br/> |
|NextRowID  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|Options  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |XSD:Boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
|RefreshOverwriteAll  <br/> |XSD:Boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
|ReplaceLinks  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |XSD:Boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
|TimeRefreshed  <br/> |XSD: DateTime  <br/> |opcional  <br/> ||Valores do tipo xsd: DateTime.  <br/> |
   

