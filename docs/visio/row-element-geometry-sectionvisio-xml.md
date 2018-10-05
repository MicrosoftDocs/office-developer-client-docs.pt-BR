---
title: Elemento de linha (seção Geometry) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Contém linhas que listam as coordenadas dos vértices de linhas e arcos que compõem a forma.
ms.openlocfilehash: 53482b0db3f2deb3c8e2ba30f41be67f0d9e27a0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400086"
---
# <a name="row-element-geometry-section-visio-xml"></a>Elemento de linha (seção Geometry) ('Visio XML')

Contém linhas que listam as coordenadas dos vértices de linhas e arcos que compõem a forma.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |# XML do mestre, página # XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Seção](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contém linhas que listam as coordenadas dos vértices de linhas e arcos que compõem a forma.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

> [!NOTE]
> O elemento de célula é o único filho deste elemento. Dependendo do atributo "T" deste elemento, o significado dos elementos de célula são diferentes. Na tabela a seguir, o texto parathetical no nome do elemento corresponde ao valor "T" ao qual o tópico se aplica. 
  
|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Cell (Linha ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y e um arco de uma curva circular.  <br/> |
|[Elemento Cell (Linha Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y de um ponto central de uma elipse e dois pontos na elipse.  <br/> |
|[Elemento Cell (Linha EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do ponto de extremidade de um arco elíptico, as coordenadas x e y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse e a razão entre os eixos principal e secundário da elipse.  <br/> |
|[Elemento Cell (Linha InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y de dois pontos em uma linha infinita  <br/> |
|[Elemento Cell (Linha LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do vértice final de um segmento de linha reta.  <br/> |
|[Elemento Cell (Linha MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do primeiro vértice de uma forma ou representa as coordenadas x e y do primeiro vértice depois de uma quebra no caminho.  <br/> |
|[Elemento Cell (Linha NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y, a posição do penúltimo nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura e a fórmula para uma B-spline não-racional uniforme (NURBS).  <br/> |
|[Elemento Cell (Linha PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do último ponto de uma polilinha e uma fórmula de polilinha.  <br/> |
|[Elemento Cell (Linha RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, as coordenadas x e y do ponto de controle de início da largura da forma relativa curva e a altura e as coordenadas x e y do controle ponto do final da largura e a altura da forma relativa curva.  <br/> |
|[Elemento Cell (Linha RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier quadrática em relação à largura da forma e a altura e as coordenadas x e y do ponto de controle de largura e a altura da forma relativa curva.  <br/> |
|[Elemento Cell (Linha RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y-do ponto de extremidade do arco elíptico em relação à largura da forma e a altura, coordenadas x e y-dos pontos de controle do arco em relação à largura da forma e altura, o ângulo do eixo x para o eixo de principal da elipse e a razão entre eixos principal e secundária da elipse.  <br/> |
|[Elemento Cell (Linha RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém x-coordenadas e y do vértice final de um segmento de linha reta em relação à largura e altura de uma forma.  <br/> |
|[Elemento Cell (Linha RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do primeiro vértice de uma forma ou as coordenadas x e y do primeiro vértice depois de uma quebra no caminho, em relação a altura e largura da forma.  <br/> |
|[Elemento Cell (Linha RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier quadrática em relação à largura da forma e a altura e as coordenadas x e y do ponto de controle de largura e a altura da forma relativa curva.  <br/> |
|[Elemento Cell (Linha SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y para o ponto de controle e o nó de uma spline.  <br/> |
|[Elemento Cell (Linha SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contém as coordenadas x e y para o segundo ponto de controle de uma spline, seus primeiro e segundo nós e o grau da spline.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica se uma linha que seria contrário herdada de uma forma mestra foi excluída.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica o identificador baseada em um para a linha. Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX é usado somente para as seções de caractere, Conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, zero e guias. Uma linha só pode ter um dos atributos IX ou N.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica o nome exclusivo do dependentes de idioma da linha.  <br/> |Valores do tipo xsd: String.  <br/> |
|N  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica o nome exclusivo do independente do idioma da linha. O atributo N é usado somente para as seções do usuário, propriedade, ações, controle, Conexão, hiperlink e ActionTag. Uma linha só pode ter um dos atributos IX ou N.  <br/> |Valores do tipo xsd: String.  <br/> |
|T  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica o tipo do caminho geométrico representado por linha e usada na visualização de geometria. O atributo T é usado apenas para a seção Geometry.  <br/> |Valores do tipo xsd: String.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **T** deste elemento de **linha** deve ser um conjunto limitado de valores que correspondem às linhas do ShapeSheet. Consulte a tabela abaixo para determinar os valores do atributo **T** que são permitidos para esse elemento de **linha** . 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Contém as coordenadas x e y e um arco de uma curva circular.  <br/> |[Linha ArcTo (Seção Geometry)](arcto-row-geometry-section.md) <br/> |
|Elipse  <br/> |Contém as coordenadas x e y de um ponto central de uma elipse e dois pontos na elipse.  <br/> |[Linha Ellipse (Seção Geometry)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Contém as coordenadas x e y do ponto de extremidade de um arco elíptico, as coordenadas x e y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse e a razão entre os eixos principal e secundário da elipse.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Contém as coordenadas x e y de dois pontos em uma linha infinita  <br/> |[Linha InfiniteLine (Seção Geometry)](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Contém as coordenadas x e y do vértice final de um segmento de linha reta.  <br/> |[Linha LineTo (Seção Geometry)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Contém as coordenadas x e y do primeiro vértice de uma forma ou representa as coordenadas x e y do primeiro vértice depois de uma quebra no caminho.  <br/> |[Linha MoveTo (Seção Geometry)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Contém as coordenadas x e y, a posição do penúltimo nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura e a fórmula para uma B-spline não-racional uniforme (NURBS).  <br/> |[Linha NURBSTo (Seção Geometry)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Contém as coordenadas x e y do último ponto de uma polilinha e uma fórmula de polilinha.  <br/> |[Linha PolylineTo (Seção Geometry)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, as coordenadas x e y do ponto de controle de início da largura da forma relativa curva e a altura e as coordenadas x e y do controle ponto do final da largura e a altura da forma relativa curva.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Contém as coordenadas x e y-do ponto de extremidade do arco elíptico em relação à largura da forma e a altura, coordenadas x e y-dos pontos de controle do arco em relação à largura da forma e altura, o ângulo do eixo x para o eixo de principal da elipse e a razão entre eixos principal e secundária da elipse.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Contém x-coordenadas e y do vértice final de um segmento de linha reta em relação à largura e altura de uma forma.  <br/> |[Linha RelLineTo (Seção Geometry)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Contém as coordenadas x e y do primeiro vértice de uma forma ou as coordenadas x e y do primeiro vértice depois de uma quebra no caminho, em relação a altura e largura da forma.  <br/> |[Linha RelMoveTo (Seção Geometry)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier quadrática em relação à largura da forma e a altura e as coordenadas x e y do ponto de controle de largura e a altura da forma relativa curva.  <br/> |[Linha RelQuadBezTo (Seção Geometry)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Contém as coordenadas x e y para o ponto de controle e o nó de uma spline.  <br/> |[Linha SplineKnot (Seção Geometry)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Contém as coordenadas x e y para o segundo ponto de controle de uma spline, seus primeiro e segundo nós e o grau da spline.  <br/> |[Linha SplineStart (Seção Geometry)](splinestart-row-geometry-section.md) <br/> |
   

