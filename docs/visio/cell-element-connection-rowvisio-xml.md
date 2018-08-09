---
title: Elemento de célula (linha de Conexão) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Contém as coordenadas x ou y, direção horizontal ou vertical ou tipo de um ponto de conexão único em uma forma.
ms.openlocfilehash: 52328e50b185a96ebb06634248b93a4332ac35c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771443"
---
# <a name="cell-element-connection-row-visio-xml"></a>Elemento de célula (linha de Conexão) ('Visio XML')

Contém as coordenadas x ou y, direção horizontal ou vertical ou tipo de um ponto de conexão único em uma forma.
  
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
|[Elemento Row (Seção Connection)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x e y, direção horizontal e vertical e tipo para um ponto de conexão único em uma forma.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Contém as coordenadas x ou y, direção horizontal e vertical e tipo para um ponto de conexão único em uma forma.  <br/> |
   
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
|AutoGen  <br/> |Especifica se o ponto de conexão é gerado automaticamente. Um valor de 1 indica que o ponto de conexão é gerado automaticamente.  <br/> |Nenhum.  <br/> |
|DirX  <br/> |Determina o componente x para o vetor de alinhamento necessário de um ponto de conexão coincidente.  <br/> |[Célula DirX / A (Seção Connection Points)](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Determina o componente de y para o vetor de alinhamento necessário de um ponto de conexão coincidente.  <br/> |[Célula DirY / B (Seção Connection Points)](diryb-cell-connection-points-section.md) <br/> |
|Prompt  <br/> |Este atributo é reservado para uso futuro.  <br/> |Nenhum.  <br/> |
|Tipo  <br/> |Especifica o tipo de ponto de conexão.  <br/> |[Célula Type / C (Seção Connection Points)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Representa a coordenada x de um ponto de conexão em coordenadas locais.  <br/> |[Célula X (Seção Connection Points)](x-cell-connection-points-section.md) <br/> |
|Y  <br/> |Determina a coordenada y de um ponto de conexão em coordenadas locais.  <br/> |[Célula Y (Seção Connection Points)](y-cell-connection-points-section.md) <br/> |
   

