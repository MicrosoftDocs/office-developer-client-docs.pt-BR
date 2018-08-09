---
title: Elemento de célula (RelEllipticalArcTo linha) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: Contém ou y coordenadas x do ponto de extremidade do arco elíptico em relação à largura e a altura da forma ou y coordenadas x do controle aponta do arco em relação à largura e a altura, o ângulo do eixo x para o eixo principal da elipse ou taxa entre a forma a eixos principal e secundária da elipse.
ms.openlocfilehash: 661f6971ca4c03c68950ead45065bd12160918d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771477"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>Elemento de célula (RelEllipticalArcTo linha) ('Visio XML')

Contém ou y coordenadas x do ponto de extremidade do arco elíptico em relação à largura e a altura da forma ou y coordenadas x do controle aponta do arco em relação à largura e a altura, o ângulo do eixo x para o eixo principal da elipse ou taxa entre a forma a eixos principal e secundária da elipse.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |# XML do mestre, página # XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento de linha (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |Contém ou y coordenadas x do ponto de extremidade do arco elíptico em relação à largura e a altura da forma ou y coordenadas x do controle aponta do arco em relação à largura e a altura, o ângulo do eixo x para o eixo principal da elipse ou taxa entre a forma a eixos principal e secundária da elipse.  <br/> |
   
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
|X  <br/> |A coordenada x do vértice final em um arco relativa à largura da forma.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|Y  <br/> |A coordenada y do vértice final em um arco em relação a altura da forma.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |A coordenada x do controle do arco aponte em relação à largura da forma; um ponto do arco.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |A coordenada y do controle do arco aponte em relação à largura da forma.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |O ângulo do eixo principal do arco em relação ao eixo x de seu pai.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |A taxa de eixos principal do arco e seu eixo secundário.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
   

