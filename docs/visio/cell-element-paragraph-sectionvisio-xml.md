---
title: Elemento de célula (seção Paragraph) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: Especifica um atributo de texto da forma, como recuos, espaçamento de linha, marcadores ou alinhamento horizontal de parágrafos de formatação de parágrafo.
ms.openlocfilehash: 38309d3d1158b02084af6686c483547b28b8995f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771464"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Elemento de célula (seção Paragraph) ('Visio XML')

Especifica um atributo de texto da forma, como recuos, espaçamento de linha, marcadores ou alinhamento horizontal de parágrafos de formatação de parágrafo.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document,. XML de n º de mestre, página # XML  <br/> |
   
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
|[Elemento Row (Seção Paragraph)](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |Especifica um atributo de texto da forma, como recuos, espaçamento de linha, marcadores ou alinhamento horizontal de parágrafos de formatação de parágrafo.  <br/> |
   
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
|Bullet  <br/> |Determina o estilo com marcadores.  <br/> |[Célula Bullet (seção Paragraph)](bullet-cell-paragraph-section.md) <br/> |
|BulletFont  <br/> |Representa o número da fonte usada para formatar o texto quando uma sequência de caracteres com marcadores personalizada for especificada e o valor da célula Bullet for diferente de zero.  <br/> |[Célula BulletFont (Seção Paragraph)](bulletfont-cell-paragraph-section.md) <br/> |
|BulletFontSize  <br/> |Especifica o tamanho de um marcador.  <br/> |[Célula BulletSize (Seção Paragraph)](bulletsize-cell-paragraph-section.md) <br/> |
|BulletStr  <br/> |Permite criar um estilo com marcadores personalizados.  <br/> |[Célula BulletString (Seção Paragraph)](bulletstring-cell-paragraph-section.md) <br/> |
|Sinalizadores  <br/> |Indica a direção do texto: da esquerda para a direita ou vice-versa.  <br/> |[Célula Flags (Seção Paragraph)](flags-cell-paragraph-section.md) <br/> |
|HorzAlign  <br/> |Determina o alinhamento horizontal do texto no bloco de texto da forma.  <br/> |[Célula HAlign (Seção Paragraph)](halign-cell-paragraph-section.md) <br/> |
|IndFirst  <br/> |Representa a distância do recuo da primeira linha de cada parágrafo no bloco de texto da forma em relação ao recuo esquerdo do parágrafo. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo da primeira linha será o mesmo.  <br/> |[Célula IndFirst (Seção Paragraph)](indfirst-cell-paragraph-section.md) <br/> |
|IndLeft  <br/> |Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem esquerda do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo esquerdo será o mesmo.  <br/> |[Célula IndLeft (Seção Paragraph)](indleft-cell-paragraph-section.md) <br/> |
|IndRight  <br/> |Representa a distância do recuo de todas as linhas do texto em um parágrafo em relação à margem direita do bloco de texto. Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o recuo direito será o mesmo.  <br/> |[Célula IndRight (Seção Paragraph)](indright-cell-paragraph-section.md) <br/> |
|SpAfter  <br/> |Determina a quantidade de espaço inserido depois de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o último parágrafo em um bloco de texto, da célula BottomMargin.  <br/> |[Célula SpAfter (Seção Paragraph)](spafter-cell-paragraph-section.md) <br/> |
|SpBefore  <br/> |Determina a quantidade de espaço inserido antes de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o primeiro parágrafo em um bloco de texto, da célula TopMargin.  <br/> |[Célula SpBefore (Seção Paragraph)](spbefore-cell-paragraph-section.md) <br/> |
|SpLine  <br/> |Determina a distância entre uma linha do texto e a próxima, expressa em porcentagem, sendo 100% a altura da linha de um texto.  <br/> |[Célula SpLine (Seção Paragraph)](spline-cell-paragraph-section.md) <br/> |
|TextPosAfterBullet  <br/> |Representa a distância entre a primeira linha do parágrafo e o marcador.  <br/> |[Célula TextPosAfterBullet (Seção Paragraph)](textposafterbullet-cell-paragraph-section.md) <br/> |
   

