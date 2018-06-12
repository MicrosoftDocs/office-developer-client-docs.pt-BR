---
title: Elemento AutoLinkComparison (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Define uma regra que compara uma coluna no elemento pai DataRecordset com um item de dados da forma da última bem-sucedida automática vinculação ação executada na interface do usuário.
ms.openlocfilehash: 38970a84676f769c36c9bdc3f8334652f7d9ec21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771292"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>Elemento AutoLinkComparison (DataRecordSet_Type complexType) ('Visio XML')

Define uma regra que compara uma coluna no elemento pai **DataRecordset** com um item de dados da forma da última bem-sucedida automática vinculação ação executada na interface do usuário. 
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Recordsets.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Especifica um conjunto de registros e a vinculação de dados entre esse recordset e as formas em páginas de desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |XSD: String  <br/> |obrigatório  <br/> |Corresponde a um nome de coluna no conjunto de registros ADO.  <br/> |Valores do tipo xsd: String.  <br/> |
|ContextType  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Especifica as propriedades do grupo ou forma a ser usada para comparação. Valores possíveis são mostrados na tabela a seguir.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |XSD: String  <br/> |opcional  <br/> |Se o valor de ContextType for 2 ou 3, este atributo é necessário para definir uma comparação. Para ContextType = 2, ContextTypeLabel deve ser o rótulo de item de dados de forma e se **ContextType** = 3, ContextTypeLabel deve ser o nome de linha local.  <br/> |Valores do tipo xsd: String.  <br/> |
   

