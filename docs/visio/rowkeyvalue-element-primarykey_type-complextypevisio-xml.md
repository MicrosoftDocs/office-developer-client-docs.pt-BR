---
title: Elemento RowKeyValue (PrimaryKey_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Especifica o valor de uma chave primária para uma linha individual de um recordset.
ms.openlocfilehash: 3b91997b5fe8184eb89f8c53197a512d809171b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772809"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a>Elemento RowKeyValue (PrimaryKey_Type complexType) ('Visio XML')

Especifica o valor de uma chave primária para uma linha individual de um recordset.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RowKeyValue_Type](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Recordsets.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Especifica uma chave primária de um recordset.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|RowID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Um valor exclusivo que identifica uma linha de um recordset.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Value  <br/> |XSD: String  <br/> |obrigatório  <br/> |O valor da chave primária para esta linha do recordset.  <br/> |Valores do tipo xsd: String.  <br/> |
   

