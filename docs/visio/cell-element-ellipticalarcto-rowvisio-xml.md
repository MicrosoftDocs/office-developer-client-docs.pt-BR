---
title: Elemento de célula (linha EllipticalArcTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c0aa7a3-cc54-ffac-2c62-917b3d0a357e
description: Contém ou y coordenadas x do ponto de extremidade do arco elíptico, pontos de x ou y-coordenadas do controle do arco, o ângulo do eixo x para o eixo principal da elipse ou proporção entre os eixos de principais e secundárias da elipse.
ms.openlocfilehash: 01d28fae5943251b61d0d26211ee91f09f25b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771458"
---
# <a name="cell-element-ellipticalarcto-row-visio-xml"></a>Elemento de célula (linha EllipticalArcTo) ('Visio XML')

Contém ou y coordenadas x do ponto de extremidade do arco elíptico, pontos de x ou y-coordenadas do controle do arco, o ângulo do eixo x para o eixo principal da elipse ou proporção entre os eixos de principais e secundárias da elipse.
  
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
|[Elemento de linha (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[EllipticalArcTo_Type](ellipticalarcto_type-complextypevisio-xml.md) <br/> |Contém ou y coordenadas x do ponto de extremidade do arco elíptico, pontos de x ou y-coordenadas do controle do arco, o ângulo do eixo x para o eixo principal da elipse ou proporção entre os eixos de principais e secundárias da elipse.  <br/> |
   
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
|X  <br/> |A coordenada x do vértice final em um arco.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|Y  <br/> |A coordenada y do vértice final em um arco.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |A coordenada x do ponto de controle do arco, um ponto do arco. A melhor localização para o ponto de controle é aproximadamente no meio dos vértices inicial e final do arco. Caso contrário, o tamanho do arco pode ser ampliado de forma exagerada para passar pelo ponto de controle, com resultados imprevisíveis.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |A coordenada y de um ponto de controle do arco.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |O ângulo do eixo de principal do arco em relação ao eixo x da forma pai.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
   

