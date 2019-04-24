---
title: Elemento StyleSheet (StyleSheets_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: Representa um estilo definido em um documento.
ms.openlocfilehash: af1f8270be28e7edabf22d93471517531f5cc226
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329796"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a>Elemento StyleSheet (StyleSheets_Type complexType) (' Visio XML ')

Representa um estilo definido em um documento.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Contém uma coleção de elementos **StyleSheet** para o documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma única propriedade.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de propriedades relacionadas.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A ID do elemento de folha de estilos do qual esse estilo herda a formatação de preenchimento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A identificação exclusiva do elemento no seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |opcional  <br/> |Indica se o nome foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |opcional  <br/> |Indica se o nome Universal foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A ID do elemento de folha de estilos do qual esse estilo herda a formatação de linha.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |xsd:string  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A ID do elemento de folha de estilos do qual esse estilo herda a formatação de texto.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

