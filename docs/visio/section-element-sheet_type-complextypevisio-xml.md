---
title: Elemento Section (Sheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Especifica uma coleção de propriedades relacionadas.
ms.openlocfilehash: 2862d2ccf10d235996c2a6fb26691d498bdfdbcf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539030"
---
# <a name="section-element-sheet_type-complextype-visio-xml"></a>Elemento Section (Sheet_Type complexType) (XML do Visio)

Especifica uma coleção de propriedades relacionadas.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Especifica as propriedades de um desenho.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica as propriedades de uma página em um desenho.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Especifica as propriedades da página de desenho associadas ao mestre.  <br/> |
|[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de propriedades associadas a uma forma.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de propriedades associadas a um estilo, desenho, página de desenho ou forma.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Especifica uma folha de estilos.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma única propriedade.  <br/> |
|[Linha](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de **Cell_Type** elementos.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se uma coleção que seria herdada foi excluída. Deve ser igual a 0 ou 1. Um valor 1 especifica que a coleção não é usada e DEVE ser ignorada. Um valor 0 especifica que a coleção de propriedades é válida para a forma. Se o **atributo Del** não estiver presente, o valor será 0.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica o índice baseado em zero do elemento. Ele DEVE ser exclusivo entre todos os elementos **Section_Type** com o mesmo **atributo N** do Sheet_Type **.** Ele DEVE ser maior que o atributo **IX** de qualquer elemento **Section_Type** anterior com o mesmo **atributo N** do Sheet_Type **.**  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|N  <br/> |xsd:string  <br/> |obrigatório  <br/> |Especifica o nome independente do idioma da coleção de propriedades. Ele DEVE ser exclusivo entre todos os **Section_Type** elementos do elemento **Sheet_Type,** a menos que seja igual a "Geometry". Ele DEVE ser igual a um subheading em **Seções**.  <br/> |Valores do tipo xsd:string.  <br/> |
   
### <a name="remarks"></a>Comentários

O **atributo N** deste elemento **Section** deve ser um de um conjunto limitado de valores que correspondem às **células ShapeSheet.** Consulte a tabela abaixo para determinar os valores do **atributo N** que são permitidos para este **elemento Section.** 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|Ações  <br/> |Uma coleção de propriedades usadas para avaliação de fórmulas. Ele DEVE ter um **ShapeSheet_Type** ou **PageSheet_Type** elemento pai.  <br/> |[Seção Actions](actions-section.md) <br/> |
|ActionTag  <br/> |Uma coleção de propriedades que são usadas somente para avaliação de fórmulas. Ele DEVE ter um **ShapeSheet_Type** ou **PageSheet_Type** elemento pai.  <br/> |[Seção de marca de ação](action-tag-section.md) <br/> |
|Conexões  <br/> |Uma coleção de propriedades que são usadas somente para avaliação de fórmulas. Ele DEVE ter um **ShapeSheet_Type** elemento pai.  <br/> ||
|Controles  <br/> |Uma coleção de propriedades que são usadas somente para avaliação de fórmulas. Ele DEVE ter um **ShapeSheet_Type** elemento pai.  <br/> |[Seção Controls](controls-section.md) <br/> |
|Hiperlink  <br/> |Uma coleção de propriedades relacionadas que especificam os hiperlinks de forma. Ele DEVE ter um **ShapeSheet_Type** elemento pai.  <br/> |[Seção Hyperlinks](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Uma coleção de propriedades relacionadas que especificam os dados da forma. Ele DEVE ter um **ShapeSheet_Type** elemento pai.  <br/> |[Seção Shape Data](shape-data-section.md) <br/> |
|Usuário  <br/> |Uma coleção de propriedades usadas para avaliação de fórmulas. Ele DEVE ter um **DocumentSheet_Type,** **PageSheet_Type** **ou** ShapeSheet_Type elemento pai.  <br/> |[Seção User-defined Cells](user-defined-cells-section.md) <br/> |
   
O **atributo IX** deste elemento **Section** deve ser um de um conjunto limitado de valores que correspondem às **células ShapeSheet.** Consulte a tabela abaixo para determinar os valores do atributo **IX** que são permitidos para este **elemento Section.** 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|Annotation  <br/> |Uma coleção de propriedades que contém informações sobre comentários inseridos em uma página de documento.  <br/> |[Seção Annotation](annotation-section.md) <br/> |
|Caractere  <br/> |Uma coleção de propriedades relacionadas que especificam as propriedades de caractere do texto de uma forma. Ele DEVE ter um **ShapeSheet_Type** pai ou um **StyleSheet_Type** pai.  <br/> |[Seção Character](character-section.md) <br/> |
|Conexões  <br/> |Uma coleção de propriedades que são usadas somente para avaliação de fórmulas. Ele DEVE ter um **ShapeSheet_Type** elemento pai.  <br/> |[Seção Connection Points](connection-points-section.md) <br/> |
|Campo  <br/> |Uma coleção de propriedades relacionadas que especificam os campos de texto de uma forma. Ele DEVE ter um **ShapeSheet_Type** elemento pai.  <br/> |[Seção Text Fields](text-fields-section.md) <br/> |
|FillGradient  <br/> |Uma coleção de propriedades que especificam o gradiente de cor de preenchimento de uma forma. Ele DEVE ter um **ShapeSheet_Type** ou **StyleSheet_Type** pai.  <br/> |[Seção Fill Gradient](fill-gradient-section.md) <br/> |
|Geometria  <br/> |Uma coleção de propriedades relacionadas que especificam a visualização de geometria. Ele DEVE ter um **ShapeSheet_Type** elemento pai. O primeiro **Row_Type** elemento filho desse elemento DEVE ser do tipo MoveTo, RelMoveTo, Ellipse ou InfiniteLine.  <br/> |[Seção Geometry](geometry-section.md) <br/> |
|Camadas  <br/> |Uma coleção de propriedades que mostra todas as camadas definidas em uma página de desenho. Ele DEVE ser o filho de um **PageSheet_Type** elemento.  <br/> |[Seção Layers](layers-section.md) <br/> |
|Gradiente de Linha  <br/> |Uma coleção de propriedades relacionadas que especificam o gradiente de cor de linha de uma forma. Ele DEVE ter um **ShapeSheet_Type** ou **StyleSheet_Type** pai.  <br/> |[Seção Line Gradient](line-gradient-section.md) <br/> |
|Parágrafo  <br/> |Uma coleção de propriedades relacionadas que especificam as propriedades de parágrafo do texto de uma forma. Ele DEVE ter um **ShapeSheet_Type** pai ou um **StyleSheet_Type** pai.  <br/> |[Seção Paragraph](paragraph-section.md) <br/> |
|Revisor  <br/> |Uma coleção de propriedades usadas para avaliação de fórmulas. Ele DEVE ter um **DocumentSheet_Type** elemento pai.  <br/> |[Seção Reviewer](reviewer-section.md) <br/> |
|Scratch  <br/> |Uma coleção de propriedades usadas para avaliação de fórmulas. Ele DEVE ter um **DocumentSheet_Type,** **PageSheet_Type** **ou** ShapeSheet_Type elemento pai.  <br/> |[Seção Scratch](scratch-section.md) <br/> |
|Guias  <br/> |Uma coleção de propriedades relacionadas que especificam as propriedades de guias do texto de uma forma. Ele DEVE ter um **ShapeSheet_Type** pai ou um **StyleSheet_Type** pai.  <br/> |[Seção Tabs](tabs-section.md) <br/> |
   

