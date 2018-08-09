---
title: Elemento de célula (controles de linha) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Contém uma propriedade para uma alça de controle específico definida para uma forma.
ms.openlocfilehash: ff9bd2111b0f5a6544638fb7b33a1a9b797ede7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771455"
---
# <a name="cell-element-controls-row-visio-xml"></a>Elemento de célula (controles de linha) ('Visio XML')

Contém uma propriedade para uma alça de controle específico definida para uma forma.
  
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
|[Elemento Row (Seção Controls)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Contém uma propriedade para uma alça de controle específico definida para uma forma.  <br/> |
   
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
|CanGlue  <br/> |Determina se é possível associar uma alça de controle a outras formas.  <br/> |[Célula Can Glue (Seção Controls)](can-glue-cell-controls-section.md) <br/> |
|Prompt  <br/> |Representa uma sequência de texto descritiva exibida como uma Dica de Ferramenta quando o usuário pausa o ponteiro sobre a alça de controle de uma forma.  <br/> |[Célula Tip (Seção Controls)](tip-cell-controls-section.md) <br/> |
|X  <br/> |Representa a coordenada x que indica a localização da alça de controle da forma em coordenadas locais.  <br/> |[Célula X (Seção Controls)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Especifica o tipo de comportamento que a coordenada x da alça de controle exibe depois da alça ser movida.  <br/> |Nenhum.  <br/> |
|xDyn  <br/> |Representa a coordenada x do ponto de ancoragem de uma alça de controle em coordenadas locais.  <br/> |[Célula X Dynamics (Seção Controls)](x-dynamics-cell-controls-section.md) <br/> |
|Y  <br/> |Representa a coordenada y que indica a localização da alça de controle da forma em coordenadas locais.  <br/> |[Célula Y (Seção Controls)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Especifica o tipo de comportamento que a coordenada y da alça de controle irá exibir depois da alça ser movida.  <br/> |Nenhum.  <br/> |
|YDyn  <br/> |Representa a coordenada y do ponto de ancoragem de uma alça de controle em coordenadas locais.  <br/> |[Célula Y Dynamics (Seção Controls)](y-dynamics-cell-controls-section.md) <br/> |
   

