---
title: Elemento Cell (Linha Actions) ("XML do Visio")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de marca de ação ou atalho.
ms.openlocfilehash: 01b81a593de07be8059263d7a6e6538f31ed3be1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356270"
---
# <a name="cell-element-actions-row-visio-xml"></a>Elemento Cell (Linha Actions) ("XML do Visio")

Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de marca de ação ou atalho.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
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
|[Elemento Row (Seção Actions)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de marca de ação ou atalho.  <br/> |
   
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
|Ação  <br/> |Contém a fórmula a ser executada quando um usuário escolhe um comando em um menu de marca de ação ou atalho.  <br/> |[Célula Action (Seção Actions)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Indica se um separador deve ser inserido no menu acima desta ação.  <br/> |[Célula BeginGroup (Seção Actions)](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |Identifica o ícone que aparece ao lado de um item em um menu de marca de ação ou atalho.  <br/> |[Célula ButtonFace (Seção Actions)](buttonface-cell-actions-section.md) <br/> |
|Checked  <br/> |Indica se um item é selecionado no menu de marca de ação ou atalho.  <br/> |[Célula Checked (Seção Actions)](checked-cell-actions-section.md) <br/> |
|Disabled  <br/> |Indica se um item está desabilitado no menu de marca de ação ou atalho.  <br/> |[Célula Disabled (Seção Actions)](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Determina se a linha é um submenu filho da última linha acima dela que não seja um submenu filho.  <br/> |[Célula FlyoutChild (Seção Actions)](flyoutchild-cell-actions-section.md) <br/> |
|Invisible  <br/> |Indica se a ação ficará visível no menu de marca de ação ou atalho.  <br/> |[Célula Invisible (Seção Actions)](invisible-cell-actions-section.md) <br/> |
|Menu  <br/> |Define o nome de um item de menu que aparece em um menu de marca de ação ou atalho de uma forma ou página.  <br/> |[Célula Menu (Seção Actions)](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Controla se a ação em um menu de marca de ação ou atalho é somente leitura ou não.  <br/> |[Célula ReadOnly (Seção Actions)](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Um número que determina a ordem das ações que aparecem no menu de marca de ação ou atalho.  <br/> |[Célula SortKey (Seção Actions)](sortkey-cell-actions-section.md) <br/> |
|TagName  <br/> |Contém o nome da marca de ação à qual essa ação está associada.  <br/> |[Célula TagName (Seção Actions)](tagname-cell-actions-section.md) <br/> |
   

