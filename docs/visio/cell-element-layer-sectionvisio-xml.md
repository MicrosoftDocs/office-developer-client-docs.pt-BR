---
title: Elemento Cell (Seção Layer) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: Especifica uma propriedade para uma camada ou suas propriedades para uma página.
ms.openlocfilehash: e96fdc1dcd5c9a7a2cb8753beaff766c2b477af2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318169"
---
# <a name="cell-element-layer-section-visio-xml"></a>Elemento Cell (Seção Layer) ('Visio XML')

Especifica uma propriedade para uma camada ou suas propriedades para uma página.
  
## <a name="element-information"></a>Informações do elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |masters.xml, pages.xml  <br/> |
   
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
|[Elemento Row (Seção Layer)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade para uma camada ou suas propriedades para uma página.  <br/> |
   
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
|Ativo  <br/> |Especifica se uma camada está ativa.  <br/> |Nenhum.  <br/> |
|Cor  <br/> |Especifica um destes elementos: o índice de cor na tabela de cores usado para exibir a camada ou um valor RGB que especifica uma cor personalizada que não está na tabela de cores.  <br/> |Nenhum.  <br/> |
|ColorTrans  <br/> |Determina o grau de transparência de uma camada ou cor de texto da forma, de 0 (totalmente opaco) e 1 (totalmente transparente).  <br/> |Nenhum.  <br/> |
|Glue  <br/> |Especifica se as formas pertencentes à camada podem ser coladas.  <br/> |Nenhum.  <br/> |
|Lock  <br/> |Especifica se as formas pertencentes à camada de estão protegidas contra seleção ou edição.  <br/> |Nenhum.  <br/> |
|Name  <br/> |O nome de uma camada.  <br/> |Nenhum.  <br/> |
|NameUniv  <br/> |Especifica o nome universal de uma camada.  <br/> |Nenhum.  <br/> |
|Imprimir  <br/> |Especifica se as formas pertencentes à camada serão impressas quando o desenho for impresso.  <br/> |Nenhum.  <br/> |
|Snap  <br/> |Especifica se outras formas podem ser ajustadas a formas atribuídas à camada.  <br/> |Nenhum.  <br/> |
|Status  <br/> |Especifica se a camada é válida para um documento.  <br/> |Nenhum.  <br/> |
|Visible  <br/> |Especifica se as formas pertencentes à camada ficarão visíveis na página de desenho.  <br/> |Nenhum.  <br/> |
   

