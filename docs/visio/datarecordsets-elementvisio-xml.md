---
title: Elemento DataRecordSets (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Contém todos os elementos DataRecordset do documento.
ms.openlocfilehash: efa7d58eabc1b1192862dbbe090ddd5008947c1d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542440"
---
# <a name="datarecordsets-element-visio-xml"></a>Elemento DataRecordSets (XML do Visio)

Contém todos os elementos **DataRecordset** do documento. 
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

Nenhum
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Contém todos os elementos **DataRecordset** do documento.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A ID do conjunto de registro de dados ativo na janela **Dados Externos** quando a janela é fechada, para que ele possa ser restaurado da próxima vez que a janela for aberta.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |xsd:string  <br/> |opcional  <br/> |A ordem dos conjuntos de registros de dados exibidos nas guias da janela **Dados Externos**. Uma lista ordenada de IDs de conjunto de registros de dados, separados por ponto e vírgula.  <br/> |Valores do tipo xsd:string.  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A próxima ID disponível para um novo conjunto de registros de dados.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

