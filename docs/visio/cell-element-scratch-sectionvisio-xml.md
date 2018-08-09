---
title: Elemento de célula (Scratch seção) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af17b1c5-51ee-f46f-79d0-4f33369b66f1
description: Especifica uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.
ms.openlocfilehash: c8917a8d4bcf26789f631238e6a9547e9ca2d59c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771478"
---
# <a name="cell-element-scratch-section-visio-xml"></a>Elemento de célula (Scratch seção) ('Visio XML')

Especifica uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document, masters.xml,. XML de # mestre, pages.xml,. XML n º de página  <br/> |
   
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
|[Elemento Row (Seção Scratch)](row-element-scratch-sectionvisio-xml.md) <br/> |[ScratchRow_Type](scratch_type-complextypevisio-xml.md) <br/> |Especifica uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica uma referência a uma página.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: String  <br/> |opcional  <br/> |Indica que a fórmula é avaliada como um erro. O valor de **f** é o valor atual (uma sequência de mensagem de erro;) o valor do atributo **V** é o último valor válido.  <br/> |Uma cadeia de caracteres de mensagem de erro.  <br/> |
|S  <br/> |XSD: String  <br/> |opcional  <br/> | Representa a fórmula do elemento. Este atributo pode conter uma das cadeias de caracteres seguintes:  <br/>  '(alguns formula)' se a fórmula existe localmente  <br/>  `No Formula`Se a fórmula localmente é excluída ou bloqueada  <br/>  `Inh`Se a fórmula for herdada.  <br/> |Uma fórmula.  <br/> |
|N  <br/> |XSD: String  <br/> |obrigatório  <br/> |Representa o nome da célula ShapeSheet.  <br/> |O nome da célula ShapeSheet.  <br/> Consulte a seção comentários abaixo.  <br/> |
|U  <br/> |XSD: String  <br/> |opcional  <br/> |Representa uma unidade de medida padrão é DL.  <br/> |As unidades da célula.  <br/> |
|V  <br/> |XSD: String  <br/> |opcional  <br/> |Representa o valor da célula.  <br/> |O valor da célula ShapeSheet.  <br/> |
   
### <a name="remarks"></a>Comentários

O atributo **N** deste elemento de **célula** deve ser um conjunto limitado de valores que corresponde às células da ShapeSheet. Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para esse elemento de **célula** . 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|A  <br/> |Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.  <br/> |[Seção Scratch](scratch-section.md) <br/> |
|B  <br/> |Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.  <br/> |[Seção Scratch](scratch-section.md) <br/> |
|C  <br/> |Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.  <br/> |[Seção Scratch](scratch-section.md) <br/> |
|D  <br/> |Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.  <br/> |[Seção Scratch](scratch-section.md) <br/> |
|X  <br/> |Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.  <br/> |[Seção Scratch](scratch-section.md) <br/> |
|Y  <br/> |Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.  <br/> |[Seção Scratch](scratch-section.md) <br/> |
   

