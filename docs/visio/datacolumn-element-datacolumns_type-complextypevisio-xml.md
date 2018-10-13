---
title: Elemento DataColumn (DataColumns_Type complexType) ("XML do Visio")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Define a aparência de uma coluna de dados na janela Dados Externos na interface de usuário do Visio, e qualifica os dados na coluna definindo o tipo de dados e a formatação.
ms.openlocfilehash: 453ff44131575bd3d6927fdddb81db5f3f431a3b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395844"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>Elemento DataColumn (DataColumns_Type complexType) ("XML do Visio")

Define a aparência de uma coluna de dados na janela **Dados Externos** na interface de usuário do Visio e qualifica os dados na coluna definindo o tipo de dados e formatação. 
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contém todos os elementos de **DataColumn** em um conjunto de registros de dados.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Calendar  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |ID do Calendário da coluna de dados.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |obrigatório  <br/> |Nome externo da coluna de dados. É exibido em títulos na janela **Dados Externos** e nos rótulos de gráficos de dados.  <br/> |Valores do tipo xsd:string.  <br/> |
|Currency  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |ID de Moeda da coluna de dados.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Tipo dos dados na coluna de dados.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica o grau (potência) das unidades, por exemplo ao quadrado ou ao cubo. O padrão (atributo ausente) é 1.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Define a posição de exibição da coluna de dados na janela **Dados Externos**, da coluna mais à esquerda (0) à coluna mais à direita (maior valor).  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Largura da coluna de dados na janela **Dados Externos**.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Hyperlink  <br/> |xsd:boolean  <br/> |opcional  <br/> |Define se a coluna de dados criará um hiperlink em uma forma quando a forma for vinculada a dados.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Label  <br/> |xsd:string  <br/> |obrigatório  <br/> |Rótulo da coluna de dados.  <br/> |Valores do tipo xsd:string.  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |ID de idioma da coluna de dados.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Mapped  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se a coluna ficará visível na janela **Dados Externos**. True (1) para a coluna ficar visível; False (0) para a coluna não ficar visível. O padrão (atributo ausente) é a coluna ficar visível.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Name  <br/> |xsd:string  <br/> |obrigatório  <br/> |Nome interno da coluna de dados. Usado como o nome da linha para o item de dados da forma (propriedade personalizada) adicionado a uma forma, quando a forma está vinculada a uma linha de dados.  <br/> |Valores do tipo xsd:string.  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |opcional  <br/> |Rótulo de coluna retornado para o Visio pela interface ADO subjacente.  <br/> |Valores do tipo xsd:string.  <br/> |
|UnitType  <br/> |xsd:string  <br/> |opcional  <br/> |Tipo de unidade dos dados na coluna de dados.  <br/> |Valores do tipo xsd:string.  <br/> |
   

