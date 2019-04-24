---
title: Elemento Row (seção geometry) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Contém linhas que listam as coordenadas das vértices para as linhas e arcos que compõem a forma.
ms.openlocfilehash: 53482b0db3f2deb3c8e2ba30f41be67f0d9e27a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358546"
---
# <a name="row-element-geometry-section-visio-xml"></a>Elemento Row (seção geometry) (' Visio XML ')

Contém linhas que listam as coordenadas das vértices para as linhas e arcos que compõem a forma.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contém linhas que listam as coordenadas das vértices para as linhas e arcos que compõem a forma.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

> [!NOTE]
> O elemento Cell é o único filho desse elemento. Dependendo do atributo "T" desse elemento, o significado dos elementos da célula são diferentes. Na tabela abaixo, o texto parathetical no nome do elemento corresponde ao valor "T" ao qual o tópico se aplica. 
  
|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Cell (Linha ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y ou a curva de um arco circular.  <br/> |
|[Elemento Cell (Linha Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y de um ponto central de uma elipse e dois pontos na elipse.  <br/> |
|[Elemento Cell (Linha EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do ponto de extremidade de um arco elíptico, as coordenadas x e y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse e a razão entre os eixos principal e secundário da elipse.  <br/> |
|[Elemento Cell (Linha InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y de dois pontos em uma linha infinita  <br/> |
|[Elemento Cell (Linha LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do vértice final de um segmento de linha reta.  <br/> |
|[Elemento Cell (Linha MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do primeiro vértice de uma forma ou representa as coordenadas x e y do primeiro vértice depois de uma quebra no caminho.  <br/> |
|[Elemento Cell (Linha NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y, a posição do penúltimo nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura e a fórmula para uma B-spline não-racional uniforme (NURBS).  <br/> |
|[Elemento Cell (Linha PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do último ponto de uma polilinha e uma fórmula de polilinha.  <br/> |
|[Elemento Cell (Linha RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva Bézier cúbica em relação à largura e altura da forma, as coordenadas x e y do ponto de controle do início da largura e altura de uma forma relativa de curva e as coordenadas x e y do controle ponto do final da largura e altura da forma relativa da curva.  <br/> |
|[Elemento Cell (Linha RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier quadrática em relação à largura e altura da forma e às coordenadas x e y do ponto de controle da largura e altura da forma relativa da curva.  <br/> |
|[Elemento Cell (Linha RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do ponto de extremidade de um arco elíptico em relação à largura e altura da forma, coordenadas x e y dos pontos de controle no arco em relação à largura e altura da forma, ângulo do eixo x para o eixo principal da elipse e proporção entre eixos principais e secundários da elipse.  <br/> |
|[Elemento Cell (Linha RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do vértice final de um segmento de linha reta em relação à largura e à altura de uma forma.  <br/> |
|[Elemento Cell (Linha RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do primeiro vértice de uma forma ou as coordenadas x e y do primeiro vértice depois de uma quebra em um caminho, em relação à altura e à largura da forma.  <br/> |
|[Elemento Cell (Linha RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier quadrática em relação à largura e altura da forma e às coordenadas x e y do ponto de controle da largura e altura da forma relativa da curva.  <br/> |
|[Elemento Cell (Linha SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y para o ponto de controle e o nó de uma spline.  <br/> |
|[Elemento Cell (Linha SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y para o segundo ponto de controle de uma spline, seus primeiro e segundo nós e o grau da spline.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se uma linha que seria herdada de uma forma mestra foi excluída.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica o identificador baseado em um da linha. Ele deve ser unqiue e maior que outros identificadores na mesma seção. O atributo IX é usado somente para as seções caractere, conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, rabisco e guias. Uma linha pode ter apenas um dos atributos IX ou N.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o nome exclusivo dependente de idioma da linha.  <br/> |Valores do tipo xsd:string.  <br/> |
|N  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o nome exclusivo independente do idioma da linha. O atributo N é usado apenas para as seções usuário, propriedade, ações, controle, conexão, hiperlink e ActionTag. Uma linha pode ter apenas um dos atributos IX ou N.  <br/> |Valores do tipo xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o tipo de caminho geométrico representado pela linha e usado na visualização de geometria. O atributo T é usado apenas para a seção Geometry.  <br/> |Valores do tipo xsd:string.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **T** desse elemento **Row** deve ser um de um conjunto limitado de valores que correspondem às linhas do ShapeSheet. Consulte a tabela abaixo para determinar os valores do atributo **T** que são permitidos para este elemento **Row** . 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Contém as coordenadas x e y ou a curva de um arco circular.  <br/> |[Linha ArcTo (Seção Geometry)](arcto-row-geometry-section.md) <br/> |
|Elipse  <br/> |Contém as coordenadas x e y de um ponto central de uma elipse e dois pontos na elipse.  <br/> |[Linha Ellipse (Seção Geometry)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Contém as coordenadas x e y do ponto de extremidade de um arco elíptico, as coordenadas x e y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse e a razão entre os eixos principal e secundário da elipse.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Contém as coordenadas x e y de dois pontos em uma linha infinita  <br/> |[Linha InfiniteLine (Seção Geometry)](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Contém as coordenadas x e y do vértice final de um segmento de linha reta.  <br/> |[Linha LineTo (Seção Geometry)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Contém as coordenadas x e y do primeiro vértice de uma forma ou representa as coordenadas x e y do primeiro vértice depois de uma quebra no caminho.  <br/> |[Linha MoveTo (Seção Geometry)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Contém as coordenadas x e y, a posição do penúltimo nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura e a fórmula para uma B-spline não-racional uniforme (NURBS).  <br/> |[Linha NURBSTo (Seção Geometry)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Contém as coordenadas x e y do último ponto de uma polilinha e uma fórmula de polilinha.  <br/> |[Linha PolylineTo (Seção Geometry)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva Bézier cúbica em relação à largura e altura da forma, as coordenadas x e y do ponto de controle do início da largura e altura de uma forma relativa de curva e as coordenadas x e y do controle ponto do final da largura e altura da forma relativa da curva.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Contém as coordenadas x e y do ponto de extremidade de um arco elíptico em relação à largura e altura da forma, coordenadas x e y dos pontos de controle no arco em relação à largura e altura da forma, ângulo do eixo x para o eixo principal da elipse e proporção entre eixos principais e secundários da elipse.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Contém as coordenadas x e y do vértice final de um segmento de linha reta em relação à largura e à altura de uma forma.  <br/> |[Linha RelLineTo (Seção Geometry)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Contém as coordenadas x e y do primeiro vértice de uma forma ou as coordenadas x e y do primeiro vértice depois de uma quebra em um caminho, em relação à altura e à largura da forma.  <br/> |[Linha RelMoveTo (Seção Geometry)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier quadrática em relação à largura e altura da forma e às coordenadas x e y do ponto de controle da largura e altura da forma relativa da curva.  <br/> |[Linha RelQuadBezTo (Seção Geometry)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Contém as coordenadas x e y para o ponto de controle e o nó de uma spline.  <br/> |[Linha SplineKnot (Seção Geometry)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Contém as coordenadas x e y para o segundo ponto de controle de uma spline, seus primeiro e segundo nós e o grau da spline.  <br/> |[Linha SplineStart (Seção Geometry)](splinestart-row-geometry-section.md) <br/> |
   

