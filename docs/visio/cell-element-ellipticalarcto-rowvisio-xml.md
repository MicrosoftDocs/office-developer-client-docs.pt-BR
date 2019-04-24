---
title: Elemento Cell (Linha EllipticalArcTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c0aa7a3-cc54-ffac-2c62-917b3d0a357e
description: Contém as coordenadas x ou y do ponto de extremidade de um arco elíptico, as coordenadas x e y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse ou a proporção entre os eixos principal e secundário da elipse.
ms.openlocfilehash: 22dc813108d8f7b5b517c298c40c73ead8d4eec4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356067"
---
# <a name="cell-element-ellipticalarcto-row-visio-xml"></a>Elemento Cell (Linha EllipticalArcTo) ('Visio XML')

Contém as coordenadas x ou y do ponto de extremidade de um arco elíptico, as coordenadas x e y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse ou a proporção entre os eixos principal e secundário da elipse.
  
## <a name="element-information"></a>Informações do elemento

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

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[EllipticalArcTo_Type](ellipticalarcto_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de um arco elíptico, as coordenadas x e y dos pontos de controle no arco, o ângulo do eixo x para o eixo principal da elipse ou a proporção entre os eixos principal e secundário da elipse.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica uma referência a uma página de desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que a fórmula gera um erro. O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.  <br/> |Uma cadeia de caracteres de mensagem de erro.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa a fórmula do elemento. Esse atributo pode conter uma das seguintes cadeias de caracteres:  <br/>  '(alguma fórmula)' se a fórmula existir localmente  <br/>  `No Formula` se a fórmula estiver excluída ou bloqueada localmente  <br/>  `Inh` se a fórmula for herdada.  <br/> |Uma fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |obrigatório  <br/> |Representa o nome da célula ShapeSheet.  <br/> |O nome da célula ShapeSheet.  <br/> Confira a seção Comentários abaixo.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa uma unidade de medida. O padrão é DL.  <br/> |As unidades da célula.  <br/> |
|S  <br/> |xsd:string  <br/> |opcional  <br/> |Representa o valor da célula.  <br/> |O valor da célula ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondam às células ShapeSheet. Consulte a tabela a seguir para determinar os valores do atributo **N** com permissão para este elemento **Cell**. 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|X  <br/> |A coordenada x do vértice final de um arco.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|Y  <br/> |A coordenada y do vértice final de um arco.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |A coordenada x do ponto de controle do arco, um ponto do arco. A melhor localização para o ponto de controle é aproximadamente no meio dos vértices inicial e final do arco. Caso contrário, o tamanho do arco pode ser ampliado de forma exagerada para passar pelo ponto de controle, com resultados imprevisíveis.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |A coordenada y do ponto de controle de um arco.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |O ângulo do eixo principal do arco em relação ao eixo x de sua forma pai.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |A razão entre os eixos principal e secundário de um arco. Apesar do significado comum dessas palavras, o eixo "principal" não precisa ser maior que o eixo "secundário". Logo, a razão não precisa ser maior que 1. Definir esta célula para um valor menor ou igual a 0, ou maior que 1000, pode ocasionar resultados imprevisíveis.  <br/> |[Linha EllipticalArcTo (Seção Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
   

