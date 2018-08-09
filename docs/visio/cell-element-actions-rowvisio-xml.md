---
title: Elemento de célula (linha Actions) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de atalho ou de ação de marca.
ms.openlocfilehash: d0f103e6f241a7982bcc2663752d9338cf4c3eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771424"
---
# <a name="cell-element-actions-row-visio-xml"></a>Elemento de célula (linha Actions) ('Visio XML')

Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de atalho ou de ação de marca.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Masters.XML,. XML de # mestre, pages.xml,. XML n º de página  <br/> |
   
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
|[Elemento Row (Seção Actions)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de atalho ou de ação de marca.  <br/> |
   
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
|Ação  <br/> |Contém a fórmula a ser executada quando o usuário escolhe um comando em um menu de atalho ou de ação de marca.  <br/> |[Célula Action (Seção Actions)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Indica se um separador está inserido no menu acima desta ação.  <br/> |[Célula BeginGroup (Seção Actions)](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |Identifica o ícone exibido ao lado de um item em um menu de atalho ou de ação de marca.  <br/> |[Célula ButtonFace (Seção Actions)](buttonface-cell-actions-section.md) <br/> |
|Verificado  <br/> |Indica se um item é verificado no menu de atalho ou marca de ação.  <br/> |[Célula Checked (Seção Actions)](checked-cell-actions-section.md) <br/> |
|Desabilitado  <br/> |Indica se um item em um menu de atalho ou de marca de ação está desabilitado.  <br/> |[Célula Disabled (Seção Actions)](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Determina se a linha é um menu de submenu filho da última linha acima da que não é filha de submenu.  <br/> |[Célula FlyoutChildd (Seção Actions)](flyoutchild-cell-actions-section.md) <br/> |
|Invisível  <br/> |Indica se uma ação é visível em um menu de atalho ou marca de ação.  <br/> |[Célula Invisible (Seção Actions)](invisible-cell-actions-section.md) <br/> |
|Menu  <br/> |Define o nome de um item de menu exibido em um menu de atalho ou de marca de ação para uma forma ou página.  <br/> |[Célula Menu (Seção Actions)](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Controla se a ação em um menu de atalho ou de marca de ação é somente leitura.  <br/> |[Célula ReadOnly (Seção Actions)](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Um número que determina a ordem de ações exibidas em um menu de atalho ou de marca de ação.  <br/> |[Célula SortKey de célula SortKey (seção Actions) (seção Actions)](sortkey-cell-actions-section.md) <br/> |
|TagName  <br/> |Contém o nome da marca de ação a que esta ação está associada.  <br/> |[Célula TagName (Seção Actions)](tagname-cell-actions-section.md) <br/> |
   

