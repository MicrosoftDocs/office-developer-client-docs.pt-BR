---
title: Elemento Cell (Linha Hiperlink) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: Contém as informações de um hiperlink único associado a uma forma. Uma forma conterá uma linha Hiperlink para cada hiperlink.
ms.openlocfilehash: 6644dc70f3d3616e5c20587db4eabaaf773c31d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356060"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Elemento Cell (Linha Hiperlink) ('Visio XML')

Contém as informações de um hiperlink único associado a uma forma. Uma forma conterá uma linha **Hiperlink** para cada hiperlink. 
  
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
|[Elemento Row (Seção Hyperlink)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |Contém as informações de um hiperlink único associado a uma forma. Uma forma conterá uma linha **Hiperlink** para cada hiperlink.  <br/> |
   
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
|Endereço  <br/> |Especifica um endereço de URL, nome do arquivo ou caminho UNC a ser acessado.  <br/> |[Célula Address (Seção Hyperlinks)](address-cell-hyperlinks-section.md) <br/> |
|Padrão  <br/> |Determina o hiperlink padrão de uma forma ou página.  <br/> |[Célula Default (Seção Hyperlinks)](default-cell-hyperlinks-section.md) <br/> |
|Descrição  <br/> |Representa uma cadeia de texto descritiva de um hiperlink.  <br/> |[Célula Description (Seção Hyperlinks)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |Representa uma sequência de caracteres que passa as informações que serão utilizadas para resolver um URL, como as coordenadas de um mapa de imagens.  <br/> |[Célula ExtraInfo (Seção Hyperlinks)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Quadro  <br/> |Representa o nome de um quadro a ser direcionado quando o aplicativo estiver aberto como um documento ativo em um aplicativo contêiner. O padrão é uma cadeia de caracteres vazia.  <br/> |[Célula Frame (Seção Hyperlinks)](frame-cell-hyperlinks-section.md) <br/> |
|Invisible  <br/> |Indica se um hiperlink é exibido no menu de atalho de um forma ou página.  <br/> |[Célula Invisible (Seção Hyperlinks)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |Especifica se o hiperlink será aberto em uma nova janela.  <br/> |[Célula NewWindow (Seção Hyperlinks)](newwindow-cell-hyperlinks-section.md) <br/> |
|SortKey  <br/> |Um número que determina a ordem dos hiperlinks que aparecem no menu de atalho.  <br/> |[Célula SortKey (Seção Hyperlinks)](sortkey-cell-hyperlinks-section.md) <br/> |
|SubAddress  <br/> |Especifica o local no documento de destino para o qual criar o link.  <br/> |[Célula SubAddress (Seção Hyperlinks)](subaddress-cell-hyperlinks-section.md) <br/> |
   

