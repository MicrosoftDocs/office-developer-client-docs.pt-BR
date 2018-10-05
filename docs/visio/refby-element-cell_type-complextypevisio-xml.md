---
title: Elemento RefBy (Cell_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Especifica uma referência a uma página de desenho.
ms.openlocfilehash: 1731bd20a5ba4358c72370dfcdc6d8a6fc791e2f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385855"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>Elemento RefBy (Cell_Type complexType) ('Visio XML')

Especifica uma referência a uma página de desenho.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document, masters.xml,. XML de # mestre, pages.xml,. XML n º de página  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Cell (Seção Action Tag)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define uma propriedade para uma marca de ação em uma forma ou página.  <br/> |
|[Elemento Cell (Linha Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de atalho ou de ação de marca.  <br/> |
|[Elemento Cell (Linha ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém o x coordenada coordenada y ou curva de um arco circular.  <br/> |
|[Elemento Cell (Seção Character)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica um atributo de formatação para sequência de texto de uma forma, como fonte, cor, estilo, caso, posição relativa à linha de base ou o tamanho do ponto.  <br/> |
|[Elemento Cell (Linha Connection)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y, direção horizontal ou vertical ou tipo de um ponto de conexão único em uma forma.  <br/> |
|[Elemento Cell (Linha Controls)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém uma propriedade para uma alça de controle específico definida para uma forma.  <br/> |
|[Elemento Cell (Linha Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto central da elipse e dois pontos na elipse.  <br/> |
|[Elemento Cell (Linha EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém ou y coordenadas x do ponto de extremidade do arco elíptico, pontos de x ou y-coordenadas do controle do arco, o ângulo do eixo x para o eixo principal da elipse ou proporção entre os eixos de principais e secundárias da elipse.  <br/> |
|[Elemento Cell (Seção Field)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Exibe as funções e as fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.  <br/> |
|[Elemento Cell (Seção Fill Gradient)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém a cor, transparência e posição de uma parada de gradiente para um gradiente do preenchimento.  <br/> |
|[Elemento Cell (Seção Geometry)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define as propriedades que determinam as propriedades de formatação e comportamentos com relação a linhas e arcos que compõem a seção Geometry.  <br/> |
|[Elemento Cell (Linha Hyperlink)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as informações de um hiperlink único associado a uma forma. Uma forma conterá uma linha Hyperlink para cada hiperlink.  <br/> |
|[Elemento Cell (Linha InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y de dois pontos em uma linha infinita.  <br/> |
|[Elemento Cell (Seção Layer)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade de uma camada, nem suas propriedades para uma página.  <br/> |
|[Elemento Cell (Seção Line Gradient)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém a cor, transparência ou posição de uma parada de gradiente para um gradiente de linha.  <br/> |
|[Elemento Cell (Linha LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém x- ou coordenadas y do vértice final de um segmento de linha reta.  <br/> |
|[Elemento Cell (Linha MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do primeiro vértice de uma forma ou representa as coordenadas x ou y do primeiro vértice depois de uma quebra no caminho.  <br/> |
|[Elemento Cell (Linha NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém a posição x ou y-coordenadas, do segundo ao último nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura ou a fórmula para uma B-spline racional não-uniforme (NURBS).  <br/> |
|[Elemento Cell (Seção Paragraph)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica um atributo de texto da forma, como recuos, espaçamento de linha, marcadores ou alinhamento horizontal de parágrafos de formatação de parágrafo.  <br/> |
|[Elemento Cell (Linha PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém ou y coordenadas x do último ponto de uma polilinha ou uma fórmula de polilinha.  <br/> |
|[Elemento Cell (Linha RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, as coordenadas x ou y do ponto de controle de início da largura da forma relativa curva e a altura ou as coordenadas x ou y do ponto de controle do final da largura e a altura da forma relativa curva.  <br/> |
|[Elemento Cell (Linha RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém ou y coordenadas x do ponto de extremidade do arco elíptico em relação à largura e a altura da forma ou y coordenadas x do controle aponta do arco em relação à largura e a altura, o ângulo do eixo x para o eixo principal da elipse ou taxa entre a forma a eixos principal e secundária da elipse.  <br/> |
|[Elemento de célula (linha RelLineTo)](cell-element-rellineto-rowvisio-xml.md) [Célula](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém x- ou coordenadas y do vértice final de um segmento de linha reta em relação à largura e altura de uma forma.  <br/> |
|[Elemento Cell (Linha RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do primeiro vértice de uma forma ou as coordenadas x ou y do primeiro vértice depois de uma quebra no caminho, em relação a altura e largura da forma.  <br/> |
|[Elemento de célula (seção de RelQuadBezTo](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier quadrática em relação à largura da forma e a altura ou as coordenadas x ou y do ponto de controle de largura e a altura da forma relativa curva.  <br/> |
|[Elemento Cell (Seção Scratch)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.  <br/> |
|[Elemento de célula (seção Shape Data](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade dos dados da forma.  <br/> |
|[Elemento Cell (Linha SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém ou y coordenadas x do ponto de controle de uma spline ou o nó de uma spline.  <br/> |
|[Elemento de célula (SplineStart seção](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y-especificadas para o segundo ponto de controle de uma spline, seu segundo nó, seu primeiro nó, o último nó ou o grau da spline.  <br/> |
|[Elemento Cell (Seção Tabs)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade que controla o alinhamento ou forma e estilo de parada de tabulação.  <br/> |
|[Elemento Cell (Seção User-defined Cells)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Uma propriedade de uma parte especificada pelo usuário de informações que podem ser referenciadas por outras células e outras ferramentas de complemento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Especifica a identificação de uma página de desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|T  <br/> |XSD: String  <br/> |obrigatório  <br/> |Especifica o tipo de referência.  <br/> |Valores do tipo xsd: String.  <br/> |
   

