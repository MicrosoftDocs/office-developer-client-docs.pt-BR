---
title: Elemento Cell (Linha Ellipse) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 210e6731-7c94-90b1-c7c4-635df974fdb6
description: Contém as coordenadas x ou y de um ponto central de uma elipse e dois pontos na elipse.
ms.openlocfilehash: 75c3cf86b7c8668b70915117e1fc70b07d2cef0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356116"
---
# <a name="cell-element-ellipse-row-visio-xml"></a>Elemento Cell (Linha Ellipse) ('Visio XML')

Contém as coordenadas x ou y de um ponto central de uma elipse e dois pontos na elipse.
  
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
|[Elemento Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Ellipse_Type](ellipse_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y de um ponto central de uma elipse e dois pontos na elipse.  <br/> |
   
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
|X  <br/> |A coordenada x do ponto central.  <br/> |[Linha Ellipse (Seção Geometry)](ellipse-row-geometry-section.md) <br/> |
|Y  <br/> |A coordenada y do ponto central.  <br/> |[Linha Ellipse (Seção Geometry)](ellipse-row-geometry-section.md) <br/> |
|A  <br/> |Uma coordenada x do primeiro ponto na elipse, juntamente com uma coordenada y representada pela célula B.  <br/> |[Linha Ellipse (Seção Geometry)](ellipse-row-geometry-section.md) <br/> |
|B  <br/> |Uma coordenada y do primeiro ponto na elipse, juntamente com uma coordenada x representada pela célula A.  <br/> |[Linha Ellipse (Seção Geometry)](ellipse-row-geometry-section.md) <br/> |
|C  <br/> |Uma coordenada x do segundo ponto na elipse, juntamente com uma coordenada y representada pela célula D.  <br/> |[Linha Ellipse (Seção Geometry)](ellipse-row-geometry-section.md) <br/> |
|D  <br/> |Uma coordenada y do segundo ponto na elipse, juntamente com uma coordenada y representada pela célula C.  <br/> |[Linha Ellipse (Seção Geometry)](ellipse-row-geometry-section.md) <br/> |
   

