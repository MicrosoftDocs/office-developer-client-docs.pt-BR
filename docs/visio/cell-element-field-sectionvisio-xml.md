---
title: Elemento de célula (seção de campo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Exibe as funções e as fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.
ms.openlocfilehash: 94c9807984ef0e327c1cc9f8449d1ea065fdd717
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771445"
---
# <a name="cell-element-field-section-visio-xml"></a>Elemento de célula (seção de campo) ('Visio XML')

Exibe as funções e as fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |# XML do mestre, página # XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Row (Seção Field)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Exibe as funções e as fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica uma referência a uma página de desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: String  <br/> |opcional  <br/> |Indica que a fórmula é avaliada como um erro. O valor de **f** é o valor atual (uma sequência de mensagem de erro;) o valor do atributo **V** é o último valor válido.  <br/> |Uma cadeia de caracteres de mensagem de erro.  <br/> |
|S  <br/> |XSD: String  <br/> |opcional  <br/> | Representa a fórmula do elemento. Este atributo pode conter uma das cadeias de caracteres seguintes:  <br/>  '(alguns formula)' se a fórmula existe localmente  <br/>  `No Formula`Se a fórmula localmente é excluída ou bloqueada  <br/>  `Inh`Se a fórmula for herdada.  <br/> |Uma fórmula.  <br/> |
|N  <br/> |XSD: String  <br/> |obrigatório  <br/> |Representa o nome da célula ShapeSheet.  <br/> |O nome da célula ShapeSheet.  <br/> Consulte a seção comentários abaixo.  <br/> |
|U  <br/> |XSD: String  <br/> |opcional  <br/> |Representa uma unidade de medida padrão é DL.  <br/> |As unidades da célula.  <br/> |
|V  <br/> |XSD: String  <br/> |opcional  <br/> |Representa o valor da célula.  <br/> |O valor da célula ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **N** deste elemento de **célula** deve ser um conjunto limitado de valores que corresponde às células da ShapeSheet. Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para esse elemento de **célula** . 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|Calendário  <br/> |Determina o calendário que é usado para um campo de texto quando o tipo de dado for Data.  <br/> |[Célula Calendar (Seção Text Fields)](calendar-cell-text-fields-section.md) <br/> |
|Formatar  <br/> |Especifica a formatação de um campo de texto que pode ser uma sequência de caracteres, um número, uma data ou uma hora, uma duração ou uma moeda.  <br/> |[Célula Format (Seção Text Fields)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Indica o tipo de campo de texto.  <br/> |[Célula ObjectKind (Seção Text Fields)](objectkind-cell-text-fields-section.md) <br/> |
|Tipo  <br/> |Especifica um tipo de dado para o valor do campo de texto.  <br/> |[Célula Type (Seção Text Fields)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Determina a categoria de um campo inserido. Esta célula é usada pelas caixas de diálogo de formato de campo e dados para determinar as informações de campo e categoria.  <br/> |[Célula UICategory (Seção Text Fields)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Determina o código de um campo inserido. Esta célula é usada pelas caixas de diálogo de formato de campo e dados para determinar as informações de campo e categoria.  <br/> |[Célula UICode (Seção Text Fields)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Determina o formato de um campo inserido. Esta célula é utilizada pelas caixas de diálogo de formato de campo e dados para determinar o campo e  <br/> |[Célula UIFormat (Seção Text Fields)](uiformat-cell-text-fields-section.md) <br/> |
|Value  <br/> |Contém a função para um campo.  <br/> |[Célula Value (Seção Text Fields)](value-cell-text-fields-section.md) <br/> |
   

