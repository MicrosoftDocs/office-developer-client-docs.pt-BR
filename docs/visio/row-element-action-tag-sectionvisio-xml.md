---
title: Elemento de linha (seção marca de ação) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: Define uma marca de ação em uma forma ou página.
ms.openlocfilehash: 1e5e432b05b1dfcd02dded41253a79802c9caf81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772760"
---
# <a name="row-element-action-tag-section-visio-xml"></a>Elemento de linha (seção marca de ação) ('Visio XML')

Define uma marca de ação em uma forma ou página.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ActionTagRow_Type](actiontagrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Masters.XML,. XML de # mestre, pages.xml,. XML n º de página  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Seção](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Define uma marca de ação em uma forma ou página.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Célula](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Define uma propriedade para uma marca de ação em uma forma ou página.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica se uma linha que seria contrário herdada de uma forma mestra foi excluída.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica o identificador baseada em um para a linha. Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX é usado somente para as seções de caractere, Conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, zero e guias. Uma linha só pode ter um dos atributos IX ou N.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica o nome exclusivo do dependentes de idioma da linha.  <br/> |Valores do tipo xsd: String.  <br/> |
|N  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica o nome exclusivo do independente do idioma da linha. O atributo N é usado somente para as seções do usuário, propriedade, ações, controle, Conexão, hiperlink e ActionTag. Uma linha só pode ter um dos atributos IX ou N.  <br/> |Valores do tipo xsd: String.  <br/> |
|T  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica o tipo do caminho geométrico representado por linha e usada na visualização de geometria. O atributo T é usado apenas para a seção Geometry.  <br/> |Valores do tipo xsd: String.  <br/> |
   

