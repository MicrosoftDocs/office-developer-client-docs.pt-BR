---
title: Elemento de célula (RelCubBezTo linha) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: daa5c527-65fe-a1e4-ab3e-24e77bdb522b
description: Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, as coordenadas x ou y do ponto de controle de início da largura da forma relativa curva e a altura ou as coordenadas x ou y do ponto de controle do final da largura e a altura da forma relativa curva.
ms.openlocfilehash: e4a5353f3ecfb514b61ee893905e54c8951a2be5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771456"
---
# <a name="cell-element-relcubbezto-row-visio-xml"></a>Elemento de célula (RelCubBezTo linha) ('Visio XML')

Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, as coordenadas x ou y do ponto de controle de início da largura da forma relativa curva e a altura ou as coordenadas x ou y do ponto de controle do final da largura e a altura da forma relativa curva.
  
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
|[Elemento de linha (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelCubBezTo_Type](relcubbezto_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, as coordenadas x ou y do ponto de controle de início da largura da forma relativa curva e a altura ou as coordenadas x ou y do ponto de controle do final da largura e a altura da forma relativa curva.  <br/> |
   
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
|X  <br/> |A coordenada x do vértice final de uma curva de Bézier cúbica relativa à largura da forma.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|Y  <br/> |A coordenada y do vértice final de uma curva de Bézier cúbica relativa à altura da forma.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|A  <br/> |A coordenada x do controle de início da curva aponte em relação à largura da forma; um ponto do arco. O ponto de controle é melhor localizado entre o início e fim vértices do arco.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|B  <br/> |A coordenada y do controle de início da curva aponte em relação à altura da forma.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|C  <br/> |A coordenada x do ponto final de controle da curva em relação à largura da forma; um ponto do arco. O ponto de controle é melhor localizado entre os vértices início de ponto de e terminando de controle do arco.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
|D  <br/> |A coordenada y do ponto final de controle da curva em relação à altura da forma.  <br/> |[Linha RelCubBezTo (Seção Geometry)](relcubbezto-row-geometry-section.md) <br/> |
   

