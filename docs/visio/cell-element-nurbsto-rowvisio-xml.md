---
title: Elemento de célula (linha NURBSTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e76bae8f-b9de-39ef-1f56-b00a6cd2ba6c
description: Contém a posição x ou y-coordenadas, do segundo ao último nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura ou a fórmula para uma B-spline racional não-uniforme (NURBS).
ms.openlocfilehash: acdc61235fde88a0f5b03eb6e83f54092b4f1fd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771468"
---
# <a name="cell-element-nurbsto-row-visio-xml"></a>Elemento de célula (linha NURBSTo) ('Visio XML')

Contém a posição x ou y-coordenadas, do segundo ao último nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura ou a fórmula para uma B-spline racional não-uniforme (NURBS).
  
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
|[Elemento de linha (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[NURBSTo_Type](nurbsto_type-complextypevisio-xml.md) <br/> |Contém a posição x ou y-coordenadas, do segundo ao último nó, a posição da última espessura, a posição do primeiro nó, a posição da primeira espessura ou a fórmula para uma B-spline racional não-uniforme (NURBS).  <br/> |
   
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
|X  <br/> |A coordenada xdo último ponto de controle de uma NURBS.  <br/> |[Linha NURBSTo (Seção Geometry)](nurbsto-row-geometry-section.md) <br/> |
|Y  <br/> |A coordenada ydo último ponto de controle de uma NURBS.  <br/> |[Linha NURBSTo (Seção Geometry)](nurbsto-row-geometry-section.md) <br/> |
|A  <br/> |O penúltimo nó de uma NURBS.  <br/> |[Linha NURBSTo (Seção Geometry)](nurbsto-row-geometry-section.md) <br/> |
|B  <br/> |A última espessura de uma NURBS.  <br/> |[Linha NURBSTo (Seção Geometry)](nurbsto-row-geometry-section.md) <br/> |
|C  <br/> |O primeiro nó de uma NURBS.  <br/> |[Linha NURBSTo (Seção Geometry)](nurbsto-row-geometry-section.md) <br/> |
|D  <br/> |A primeira espessura de uma NURBS.  <br/> |[Linha NURBSTo (Seção Geometry)](nurbsto-row-geometry-section.md) <br/> |
|E  <br/> |Uma fórmula NURBS.  <br/> |[Linha NURBSTo (Seção Geometry)](nurbsto-row-geometry-section.md) <br/> |
   

