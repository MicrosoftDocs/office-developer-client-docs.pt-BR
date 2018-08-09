---
title: Elemento de célula (linha MoveTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3b2a08f-07a0-5f1c-4910-503229927816
description: Contém as coordenadas x ou y do primeiro vértice de uma forma ou representa as coordenadas x ou y do primeiro vértice depois de uma quebra no caminho.
ms.openlocfilehash: dbcf8d111ab86671fb2aeb073d2a13f40810f941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771454"
---
# <a name="cell-element-moveto-row-visio-xml"></a>Elemento de célula (linha MoveTo) ('Visio XML')

Contém as coordenadas x ou y do primeiro vértice de uma forma ou representa as coordenadas x ou y do primeiro vértice depois de uma quebra no caminho.
  
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
|[Elemento de linha (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[MoveTo_Type](moveto_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y do primeiro vértice de uma forma ou representa as coordenadas x ou y do primeiro vértice depois de uma quebra no caminho.  <br/> |
   
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
|X  <br/> |Se a linha **MoveTo** for a primeira linha na seção, a célula **X** representará a coordenada x do primeiro vértice de uma forma. Se a linha **MoveTo** aparecer entre duas linhas, a célula **X** representará a coordenada x do primeiro vértice depois da quebra no caminho.  <br/> |[Linha MoveTo (Seção Geometry)](moveto-row-geometry-section.md) <br/> |
|Y  <br/> |Se a linha **MoveTo** for a primeira linha na seção, a célula **Y** representará a coordenada y do primeiro vértice de uma forma. Se a linha **MoveTo** aparecer entre duas linhas, a célula **Y** representará a coordenada y do primeiro vértice depois da quebra no caminho.  <br/> |[Linha MoveTo (Seção Geometry)](moveto-row-geometry-section.md) <br/> |
   

