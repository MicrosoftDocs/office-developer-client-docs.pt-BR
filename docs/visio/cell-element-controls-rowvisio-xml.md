---
title: Elemento Cell (Linha Controls) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Contém uma propriedade para uma alça de controle específica definida para uma forma.
ms.openlocfilehash: 662dfe730c92ae25b3d243364bf1fa22a5eb8605
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541831"
---
# <a name="cell-element-controls-row-visio-xml"></a>Elemento Cell (Linha Controls) (XML do Visio)

Contém uma propriedade para uma alça de controle específica definida para uma forma.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Elemento Row (Seção Controls)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Contém uma propriedade para uma alça de controle específica definida para uma forma.  <br/> |
   
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
|CanGlue  <br/> |Determina se uma alça de controle pode ser colada em outras formas.  <br/> |[Célula Can Glue (Seção Controls)](can-glue-cell-controls-section.md) <br/> |
|Aviso  <br/> |Representa uma cadeia de texto descritiva que aparece como uma ToolTip quando o usuário posiciona o ponteiro sobre a alça de controle da forma.  <br/> |[Célula Tip (Seção Controls)](tip-cell-controls-section.md) <br/> |
|X  <br/> |Representa a coordenada x que indica o local da alça de controle de uma forma em coordenadas locais.  <br/> |[Célula X Cell (Seção Controls)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Especifica o tipo de comportamento que a coordenada x da alça de controle exibirá depois de a alça ser movida.  <br/> |Nenhum.  <br/> |
|xDyn  <br/> |Representa a coordenada x de um ponto de ancoragem da alça de controle em coordenadas locais.  <br/> |[Célula X Dynamics (Seção Controls)](x-dynamics-cell-controls-section.md) <br/> |
|Y  <br/> |Representa a coordenada y que indica o local da alça de controle de uma forma em coordenadas locais.  <br/> |[Célula Y (Seção Controls)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Especifica o tipo de comportamento que a coordenada y da alça de controle irá exibir depois de a alça ser movida.  <br/> |Nenhum.  <br/> |
|YDyn  <br/> |Representa a coordenada y de um ponto de ancoragem da alça de controle em coordenadas locais.  <br/> |[Célula Y Dynamics (Seção Controls)](y-dynamics-cell-controls-section.md) <br/> |
   

