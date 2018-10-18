---
title: Elemento Cell (Seção Character) Visio XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Especifica um atributo de formatação para o formato de escrita do texto, como fonte, cor, estilo, caso, posição relativa à linha de base ou tamanho de ponto.
ms.openlocfilehash: 6dd895b33353944d27abb0d64a6a6df64ca19896
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384245"
---
# <a name="cell-element-character-section-visio-xml"></a>Elemento Cell (Seção Character) Visio XML

Especifica um atributo de formatação para o formato de escrita do texto, como fonte, cor, estilo, caso, posição relativa à linha de base ou tamanho de ponto.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Elemento Row (Seção Character)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Especifica um atributo de formatação para o formato de escrita do texto, como fonte, cor, estilo, caso, posição relativa à linha de base ou tamanho de ponto.  <br/> |
   
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
|S  <br/> |xsd:string  <br/> |opcional  <br/> |Representa uma unidade de medida. O padrão é DL.  <br/> |As unidades da célula.  <br/> |
|S  <br/> |xsd:string  <br/> |opcional  <br/> |Representa o valor da célula.  <br/> |O valor da célula ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **N** deste elemento **Cell** deve incluir um conjunto limitado de valores que correspondem às células ShapeSheet. Confira a tabela a seguir para determinar os valores do atributo **N** permitidos para este elemento **Cell**. 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|AsianFont  <br/> |Contém a enumeração da fonte usada para formatar um texto que possui caracteres asiáticos.  <br/> |[Célula AsianFont (Seção Character)](asianfont-cell-character-section.md) <br/> |
|Caso  <br/> |Determina maiusculas e minúsculas na execução do texto.  <br/> |[Célula Case (Seção Character)](case-cell-character-section.md) <br/> |
|Cor  <br/> |Determina a cor utilizada no texto da forma.  <br/> |[Célula Color (Seção Character)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Determina o grau de transparência de uma camada ou cor de texto de 0 (totalmente opaco) e 1 (totalmente transparente).  <br/> |Nenhum.  <br/> |
|ComplexScriptFont  <br/> |Contém o número do tamanho da fonte utilizada para formatar o texto composto de caracteres de scripts complexos.  <br/> |[Célula ComplexScriptFont (Seção Character)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |O tamanho da fonte utilizada para formatar o texto composto de caracteres de scripts complexos.  <br/> |[Célula ComplexScriptSize (Seção Character)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Determina se o intervalo do fluxo de texto contém um sublinhado duplo abaixo dele.  <br/> |[Célula DoubleULine (Seção Character)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Determina se um fluxo de texto é formatado como tachado duplo.  <br/> |[Célula DoubleStrikethrough (Seção Character)](doublestrikethrough-cell-character-section.md) <br/> |
|Fonte  <br/> |Representa o número da fonte usada para formatar um fluxo de texto.  <br/> |[Célula Font (Seção Character)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Especifica a largura da fonte.  <br/> |Nenhum.  <br/> |
|LangID  <br/> |Indica o idioma no qual um fluxo de texto foi inserido.  <br/> |[Célula LangID (Seção Character)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Especifica a quantidade de espaço entre as dois ou mais caracteres. Espaço pode ser adicionado ou subtraído em incrementos de 1/20 pontos.  <br/> |Nenhum.  <br/> |
|Posta  <br/> |Determina se um fluxo de texto tem uma linha acima dela.  <br/> |[Célula Overline (Seção Character)](overline-cell-character-section.md) <br/> |
|Pos  <br/> |Determina a posição do texto da forma executar em relação a linha de base.  <br/> |[Célula Pos (Seção Character)](pos-cell-character-section.md) <br/> |
|Size  <br/> |Determina o tamanho de um fluxo de texto no bloco de texto da forma.  <br/> |[Célula Size (Seção Character)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Determina se um fluxo de texto é formatado como tachado.  <br/> |[Célula Strikethru (Seção Character)](strikethru-cell-character-section.md) <br/> |
|Estilo  <br/> |Mostra a formatação de caracteres aplicada a um intervalo de um texto no bloco de texto da forma.  <br/> |[Célula Style (Seção Character)](style-cell-character-section.md) <br/> |
   

