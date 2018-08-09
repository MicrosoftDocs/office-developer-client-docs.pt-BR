---
title: Elemento DataRecordSets ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Contém todos os elementos de DataRecordset no documento.
ms.openlocfilehash: 205c4d963f111490698627040c190f322f2f36a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771661"
---
# <a name="datarecordsets-element-visio-xml"></a>Elemento DataRecordSets ('Visio XML')

Contém todos os elementos de **DataRecordset** no documento. 
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Recordsets.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

Nenhum.
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Contém todos os elementos de **DataRecordset** no documento.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A identificação do conjunto de registros de dados ativo na janela **Dados externos** quando a janela fecha, para que ele possa ser restaurado na próxima vez que a janela é aberta.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |XSD: String  <br/> |opcional  <br/> |A ordem dos conjuntos de registros de dados exibidos nas guias da janela **Dados externos** . Uma lista ordenada de IDs de registros de dados, separados por ponto e vírgula.  <br/> |Valores do tipo xsd: String.  <br/> |
|NextID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A identificação disponível próxima para um novo conjunto de registros de dados.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

