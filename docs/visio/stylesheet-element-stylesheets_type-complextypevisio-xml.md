---
title: Elemento StyleSheet (StyleSheets_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: Representa um estilo definido em um documento.
ms.openlocfilehash: 2513c7421dc8f890b7ba63f19cf3d31d23ce65ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773086"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a>Elemento StyleSheet (StyleSheets_Type complexType) ('Visio XML')

Representa um estilo definido em um documento.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Folhas de estilo](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Contém uma coleção de elementos de **folha de estilos** do documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Célula](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma única propriedade.  <br/> |
|[Seção](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de propriedades relacionadas.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A identificação do elemento StyleSheet da qual esse estilo herda a formatação de preenchimento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Indica se o nome tiver sido personalizado pelo usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Indica se o nome universal foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|LineStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A identificação do elemento StyleSheet da qual esse estilo herda a formatação de linha.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |XSD: String  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|TextStyle  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A identificação do elemento StyleSheet da qual esse estilo herda a formatação de texto.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

