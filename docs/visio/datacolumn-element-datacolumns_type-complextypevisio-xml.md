---
title: Elemento DataColumn (DataColumns_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Define como uma coluna de dados aparece na janela dados externos na interface do usuário do Visio e qualifica os dados na coluna definindo seu tipo de dados e formatação.
ms.openlocfilehash: f74061b9f3b8f4b93d8aa0e97e4e7c1e45131cbd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771672"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>Elemento DataColumn (DataColumns_Type complexType) ('Visio XML')

Define como uma coluna de dados aparece na janela **Dados externos** na interface do usuário do Visio e qualifica os dados na coluna definindo seu tipo de dados e formatação. 
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Recordsets.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contém todos os elementos de **DataColumn** em um conjunto de registros de dados.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Calendário  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |ID do calendário da coluna de dados.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |XSD: String  <br/> |obrigatório  <br/> |Nome externo da coluna de dados. É exibida nos títulos de na janela **Dados externos** e em rótulos de gráficos de dados.  <br/> |Valores do tipo xsd: String.  <br/> |
|Moeda  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |ID de moeda da coluna de dados.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|DataType  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |Tipo de dados da coluna de dados.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|Degree  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica o grau (alimentação) das unidades, por exemplo quadradas ou ao cubo. O padrão (atributo absent) é 1.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Define a posição de exibição da coluna de dados na janela **Dados externos** , na coluna mais à esquerda (0) à coluna mais à direita (maior valor).  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Largura da coluna de dados na janela **Dados externos** .  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Hiperlink  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Se a coluna de dados cria um hiperlink em uma forma quando a forma está vinculada aos dados.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Rótulo  <br/> |XSD: String  <br/> |obrigatório  <br/> |Rótulo da coluna de dados.  <br/> |Valores do tipo xsd: String.  <br/> |
|LangID  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A ID de idioma da coluna de dados.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Mapeadas  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica se a coluna é visível na janela **Dados externos** . Verdadeiro (1) para a coluna fique visível; False (0) para a coluna não devem ficar visíveis. O padrão (atributo absent) é para a coluna fique visível.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Nome  <br/> |XSD: String  <br/> |obrigatório  <br/> |Nome interno da coluna de dados. Usado como o nome da linha para o item de dados da forma (propriedades personalizadas) adicionado a uma forma quando a forma está vinculada a uma linha de dados.  <br/> |Valores do tipo xsd: String.  <br/> |
|OrigLabel  <br/> |XSD: String  <br/> |opcional  <br/> |Rótulo da coluna retornado para o Visio pela interface ADO subjacente.  <br/> |Valores do tipo xsd: String.  <br/> |
|UnitType  <br/> |XSD: String  <br/> |opcional  <br/> |Tipo de unidade de dados da coluna de dados.  <br/> |Valores do tipo xsd: String.  <br/> |
   

