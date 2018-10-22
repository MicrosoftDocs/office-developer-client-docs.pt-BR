---
title: Elemento Cell (Linha RelEllipticalArcTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: Contém as coordenadas x ou y do ponto de extremidade de um arco elíptico relativas à largura e altura da forma, as coordenadas x ou y dos pontos de controle no arco relativas à largura e altura da forma, o ângulo do eixo x para o eixo principal da elipse ou a proporção entre os eixos principal e secundário da elipse.
ms.openlocfilehash: 55e7f664aaab34aa079bafe8f11c57e99fd8a935
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383153"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>Elemento Cell (Linha RelEllipticalArcTo) ('Visio XML')

Contém as coordenadas x ou y do ponto de extremidade de um arco elíptico relativas à largura e altura da forma, as coordenadas x ou y dos pontos de controle no arco relativas à largura e altura da forma, o ângulo do eixo x para o eixo principal da elipse ou a proporção entre os eixos principal e secundário da elipse.
  
## <a name="element-information"></a>Informações do elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do ponto de extremidade de um arco elíptico relativas à largura e altura da forma, as coordenadas x ou y dos pontos de controle no arco relativas à largura e altura da forma, o ângulo do eixo x para o eixo principal da elipse ou a proporção entre os eixos principal e secundário da elipse.  <br/> |
   
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
|X  <br/> |A coordenada x do vértice final de um arco relativa à largura da forma.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|Y  <br/> |A coordenada y do vértice final de um arco relativa à altura da forma.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |A coordenada x do ponto de controle do arco relativa à largura da forma; um ponto no arco.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |A coordenada y do ponto de controle do arco relativa à largura da forma.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |O ângulo do eixo principal do arco em relação ao eixo x de seu pai.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |A proporção entre o eixo principal de um arco e seu eixo secundário.  <br/> |[Linha RelEllipticalArcTo (Seção Geometry)](relellipticalarcto-row-geometry-section.md) <br/> |
   

