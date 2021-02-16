---
title: Elemento AutoLinkComparison (DataRecordSet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Define uma regra que compara uma coluna pai do elemento DataRecordset com um item de dados de forma na última ação de vinculação automática bem-sucedida, executadas na interface do usuário.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537868"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a>Elemento AutoLinkComparison (DataRecordSet_Type complexType) (XML do Visio)

Define uma regra que compara uma coluna pai do elemento **ConjuntoDeRegistrosDeDados** com um item de dados de forma na última ação de vinculação automática bem-sucedida, executadas na interface do usuário. 
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Especifica um conjunto de registros e a vinculação de dados entre esse conjunto e as formas em páginas de desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd:string  <br/> |obrigatório  <br/> |Corresponde a um nome de coluna do conjunto de registros ADO.  <br/> |Valores do tipo xsd:string.  <br/> |
|ContextType  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Especifica as propriedades do grupo ou da forma a serem usadas para a comparação. Os valores possíveis são mostrados na tabela a seguir.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |xsd:string  <br/> |opcional  <br/> |Se o valor de ContextType for 2 ou 3, esse atributo será obrigatório para definir uma comparação. Se ContextType = 2, ContextTypeLabel deverá ser o rótulo do item de dados da forma. Se **ContextType** = 3, ContextTypeLabel deverá ser o nome da linha local.  <br/> |Valores do tipo xsd:string.  <br/> |
   

