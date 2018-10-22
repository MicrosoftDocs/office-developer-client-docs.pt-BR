---
title: Elemento Cell (Linha RelQuadBezTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b3aea70-a69f-a85e-83d8-c0fa2ee68836
description: Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier quadrática relativa à altura e largura da forma ou as coordenadas x ou y do ponto de controle da largura e altura da forma relativa da curva.
ms.openlocfilehash: 986ed0a5f6e79f13b92f2ede54361916d9681e17
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388669"
---
# <a name="cell-element-relquadbezto-row-visio-xml"></a>Elemento Cell (Linha RelQuadBezTo) ('Visio XML')

Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier quadrática relativa à altura e largura da forma ou as coordenadas x ou y do ponto de controle da largura e altura da forma relativa da curva.
  
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

### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelQuadBezTo_Type](relquadbezto_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de uma curva de Bézier quadrática relativa à altura e largura da forma ou as coordenadas x ou y do ponto de controle da largura e altura da forma relativa da curva.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica uma referência a uma página de desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |opcional  <br/> |Indica que a fórmula gera um erro. O valor de **E** é atual (uma cadeia de mensagem de erro); o valor do atributo **V** é o último valor válido.  <br/> |Uma cadeia de caracteres de mensagem de erro.  <br/> |
|F  <br/> |xsd:string  <br/> |opcional  <br/> | Representa a fórmula do elemento. Esse atributo pode conter uma das seguintes cadeias de caracteres:  <br/>  "(alguma fórmula)" se a fórmula existir localmente  <br/>  `No Formula` se a fórmula for excluída ou bloqueada localmente  <br/>  `Inh` se a fórmula for herdada.  <br/> |Uma fórmula.  <br/> |
|N  <br/> |xsd:string  <br/> |obrigatório  <br/> |Representa o nome da célula ShapeSheet.  <br/> |O nome da célula ShapeSheet.  <br/> Confira a seção Comentários abaixo.  <br/> |
|U  <br/> |xsd:string  <br/> |opcional  <br/> |Representa uma unidade de medida. O padrão é DL.  <br/> |As unidades da célula.  <br/> |
|V  <br/> |xsd:string  <br/> |opcional  <br/> |Representa o valor da célula.  <br/> |O valor da célula ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondem às células ShapeSheet. Confira a tabela a seguir para determinar os valores do atributo **N** permitidos para este elemento **Cell**. 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|X  <br/> |A coordenada x do vértice final de uma curva de Bézier quadrática relativa à largura da forma.  <br/> |[Linha RelQuadBezTo (Seção Geometry)](relquadbezto-row-geometry-section.md) <br/> |
|Y  <br/> |A coordenada y do vértice final de uma curva de Bézier quadrática relativa à altura da forma.  <br/> |[Linha RelQuadBezTo (Seção Geometry)](relquadbezto-row-geometry-section.md) <br/> |
|A  <br/> |A coordenada x do ponto de controle da curva relativa à largura da forma; um ponto do arco. A melhor localização para o ponto de controle é aproximadamente no meio dos vértices inicial e final do arco.  <br/> |[Linha RelQuadBezTo (Seção Geometry)](relquadbezto-row-geometry-section.md) <br/> |
|B  <br/> |A coordenada y do ponto de controle da curva relativa à altura da forma.  <br/> |[Linha RelQuadBezTo (Seção Geometry)](relquadbezto-row-geometry-section.md) <br/> |
   

