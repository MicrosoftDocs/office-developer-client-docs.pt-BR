---
title: Elemento DataColumns (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contém todos os elementos de DataColumn em um conjunto de registros de dados.
ms.openlocfilehash: b90b6cb18fc2bd1edc393d58a9d761cfb36ea220
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771652"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a>Elemento DataColumns (DataRecordSet_Type complexType) ('Visio XML')

Contém todos os elementos de **DataColumn** em um conjunto de registros de dados. 
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Recordsets.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataColumn](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |Define como uma coluna de dados aparece na janela **Dados externos** na interface do usuário do Visio e qualifica os dados na coluna definindo seu tipo de dados e formatação.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|SortAsc  <br/> |XSD:Boolean  <br/> |opcional  <br/> |A coluna no qual você deseja classificar os dados.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|SortColumn  <br/> |XSD: String  <br/> |opcional  <br/> |Se deseja classificar a coluna **SortColumn** em crescente (1) ou em ordem decrescente de (0).  <br/> |Valores do tipo xsd: String.  <br/> |
   

