---
title: Elemento Cell (Seção User-defined Cells) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ab7a11a0-a413-d4fe-ddf1-0d2e967dc21d
description: Uma propriedade de uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.
ms.openlocfilehash: 5b7e3eb1f4550430e4df51098b86862fcc7400da
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539311"
---
# <a name="cell-element-user-defined-cells-section-visio-xml"></a>Elemento Cell (Seção User-defined Cells) (Visio XML)

Uma propriedade de uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
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
|[Elemento Row (Seção User-defined Cells)](row-element-user-defined-cells-sectionvisio-xml.md) <br/> |[UserRow_Type](userrow_type-complextypevisio-xml.md) <br/> |Uma propriedade de uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica uma referência a uma página de desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que a fórmula gera um erro. O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.  <br/> |Uma cadeia de caracteres de mensagem de erro.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa a fórmula do elemento. Esse atributo pode conter uma das seguintes cadeias de caracteres:  <br/>  '(alguma fórmula)' se a fórmula existir localmente  <br/>  `No Formula` se a fórmula estiver excluída ou bloqueada localmente  <br/>  `Inh` se a fórmula for herdada.  <br/> |Uma fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |obrigatório  <br/> |Representa o nome da célula ShapeSheet.  <br/> |O nome da célula ShapeSheet.  <br/> Confira a seção Comentários abaixo.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa uma unidade de medida. O padrão é DL.  <br/> |As unidades da célula.  <br/> |
|S  <br/> |xsd:string  <br/> |opcional  <br/> |Representa o valor da célula.  <br/> |O valor da célula ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet. Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**. 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|Prompt  <br/> |Especifica um aviso descritivo ou comentário para a célula definida pelo usuário.  <br/> |[Célula Prompt (Seção User-Defined Cells)](prompt-cell-user-defined-cells-section.md) <br/> |
|Valor  <br/> |Especifica um valor para a célula correspondente definida pelo usuário.  <br/> |[Célula Value (Seção User-Defined Cells)](value-cell-user-defined-cells-section.md) <br/> |
   

