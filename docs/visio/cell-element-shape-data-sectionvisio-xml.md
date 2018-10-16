---
title: Elemento Cell (Seção Dados da Forma) ("XML do Visio")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Especifica uma propriedade dos dados de forma.
ms.openlocfilehash: 5e0c79d9439fb3800a277e039143060eec708b11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390637"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Elemento Cell (Seção Dados da Forma) ("XML do Visio")

Especifica uma propriedade dos dados de forma.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Row (Seção Dados da Forma)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Shape Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |Especifica uma entrada de dados de forma para associar dados a uma forma.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica uma referência a uma página de desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que a fórmula gera um erro. O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.  <br/> |Uma cadeia de caracteres de mensagem de erro.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa a fórmula do elemento. Esse atributo pode conter uma das seguintes cadeias de caracteres:  <br/>  "(alguma fórmula)" se a fórmula existir localmente  <br/>  `No Formula` se a fórmula for excluída ou bloqueada localmente  <br/>  `Inh` se a fórmula for herdada.  <br/> |Uma fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |obrigatório  <br/> |Representa o nome da célula ShapeSheet.  <br/> |O nome da célula ShapeSheet.  <br/> Confira a seção Comentários abaixo.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa uma unidade de medida. O padrão é DL.  <br/> |As unidades da célula.  <br/> |
|V  <br/> |xsd:string  <br/> |opcional  <br/> |Representa o valor da célula.  <br/> |O valor da célula ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondem às células ShapeSheet. Confira a tabela a seguir para determinar os valores do atributo **N** permitidos para este elemento **Cell**. 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|Calendar  <br/> |Especifica o tipo de calendário usado quando o Tipo de um item de dados de forma é Date.  <br/> |[Célula Calendar (Seção Dados da Forma)](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Indica se a linha Dados da Forma está atualmente vinculada a um campo em um Conjunto de Registros de Dados.  <br/> ||
|Format  <br/> |Especifica a formatação de um item de dados da forma que pode ser uma sequência de caracteres, uma lista fixa, um número, uma lista variável, uma data ou hora, uma duração ou uma moeda.  <br/> |[Célula Format (Seção Dados da Forma)](format-cell-shape-data-section.md) <br/> |
|Invisible  <br/> |Especifica se o item de dados de forma ficará visível na janela Dados da Forma.  <br/> |[Célula Invisible (Seção Dados da Forma)](invisible-cell-shape-data-section.md) <br/> |
|Label  <br/> |Especifica o rótulo que aparece para os usuários na janela Dados da Forma. Um rótulo consiste de caracteres alfanuméricos, incluindo o caractere de sublinhado (_).  <br/> |[Célula Label (Seção Dados da Forma)](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Indica o idioma no qual o valor de dados de forma foi inserido.  <br/> |[Célula LangID (Seção Dados da Forma)](langid-cell-shape-data-section.md) <br/> |
|Aviso  <br/> |Especifica um texto descritivo ou de instruções que aparece como uma dica quando o mouse está pausado sobre um valor na janela Dados da Forma.  <br/> |[Célula Prompt (Seção Dados da Forma)](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Resulta em uma cadeia de caracteres que influencia a ordem na qual os itens na janela Dados da Forma são listados.  <br/> |[Célula SortKey (Seção Dados da Forma)](sortkey-cell-shape-data-section.md) <br/> |
|Type  <br/> |Especifica um tipo de dados para o valor dados da forma.  <br/> |[Célula Type (Seção Dados da Forma)](type-cell-shape-data-section.md) <br/> |
|Value  <br/> |Contém o valor do item de dados de forma conforme inserido na caixa de diálogo Dados da Forma.  <br/> |[Célula Value (Seção Dados da Forma)](value-cell-shape-data-section.md) <br/> |
|Verify  <br/> |Determina se um usuário é solicitado a inserir informações de propriedade personalizadas para uma forma quando uma instância é criada ou quando a forma é duplicada ou copiada.  <br/> |Nenhuma.  <br/> |
   

