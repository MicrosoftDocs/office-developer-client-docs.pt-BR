---
title: Elemento de célula (seção Shape Data) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Especifica uma propriedade dos dados da forma.
ms.openlocfilehash: 899b518f86979c831c0c05913420c7a62f0ea717
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771496"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Elemento de célula (seção Shape Data) ('Visio XML')

Especifica uma propriedade dos dados da forma.
  
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
|[Elemento Row (Seção Shape Data)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Forma Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |Especifica uma entrada de dados de forma para associar os dados uma forma.  <br/> |
   
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
|Calendário  <br/> |Especifica o tipo de calendário a ser usado quando o Tipo de um item de dados for Data.  <br/> |[Célula Calendar (Seção Shape Data)](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Indica se a linha de dados da forma estiver atualmente vinculada a um campo em um conjunto de registros de dados.  <br/> ||
|Formatar  <br/> |Especifica a formatação de um item de dados da forma que pode ser uma sequência de caracteres, uma lista fixa, um número, uma lista variável, uma data ou hora, uma duração ou uma moeda.  <br/> |[Célula Format (Seção Shape Data)](format-cell-shape-data-section.md) <br/> |
|Invisível  <br/> |Especifica se o item de dados da forma será visível na janela Dados da Forma.  <br/> |[Célula Invisible (Seção Shape Data)](invisible-cell-shape-data-section.md) <br/> |
|Rótulo  <br/> |Especifica o rótulo exibido aos usuários na janela Dados da Forma. Um rótulo consiste em caracteres alfanuméricos, incluindo o caractere de sublinhado (_).  <br/> |[Célula Label (Seção Shape Data)](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Indica o idioma no qual o valor dos dados da forma foi inserido.  <br/> |[Célula LangID (Seção Shape Data)](langid-cell-shape-data-section.md) <br/> |
|Prompt  <br/> |Especifica o texto descritivo ou instrucional exibido como uma dica ao posicionar o mouse sobre o valor na janela Dados da Forma.  <br/> |[Célula Prompt (Seção Shape Data)](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Avalia uma cadeia de caracteres que influencia a ordem em que os itens são listados na janela Dados de Forma.  <br/> |[Célula SortKey (Seção Shape Data)](sortkey-cell-shape-data-section.md) <br/> |
|Tipo  <br/> |Especifica um tipo de dado para o valor de dados da forma.  <br/> |[Célula Type (Seção Shape Data)](type-cell-shape-data-section.md) <br/> |
|Value  <br/> |Contém o valor do item de dados da forma inserido na caixa de diálogo Definir Dados da Forma.  <br/> |[Célula Value (Seção Shape Data)](value-cell-shape-data-section.md) <br/> |
|Verifique se  <br/> |Especifica se o usuário é solicitado a digitar informações de propriedade personalizada para uma forma quando uma instância é criada ou a forma é duplicada ou copiada.  <br/> |Nenhum.  <br/> |
   

