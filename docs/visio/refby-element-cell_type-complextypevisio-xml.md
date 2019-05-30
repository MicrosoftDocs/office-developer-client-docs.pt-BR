---
title: Elemento RefBy (Cell_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Especifica uma referência a uma página no desenho.
ms.openlocfilehash: cb47919a97b8ad42f62bcb1337cd8e6b3596f5ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538309"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>Elemento RefBy (Cell_Type complexType) (XML do Visio)

Especifica uma referência a uma página no desenho.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Cell (seção Action tag)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define uma propriedade para uma marca de ação em uma forma ou página.  <br/> |
|[Elemento Cell (Linha Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade de uma ação associada a um comando personalizado em um menu de marca de ação ou atalho.  <br/> |
|[Elemento Cell (Linha ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém a coordenada x, a coordenada y ou a curva de um arco circular.  <br/> |
|[Elemento Cell (seção Character)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica um atributo de formatação para o formato de escrita do texto, como fonte, cor, estilo, caso, posição relativa à linha de base ou tamanho de ponto.  <br/> |
|[Elemento Cell (Linha Connection)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y, a direção horizontal ou vertical ou o tipo do ponto de conexão único em uma forma.  <br/> |
|[Elemento Cell (Linha Controls)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém uma propriedade para uma alça de controle específica definida para uma forma.  <br/> |
|[Elemento Cell (Linha Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y de um ponto central de uma elipse e dois pontos na elipse.  <br/> |
|[Elemento Cell (Linha EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de um arco elíptico, as coordenadas x e y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse ou a proporção entre os eixos principal e secundário da elipse.  <br/> |
|[Elemento Cell (seção Field)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Exibe as funções e fórmulas inseridas no texto da forma usando a caixa de diálogo Campo.  <br/> |
|[Elemento Cell (seção Fill Gradient)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de preenchimento.  <br/> |
|[Elemento Cell (seção geometry)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define propriedades que determinam as propriedades de formatação e comportamento em relação a linhas e arcos que compõem a seção Geometry.  <br/> |
|[Elemento Cell (Linha Hyperlink)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as informações de um hiperlink único associado a uma forma. Uma forma conterá uma linha Hyperlink para cada hiperlink.  <br/> |
|[Elemento Cell (Linha InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y de dois pontos em uma linha infinita.  <br/> |
|[Elemento Cell (seção Layer)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade para uma camada ou suas propriedades para uma página.  <br/> |
|[Elemento Cell (seção line Gradient)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém a cor, a transparência ou a posição de uma marca de gradiente para um gradiente de linha.  <br/> |
|[Elemento Cell (Linha LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do vértice final de um segmento de linha reta.  <br/> |
|[Elemento Cell (Linha MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do primeiro vértice de uma forma ou representa as coordenadas x ou y do primeiro vértice depois de uma quebra no caminho.  <br/> |
|[Elemento Cell (Linha NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y, a posição do penúltimo nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura ou a fórmula para uma B-spline não-racional uniforme (NURBS).  <br/> |
|[Elemento Cell (seção Paragraph)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica um atributo de formatação de parágrafo do texto de uma forma, como recuos, espaçamento de linha, marcadores ou alinhamento horizontal de parágrafos.  <br/> |
|[Elemento Cell (Linha PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do último ponto de uma polilinha ou uma fórmula de polilinha.  <br/> |
|[Elemento Cell (Linha RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier cúbica relativa à altura e a largura da forma, as coordenadas x ou y do ponto de controle do início da largura e da altura da forma relativa da curva, ou das coordenadas x ou y do ponto de controle do fim da largura e da altura da forma relativa da curva.  <br/> |
|[Elemento Cell (Linha RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de um arco elíptico relativas à largura e altura da forma, as coordenadas x ou y dos pontos de controle no arco relativas à largura e altura da forma, o ângulo do eixo x para o eixo principal da elipse ou a proporção entre os eixos principal e secundário da elipse.  <br/> |
|[Elemento Cell (linha RelLineTo)](cell-element-rellineto-rowvisio-xml.md) [Célula](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do vértice final de um segmento de linha reta relativa à largura e altura da forma.  <br/> |
|[Elemento Cell (Linha RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do primeiro vértice de uma forma ou as coordenadas x ou y do primeiro vértice depois de uma quebra no caminho, relativas à altura e largura da forma.  <br/> |
|[Elemento Cell (seção RelQuadBezTo](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier quadrática relativa à altura e largura da forma ou as coordenadas x ou y do ponto de controle da largura e altura da forma relativa da curva.  <br/> |
|[Elemento Cell (seção Scratch)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.  <br/> |
|[Elemento Cell (seção Shape data](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade dos dados de forma.  <br/> |
|[Elemento Cell (Linha SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y para o ponto de controle ou o nó de uma spline.  <br/> |
|[Elemento Cell (seção SplineStart](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y para o segundo ponto de controle de uma spline, seus primeiro e segundo nós ou o grau da spline.  <br/> |
|[Elemento Cell (seção tabs)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade que controla a posição ou o alinhamento da parada de tabulação da forma ou do estilo.  <br/> |
|[Elemento Cell (seção User-defined Cells)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Uma propriedade de uma informação especificada pelo usuário que pode ser referenciada por outras células e ferramentas de complemento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Especifica a ID de uma página no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|T  <br/> |xsd:string  <br/> |obrigatório  <br/> |Especifica o tipo de referência.  <br/> |Valores do tipo xsd:string.  <br/> |
   

