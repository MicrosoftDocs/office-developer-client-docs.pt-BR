---
title: Elemento RowMap (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Mapeia uma linha do conjunto de registros de dados a uma forma.
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385309"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a>Elemento RowMap (DataRecordSet_Type complexType) ('Visio XML')

Mapeia uma linha do conjunto de registros de dados a uma forma.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Recordsets.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

****

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |ID da página da forma vinculada aos dados na linha do conjunto de registros de dados identificado pela **RowID**.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|RowID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Identificação da linha da linha, exclusiva dentro do conjunto de registros de dados.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Identificação da forma  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Identificação da forma da forma vinculada aos dados na linha do conjunto de registros de dados identificado pela **RowID**.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

