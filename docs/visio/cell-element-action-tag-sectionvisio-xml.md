---
title: Elemento Cell (Seção Marca de Ação) ("XML do Visio")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Define uma propriedade para uma marca de ação em uma forma ou página.
ms.openlocfilehash: 61fad8575532adde0106ef6db2888fe38f3ae4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337174"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Elemento Cell (Seção Marca de Ação) ("XML do Visio")

Define uma propriedade para uma marca de ação em uma forma ou página.
  
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
|[Elemento Row (Seção ActionTag)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Define uma marca de ação em uma forma ou a página.  <br/> |
   
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
|ButtonFace  <br/> |Contém a ID da imagem de face do botão que é exibida no botão de marca de ação.  <br/> |[Célula ButtonFace (Seção Marcas de Ação)](buttonface-cell-action-tags-section.md) <br/> |
|Descrição  <br/> |Contém uma cadeia de caracteres que descreve a marca de ação, que aparece como uma dica de ferramenta quando os usuários colocam o ponteiro sobre a marca.  <br/> |[Célula Description (Seção Marcas de Ação)](description-cell-action-tags-section.md) <br/> |
|Desabilitado  <br/> |Indica se a marca de ação é exibida na janela de desenho.  <br/> |[Célula Disabled (Seção Marcas de Ação)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Determina se a marca de ação é exibida quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.  <br/> |[Célula DisplayMode (Seção Marcas de Ação)](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |O nome da marca de ação que é usada como uma chave para associar a marca de ação a suas ações.  <br/> |[Célula TagName (Seção Marcas de Ação)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |A posição coordenada x nas coordenadas locais da forma, em torno da qual o botão de marca de ação é colocado.  <br/> |[Célula X (Seção Marcas de Ação)](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |O deslocamento x do botão de marca de ação em relação ao ponto definido pelas células X e Y.  <br/> |[Célula X Justify (Seção Marcas de Ação)](x-justify-cell-action-tags-section.md) <br/> |
|Y  <br/> |A posição coordenada y nas coordenadas locais da forma, em torno da qual o botão de marca de ação é colocado.  <br/> |[Célula Y (Seção Marcas de Ação)](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |O deslocamento y do botão de marca de ação em relação ao ponto definido pelas células X e Y.  <br/> |[Célula Y Justify (Seção Marcas de Ação)](y-justify-cell-action-tags-section.md) <br/> |
   

