---
title: Elemento de célula (seção Geometry) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: Define as propriedades que determinam as propriedades de formatação e comportamentos com relação a linhas e arcos que compõem a seção Geometry.
ms.openlocfilehash: f7ac096206b9197d71691f485a7c5aafc08eb2c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771485"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Elemento de célula (seção Geometry) ('Visio XML')

Define as propriedades que determinam as propriedades de formatação e comportamentos com relação a linhas e arcos que compõem a seção Geometry.
  
## <a name="element-information"></a>Informações de elemento

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
|[Elemento de linha (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |Define as propriedades que determinam as propriedades de formatação e comportamentos com relação a linhas e arcos que compõem a seção Geometry.  <br/> |
   
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
   
## <a name="remarks"></a>Coment�rios

O atributo **N** deste elemento de **célula** deve ser um conjunto limitado de valores que corresponde às células da ShapeSheet. Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para esse elemento de **célula** . 
  
|**Valor**|**Descrição**|**Obter mais informações**|
|:-----|:-----|:-----|
|NoFill  <br/> |Indica se um caminho pode ser preenchido.  <br/> |[Célula NoFill (Seção Geometry)](nofill-cell-geometry-section.md) <br/> |
|NoLine  <br/> |Determina se uma linha será desenhada em torno do limite do caminho.  <br/> |[Célula NoLine (Seção Geometry)](noline-cell-geometry-section.md) <br/> |
|NoQuickDrag  <br/> |Determina se uma forma pode ser selecionada ou arrastada quando o usuário clica na área preenchida definida pela seção Geometry.  <br/> |[Célula NoQuickDrag (seção Geometry)](noquickdrag-cell-geometry-section.md) <br/> |
|NoShow  <br/> |Indica se um caminho será exibido na página de desenho.  <br/> |[Célula NoShow (Seção Geometry)](noshow-cell-geometry-section.md) <br/> |
|NoSnap  <br/> |Determina se outras formas serão ajustadas a um caminho.  <br/> |[Célula NoSnap (Seção Geometry)](nosnap-cell-geometry-section.md) <br/> |
   

