---
title: Elemento section (Sheet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Especifica uma coleção de propriedades relacionadas.
ms.openlocfilehash: e20d076d4e1958cce29554d728b64385c2f8adef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326079"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Elemento section (Sheet_Type complexType) (' Visio XML ')

Especifica uma coleção de propriedades relacionadas.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Especifica as propriedades da página de desenho associada ao mestre.  <br/> |
|[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de propriedades associadas a uma forma.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de propriedades associadas a um estilo, desenho, página de desenho ou forma.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Especifica uma folha de estilos.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma única propriedade.  <br/> |
|[Linha](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de elementos **Cell_Type** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se uma coleção que seria herdada foi excluída. Ele deve ser igual a 0 ou 1. Um valor 1 especifica que a coleção não é usada e deve ser ignorada. Um valor de 0 especifica que a coleção de propriedades é válida para a forma. Se o atributo **del** não estiver presente, o valor será 0.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica o índice baseado em zero do elemento. Ele deve ser exclusivo entre todos os elementos **Section_Type** com o mesmo atributo **N** do **Sheet_Type**que o contém. Ele deve ser maior que o atributo **IX** de qualquer elemento **Section_Type** anterior com o mesmo atributo **N** do **Sheet_Type**que o contém.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|N  <br/> |xsd:string  <br/> |obrigatório  <br/> |Especifica o nome independente do idioma da coleção de propriedades. Ele deve ser exclusivo entre todos os elementos **Section_Type** do elemento **Sheet_Type** que o contém, a menos que seja igual a "Geometry". Ele deve ser igual a um subtítulo em **seções**.  <br/> |Valores do tipo xsd:string.  <br/> |
   
### <a name="remarks"></a>Comentários

O atributo **N** deste elemento **Section** deve ser um de um conjunto limitado de valores que correspondem às células do **ShapeSheet** . Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para este elemento de **seção** . 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|Ações  <br/> |Uma coleção de propriedades que são usadas para avaliação de fórmulas. Ele deve ter um elemento pai **ShapeSheet_Type** ou **PageSheet_Type** .  <br/> |[Seção Actions](actions-section.md) <br/> |
|ActionTag  <br/> |Uma coleção de propriedades que são usadas apenas para avaliação de fórmulas. Ele deve ter um elemento pai **ShapeSheet_Type** ou **PageSheet_Type** .  <br/> |[Seção de marca de ação](action-tag-section.md) <br/> |
|Conexões  <br/> |Uma coleção de propriedades que são usadas apenas para avaliação de fórmulas. Ele deve ter um elemento pai **ShapeSheet_Type** .  <br/> ||
|Controles  <br/> |Uma coleção de propriedades que são usadas apenas para avaliação de fórmulas. Ele deve ter um elemento pai **ShapeSheet_Type** .  <br/> |[Seção Controls](controls-section.md) <br/> |
|Hiperlink  <br/> |Uma coleção de propriedades relacionadas que especificam os hiperlinks da forma. Ele deve ter um elemento pai **ShapeSheet_Type** .  <br/> |[Seção Hyperlinks](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Uma coleção de propriedades relacionadas que especifica os dados da forma. Ele deve ter um elemento pai **ShapeSheet_Type** .  <br/> |[Seção Shape Data](shape-data-section.md) <br/> |
|Usuário  <br/> |Uma coleção de propriedades que são usadas para avaliação de fórmulas. Ele deve ter um elemento pai **DocumentSheet_Type**, **PageSheet_Type**ou **ShapeSheet_Type** .  <br/> |[Seção User-defined Cells](user-defined-cells-section.md) <br/> |
   
O atributo **IX** deste elemento **Section** deve ser um de um conjunto limitado de valores que correspondem às células do **ShapeSheet** . Consulte a tabela abaixo para determinar os valores do atributo **IX** que são permitidos para este elemento **Section** . 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|Comentário  <br/> |Uma coleção de propriedades que contém informações sobre comentários inseridos em uma página de documento.  <br/> |[Seção Annotation](annotation-section.md) <br/> |
|Caractere  <br/> |Uma coleção de propriedades relacionadas que especificam as propriedades de caracteres do texto de uma forma. Ele deve ter um elemento pai **ShapeSheet_Type** ou um elemento pai **StyleSheet_Type** .  <br/> |[Seção Character](character-section.md) <br/> |
|Conexões  <br/> |Uma coleção de propriedades que são usadas apenas para avaliação de fórmulas. Ele deve ter um elemento pai **ShapeSheet_Type** .  <br/> |[Seção Connection Points](connection-points-section.md) <br/> |
|Campo  <br/> |Uma coleção de propriedades relacionadas que especificam os campos de texto de uma forma. Ele deve ter um elemento pai **ShapeSheet_Type** .  <br/> |[Seção Text Fields](text-fields-section.md) <br/> |
|FillGradient  <br/> |Uma coleção de propriedades que especifica o gradiente de cor de preenchimento de uma forma. Ele deve ter um elemento pai **ShapeSheet_Type** ou **StyleSheet_Type** .  <br/> |[Seção Fill Gradient](fill-gradient-section.md) <br/> |
|Geometria  <br/> |Uma coleção de propriedades relacionadas que especificam a visualização de geometria. Ele deve ter um elemento pai **ShapeSheet_Type** . O primeiro elemento filho **Row_Type** desse elemento deve ser do tipo MoveTo, RelMoveTo, Ellipse ou InfiniteLine.  <br/> |[Seção Geometry](geometry-section.md) <br/> |
|Camadas  <br/> |Uma coleção de propriedades que mostram todas as camadas definidas em uma página de desenho. Ele deve ser o filho de um elemento **PageSheet_Type** .  <br/> |[Seção Layers](layers-section.md) <br/> |
|Gradiente de linha  <br/> |Uma coleção de propriedades relacionadas que especificam o Gradient de cor da linha de uma forma. Ele deve ter um elemento pai **ShapeSheet_Type** ou **StyleSheet_Type** .  <br/> |[Seção line Gradient](line-gradient-section.md) <br/> |
|Parágrafo  <br/> |Uma coleção de propriedades relacionadas que especificam as propriedades de parágrafo do texto de uma forma. Ele deve ter um elemento pai **ShapeSheet_Type** ou um elemento pai **StyleSheet_Type** .  <br/> |[Seção Paragraph](paragraph-section.md) <br/> |
|Revisor  <br/> |Uma coleção de propriedades que são usadas para avaliação de fórmulas. Ele deve ter um elemento pai **DocumentSheet_Type** .  <br/> |[Seção Reviewer](reviewer-section.md) <br/> |
|Zero  <br/> |Uma coleção de propriedades que são usadas para avaliação de fórmulas. Ele deve ter um elemento pai **DocumentSheet_Type**, **PageSheet_Type**ou **ShapeSheet_Type** .  <br/> |[Seção Scratch](scratch-section.md) <br/> |
|Guias  <br/> |Uma coleção de propriedades relacionadas que especifica as propriedades de guias do texto de uma forma. Ele deve ter um elemento pai **ShapeSheet_Type** ou um elemento pai **StyleSheet_Type** .  <br/> |[Seção Tabs](tabs-section.md) <br/> |
   

