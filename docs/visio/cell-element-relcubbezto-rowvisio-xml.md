---
title: Elemento Cell (Linha RelCubBezTo) ("XML do Visio")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: daa5c527-65fe-a1e4-ab3e-24e77bdb522b
description: Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier cúbica relativa à altura e a largura da forma, as coordenadas x ou y do ponto de controle do início da largura e da altura da forma relativa da curva, ou das coordenadas x ou y do ponto de controle do fim da largura e da altura da forma relativa da curva.
ms.openlocfilehash: 15cfbbfd9b773169e338d7d364540582229a4ac7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398609"
---
# <a name="cell-element-relcubbezto-row-visio-xml"></a>Elemento Cell (Linha RelCubBezTo) ("XML do Visio")

Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier cúbica relativa à altura e a largura da forma, as coordenadas x ou y do ponto de controle do início da largura e da altura da forma relativa da curva, ou das coordenadas x ou y do ponto de controle do fim da largura e da altura da forma relativa da curva.
  
## <a name="element-information"></a>Elemento de informações

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

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** e **choice**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelCubBezTo_Type](relcubbezto_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier cúbica relativa à altura e a largura da forma, as coordenadas x ou y do ponto de controle do início da largura e da altura da forma relativa da curva, ou das coordenadas x ou y do ponto de controle do fim da largura e da altura da forma relativa da curva.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica uma referência a uma página de desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que a fórmula gera um erro. O valor de **E** é o atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.  <br/> |Uma cadeia de caracteres de mensagem de erro.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa a fórmula do elemento. Esse atributo pode conter uma das seguintes cadeias de caracteres:  <br/>  '(alguma fórmula)' se a fórmula existir localmente  <br/>  `No Formula` se a fórmula estiver excluída ou bloqueada localmente  <br/>  `Inh` se a fórmula for herdada.  <br/> |Uma fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |obrigatório  <br/> |Representa o nome da célula ShapeSheet.  <br/> |O nome da célula ShapeSheet.  <br/> Confira a seção Comentários abaixo.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa uma unidade de medida. O padrão é DL.  <br/> |As unidades da célula.  <br/> |
|V  <br/> |xsd:string  <br/> |opcional  <br/> |Representa o valor da célula.  <br/> |O valor da célula ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet. Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**. 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|X  <br/> |A coordenada x do vértice final de uma curva de Bézier cúbica relativa à largura da forma.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|Y  <br/> |A coordenada y do vértice final de uma curva de Bézier cúbica relativa à altura da forma.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|A  <br/> |Aponte a coordenada x do ponto de controle do início de curva em relação à largura da forma; um ponto do arco. O ponto de controle fica melhor localizado entre os vértices de início e fim do arco.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|B  <br/> |A coordenada y do ponto de controle de início de uma curva em relação à altura da forma.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|C  <br/> |A coordenada x do ponto de controle final da curva relativa à largura da forma; um ponto do arco. O ponto de controle fica melhor localizado entre o ponto de controle de início e os vértices de fim do arco.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|D  <br/> |A coordenada y do ponto de controle final de uma curva relativo à altura da forma.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
   

