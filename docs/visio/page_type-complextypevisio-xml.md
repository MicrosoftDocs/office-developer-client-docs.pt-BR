---
title: Page_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334395"
---
# <a name="pagetype-complextype-visio-xml"></a>Page_Type complexType (' Visio XML ')

## <a name="type-information"></a>Informação de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base da extensão** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="Page_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Background"
  type="xsd:boolean"
    />
    <xs:attribute name="BackPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
    <xs:attribute name="ReviewerID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AssociatedPage"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-page_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|AssociatedPage  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|Background  <br/> |xsd:boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
|BackPage  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |opcional  <br/> ||Valores do tipo xsd:boolean.  <br/> |
|Name  <br/> |xsd:string  <br/> |opcional  <br/> ||Valores do tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |opcional  <br/> ||Valores do tipo xsd:string.  <br/> |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> ||Valores do tipo xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores do tipo xsd: Double.  <br/> |
|ViewCenterY  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores do tipo xsd: Double.  <br/> |
|ViewScale  <br/> |xsd: Double  <br/> |opcional  <br/> ||Valores do tipo xsd: Double.  <br/> |
   

