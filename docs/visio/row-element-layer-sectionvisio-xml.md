---
title: Elemento Row (Seção Layer) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Contém elementos que definem uma única camada e suas propriedades para uma página.
ms.openlocfilehash: edd076651838d7522af07013cda5fedd9a28de7f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540859"
---
# <a name="row-element-layer-section-visio-xml"></a>Elemento Row (Seção Layer) (Visio XML)

Contém elementos que definem uma única camada e suas propriedades para uma página.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |masters.xml, pages.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contém elementos que definem uma única camada e suas propriedades para uma página.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Cell](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma propriedade para uma camada ou suas propriedades para uma página.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se uma linha que seria herdada de uma forma mestra foi excluída.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica o identificador baseado em um para a linha. Ele deve ser unqiue e maior do que outros identificadores na mesma seção. O atributo IX só é usado para as seções Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch e Tabs. Uma linha só pode ter um dos atributos IX ou N.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o nome exclusivo dependente do idioma da linha.  <br/> |Valores do tipo xsd:string.  <br/> |
|N  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o nome exclusivo da linha independente do idioma. O atributo N só é usado para as seções User, Property, Actions, Control, Connection, Hyperlink e ActionTag. Uma linha só pode ter um dos atributos IX ou N.  <br/> |Valores do tipo xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o tipo do caminho geométrico representado pela linha e usado na visualização de geometria. O atributo T só é usado para a seção Geometry.  <br/> |Valores do tipo xsd:string.  <br/> |
   

