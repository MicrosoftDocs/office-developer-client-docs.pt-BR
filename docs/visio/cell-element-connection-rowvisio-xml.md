---
title: Elemento Cell (Linha Connection) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Contém as coordenadas x ou y, a direção horizontal ou vertical ou o tipo do ponto de conexão único em uma forma.
ms.openlocfilehash: 367d7e462c1eb5b8fa6ee0572346f45ad621fa15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356102"
---
# <a name="cell-element-connection-row-visio-xml"></a>Elemento Cell (Linha Connection) ('Visio XML')

Contém as coordenadas x ou y, a direção horizontal ou vertical ou o tipo do ponto de conexão único em uma forma.
  
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
|[Elemento Row (Seção Connection)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x e y, a direção horizontal e vertical e o tipo do ponto de conexão único em uma forma.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y, a direção horizontal e vertical e o tipo do ponto de conexão único em uma forma.  <br/> |
   
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
|AutoGen  <br/> |Especifica se o ponto de conexão é gerado automaticamente. O valor 1 indica que o ponto de conexão é gerado automaticamente.  <br/> |Nenhum.  <br/> |
|DirX  <br/> |Determina o componente x do vetor de alinhamento obrigatório de um ponto de conexão correspondente.  <br/> |[Célula DirX/A (Seção Connection Points)](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Determina o componente y do vetor de alinhamento obrigatório de um ponto de conexão correspondente.  <br/> |[Célula DirY/B (Seção Connection Points)](diryb-cell-connection-points-section.md) <br/> |
|Aviso  <br/> |Esse atributo é reservado para uso futuro.  <br/> |Nenhum.  <br/> |
|Tipo  <br/> |Determina o tipo de ponto de conexão.  <br/> |[Célula Type/C (Seção Connection Points)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Representa a coordenada x de um ponto de conexão em coordenadas locais.  <br/> |[Célula X Cell (Seção Connection Points)](x-cell-connection-points-section.md) <br/> |
|Y  <br/> |Determina a coordenada y de um ponto de conexão em coordenadas locais.  <br/> |[Célula Y (Seção Connection Points)](y-cell-connection-points-section.md) <br/> |
   

