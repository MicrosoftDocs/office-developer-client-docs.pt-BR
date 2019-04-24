---
title: Masters_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341654"
---
# <a name="masterstype-complextype-visio-xml"></a>Masters_Type complexType (' Visio XML ')

## <a name="type-information"></a>Informação de tipo

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base da extensão** <br/> |Nenhum  <br/> |
   
## <a name="definition"></a>Definição

```XML
          <xs:complexType name="Masters_Type">
          
          <xs:sequence>
    <xs:element name="Master"  type="Master_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="MasterShortcut"  type="MasterShortcut_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> ||
|[MasterShortcut](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Atributos

Nenhum.
  

