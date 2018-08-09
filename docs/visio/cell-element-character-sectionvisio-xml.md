---
title: Elemento de célula (seção Character) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Especifica um atributo de formatação para sequência de texto de uma forma, como fonte, cor, estilo, caso, posição relativa à linha de base ou o tamanho do ponto.
ms.openlocfilehash: 0d0725ec6ff19104d95780dcfbb3fff9715cbe92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771444"
---
# <a name="cell-element-character-section-visio-xml"></a>Elemento de célula (seção Character) ('Visio XML')

Especifica um atributo de formatação para sequência de texto de uma forma, como fonte, cor, estilo, caso, posição relativa à linha de base ou o tamanho do ponto.
  
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
|[Elemento Row (Seção Character)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Especifica um atributo de formatação para sequência de texto de uma forma, como fonte, cor, estilo, caso, posição relativa à linha de base ou o tamanho do ponto.  <br/> |
   
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
|AsianFont  <br/> |Contém a enumeração da fonte utilizada para formatar um texto executar que contém caracteres asiáticos.  <br/> |[Célula AsianFont (Seção Character)](asianfont-cell-character-section.md) <br/> |
|Caso  <br/> |Determina o caso do fluxo de texto de uma forma.  <br/> |[Célula Case (Seção Character)](case-cell-character-section.md) <br/> |
|Cor  <br/> |Determina a cor utilizada para o fluxo de texto de uma forma.  <br/> |[Célula Color (Seção Character)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Determina o grau de transparência para uma camada ou o texto da forma executar cor, a partir de 0 (completamente opaco) até 1 (completamente transparente).  <br/> |Nenhum.  <br/> |
|ComplexScriptFont  <br/> |Contém o número da fonte utilizada para formatar um texto executar composto de caracteres de scripts complexos.  <br/> |[Célula ComplexScriptFont (Seção Character)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |O tamanho da fonte utilizada para formatar um texto execute composto de caracteres de scripts complexos.  <br/> |[Célula ComplexScriptSize (Seção Character)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Determina se o intervalo de uma execução de texto possui um sublinhado duplo abaixo dele.  <br/> |[Célula DoubleULine (Seção Character)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Determina se um fluxo de texto está formatado como tachado duplo.  <br/> |[Célula DoubleStrikethrough (Seção Character)](doublestrikethrough-cell-character-section.md) <br/> |
|Font  <br/> |Representa o número da fonte usada para formatar uma execução de texto.  <br/> |[Célula Font (Seção Character)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Especifica a largura da fonte.  <br/> |Nenhum.  <br/> |
|LangID  <br/> |Indica o idioma no qual executar um texto foi inserido.  <br/> |[Célula LangID (Seção Character)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Especifica a quantidade de espaço entre dois ou mais caracteres. Espaço pode ser adicionado ou subtraído em incrementos de 1/20 pontos.  <br/> |Nenhum.  <br/> |
|Linha sobreposta  <br/> |Determina se um fluxo de texto tem uma linha acima dele.  <br/> |[Célula Overline (Seção Character)](overline-cell-character-section.md) <br/> |
|POS  <br/> |Determina a posição do texto de uma forma executado em relação à linha de base.  <br/> |[Célula Pos (Seção Character)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Determina o tamanho de um fluxo no bloco de texto da forma de texto.  <br/> |[Célula Size (Seção Character)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Determina se um fluxo de texto está formatado como tachado.  <br/> |[Célula Strikethru (Seção Character)](strikethru-cell-character-section.md) <br/> |
|Style  <br/> |Mostra que a formatação de caracteres aplicada a um intervalo de um texto execute no bloco de texto da forma.  <br/> |[Célula Style (Seção Character)](style-cell-character-section.md) <br/> |
   

