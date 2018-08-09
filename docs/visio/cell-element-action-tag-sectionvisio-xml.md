---
title: Elemento de célula (seção marca de ação) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Define uma propriedade para uma marca de ação em uma forma ou página.
ms.openlocfilehash: 0945235c49e77210564e50e5c111579ab37f3e31
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771428"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Elemento de célula (seção marca de ação) ('Visio XML')

Define uma propriedade para uma marca de ação em uma forma ou página.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Masters.XML,. XML de # mestre, pages.xml,. XML n º de página  <br/> |
   
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
|[Elemento de linha (seção ActionTag)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Define uma marca de ação em uma forma ou página.  <br/> |
   
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
|ButtonFace  <br/> |Contém a identificação da imagem da face do botão exibido no botão de marca de ação.  <br/> |[Célula ButtonFace (Seção Action Tags)](buttonface-cell-action-tags-section.md) <br/> |
|Descrição  <br/> |Contém uma cadeia de caracteres que descreve a marca de ação, exibida como dica de ferramenta, quando os usuários posicionam o ponteiro sobre a marca.  <br/> |[Célula Description (Seção Action Tags)](description-cell-action-tags-section.md) <br/> |
|Desabilitado  <br/> |Indica se a marca de ação é exibida na janela de desenho.  <br/> |[Célula Disabled (Seção Action Tags)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Determina se a marca de ação aparece quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.  <br/> |[Célula DisplayMode (seção de marcas de ação)](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |Nome da marca de ação usada como chave para associar a marca de ação a suas ações.  <br/> |[Célula TagName (Seção Action Tags)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |A posição da coordenada x nas coordenadas locais da forma em torno da qual é colocado o botão de marca de ação.  <br/> |[Célula X (Seção Action Tags)](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |O deslocamento x do botão de marca de ação referente ao ponto definido pelas células X e Y.  <br/> |[Célula X Justify (Seção Action Tags)](x-justify-cell-action-tags-section.md) <br/> |
|Y  <br/> |A posição da coordenada y nas coordenadas locais da forma em torno da qual é colocado o botão de marca de ação.  <br/> |[Célula Y (Seção Action Tags)](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |O deslocamento y do botão de marca de ação em relação ao ponto definido pelas células X e Y.  <br/> |[Célula Y Justify (Seção Action Tags)](y-justify-cell-action-tags-section.md) <br/> |
   

