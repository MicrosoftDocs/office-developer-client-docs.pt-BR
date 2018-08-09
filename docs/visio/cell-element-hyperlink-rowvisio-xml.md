---
title: Elemento de célula (linha de hiperlink) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: Contém as informações de um hiperlink único associado a uma forma. Uma forma conterá uma linha Hyperlink para cada hiperlink.
ms.openlocfilehash: b664f5e0ac7cfe27b7198dd59b1b8be1af276db7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771453"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Elemento de célula (linha de hiperlink) ('Visio XML')

Contém as informações de um único hiperlink associado a uma forma. Uma forma conterá uma linha **Hyperlink** para cada hiperlink. 
  
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
|[Elemento Row (Seção Hyperlink)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |Contém as informações de um único hiperlink associado a uma forma. Uma forma conterá uma linha **Hyperlink** para cada hiperlink.  <br/> |
   
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
|Endereço  <br/> |Especifica uma URL, um nome de arquivo ou um caminho UNC para o qual ir.  <br/> |[Célula Address (Seção Hyperlinks)](address-cell-hyperlinks-section.md) <br/> |
|Default  <br/> |Determina o hiperlink padrão para uma forma ou página.  <br/> |[Célula Default (Seção Hyperlinks)](default-cell-hyperlinks-section.md) <br/> |
|Descrição  <br/> |Representa uma cadeia de caracteres de texto descritivo para um hiperlink.  <br/> |[Célula Description (Seção Hyperlinks)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |Representa uma cadeia de caracteres que passa informações a serem usadas na resolução de uma URL, como as coordenadas de um mapa de imagem.  <br/> |[Célula ExtraInfo (Seção Hyperlinks)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Frame  <br/> |Representa o nome de um quadro a ser direcionado quando o aplicativo estiver aberto como um documento ativo em um aplicativo contêiner. O padrão é uma cadeia de caracteres vazia.  <br/> |[Célula Frame (Seção Hyperlinks)](frame-cell-hyperlinks-section.md) <br/> |
|Invisível  <br/> |Indica se um hiperlink será exibido no menu de atalho para uma forma ou página.  <br/> |[Célula Invisible (Seção Hyperlinks)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |Especifica quando abrir o hiperlink em uma nova janela.  <br/> |[Célula NewWindow (Seção Hyperlinks)](newwindow-cell-hyperlinks-section.md) <br/> |
|SortKey  <br/> |Um número que determina a ordem de hiperlinks que aparecem em um menu de atalho.  <br/> |[Célula SortKey (Seção Hyperlinks)](sortkey-cell-hyperlinks-section.md) <br/> |
|Subendereço  <br/> |Especifica uma localidade no documento de destino à qual vincular.  <br/> |[Célula SubAddress (Seção Hyperlinks)](subaddress-cell-hyperlinks-section.md) <br/> |
   

