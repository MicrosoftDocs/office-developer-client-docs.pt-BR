---
title: Elemento Cell (Seção Field) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Exibe as funções e fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.
ms.openlocfilehash: f6c3c724b210ad579012ff58b93333e28c2a8cf1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383335"
---
# <a name="cell-element-field-section-visio-xml"></a>Elemento Cell (Seção Field) ('Visio XML')

Exibe as funções e fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.
  
## <a name="element-information"></a>Informações do elemento

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

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Row (Seção Field)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Exibe as funções e fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.  <br/> |
   
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
|Calendário  <br/> |Determina o calendário a ser usado para um campo de texto quando o tipo de dado for Data.  <br/> |[Célula Calendar (Seção Text Fields)](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |Especifica a formatação de um campo de texto que pode ser uma sequência de caracteres, um número, uma data ou hora, uma duração ou uma moeda.  <br/> |[Célula Format (Seção Text Fields)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Indica o tipo de campo de texto.  <br/> |[Célula ObjectKind (Seção Text Fields)](objectkind-cell-text-fields-section.md) <br/> |
|Tipo  <br/> |Especifica um tipo de dados para o campo de texto.  <br/> |[Célula Type (Seção Text Fields)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Determina a categoria de um campo inserido. Esta célula é usada pelas caixas de diálogo Campo e Formato de dados para determinar as informações de campo e categoria.  <br/> |[Célula UICategory (Seção Text Fields)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Determina o código de um campo inserido. Esta célula é usada pelas caixas de diálogo Campo e Formato de dados para determinar as informações de campo e categoria.  <br/> |[Célula UICode (Seção Text Fields)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Determina o formato de um campo inserido. Esta célula é usada pelas caixas de diálogo Campo e Formato de dados para determinar as informações  <br/> |[Célula UIFormat (Seção Text Fields)](uiformat-cell-text-fields-section.md) <br/> |
|Value  <br/> |Contém a função de um campo.  <br/> |[Célula Value (Seção Text Fields)](value-cell-text-fields-section.md) <br/> |
   

