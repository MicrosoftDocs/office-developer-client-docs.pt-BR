---
title: Elemento de célula (seção Layer) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: Especifica uma propriedade de uma camada, nem suas propriedades para uma página.
ms.openlocfilehash: 92be29321ba637bb694c0cf5d3cddcb888618c1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771482"
---
# <a name="cell-element-layer-section-visio-xml"></a>Elemento de célula (seção Layer) ('Visio XML')

Especifica uma propriedade de uma camada, nem suas propriedades para uma página.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Masters.XML, pages.xml  <br/> |
   
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
|[Elemento Row (Seção Layer)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade de uma camada, nem suas propriedades para uma página.  <br/> |
   
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
|Ativo  <br/> |Especifica se uma camada está ativa.  <br/> |Nenhum.  <br/> |
|Cor  <br/> |Especifica um dos seguintes: O índice da cor na tabela de cores usado para exibir a camada ou um valor RGB especificando uma cor personalizada não na tabela de cores.  <br/> |Nenhum.  <br/> |
|ColorTrans  <br/> |Determina o grau de transparência para uma camada ou a cor do texto da forma, de 0 (completamente opaco) até 1 (completamente transparente).  <br/> |Nenhum.  <br/> |
|Cola  <br/> |Especifica se as formas pertencentes à camada podem ser coladas.  <br/> |Nenhum.  <br/> |
|Lock  <br/> |Especifica se as formas pertencentes à camada estão protegidas contra seleção ou edição.  <br/> |Nenhum.  <br/> |
|Nome  <br/> |O nome de uma camada.  <br/> |Nenhum.  <br/> |
|NameUniv  <br/> |Especifica o nome universal de uma camada.  <br/> |Nenhum.  <br/> |
|Imprimir  <br/> |Especifica se as formas pertencentes à camada serão impressas quando o desenho é impresso.  <br/> |Nenhum.  <br/> |
|Ajustar  <br/> |Especifica se outras formas podem ser ajustadas a formas atribuídas à camada.  <br/> |Nenhum.  <br/> |
|Status  <br/> |Especifica se a camada é uma camada válida para um documento.  <br/> |Nenhum.  <br/> |
|Visible  <br/> |Especifica se as formas pertencentes à camada serão visíveis na página de desenho.  <br/> |Nenhum.  <br/> |
   

