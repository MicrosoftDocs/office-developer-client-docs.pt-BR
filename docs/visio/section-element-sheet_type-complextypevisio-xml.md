---
title: Elemento de seção (Sheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Especifica uma coleção de propriedades relacionadas.
ms.openlocfilehash: 7cb5e1c30960e69b252abc7af38e021607fd3502
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772857"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Elemento de seção (Sheet_Type complexType) ('Visio XML')

Especifica uma coleção de propriedades relacionadas.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document, masters.xml,. XML de # mestre, pages.xml,. XML n º de página  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Especifica as propriedades de um desenho.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica as propriedades de uma página em um desenho.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Especifica as propriedades da página de desenho associados com o mestre.  <br/> |
|[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica um conjunto de propriedades associadas a uma forma.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Especifica um conjunto de propriedades associadas a um estilo, do desenho, desenho página ou forma.  <br/> |
|[Folha de estilos](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Especifica uma folha de estilo.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Célula](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma única propriedade.  <br/> |
|[Row](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Especifica um conjunto de elementos de **Cell_Type** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica se uma coleção que, caso contrário, seria herdada foi excluída. Ela deve ser igual a 0 ou 1. Um valor de 1 Especifica que a coleção não é utilizada e deve ser ignorada. Um valor 0 especifica que a coleção das propriedades é válida para a forma. Se o atributo **Del** não estiver presente, o valor é 0.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Especifica o índice baseado em zero do elemento. Ela deve ser exclusiva entre todos os elementos de **Section_Type** com o mesmo atributo **N** do contendo **Sheet_Type**. Ele deve ser maior do que o atributo **IX** de qualquer elemento de **Section_Type** anterior com o mesmo atributo **N** do contendo **Sheet_Type**.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|N  <br/> |XSD: String  <br/> |obrigatório  <br/> |Especifica o nome independente do idioma da coleção de propriedades. Ela deve ser exclusiva entre todos os elementos de **Section_Type** do elemento **Sheet_Type** contido, a menos que é igual a "Geometria". Ela deve ser igual a um subtítulo nas **seções**.  <br/> |Valores do tipo xsd: String.  <br/> |
   
### <a name="remarks"></a>Comentários

O atributo **N** deste elemento de **seção** deve ser um conjunto limitado de valores que corresponde às células da **ShapeSheet** . Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para esse elemento da **seção** . 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|Actions  <br/> |Uma coleção de propriedades que são usados para avaliação de fórmulas. Ele deve ter um elemento de pai **ShapeSheet_Type** ou **PageSheet_Type** .  <br/> |[Seção Actions](actions-section.md) <br/> |
|ActionTag  <br/> |Uma coleção de propriedades que são usados para avaliação de fórmulas apenas. Ele deve ter um elemento de pai **ShapeSheet_Type** ou **PageSheet_Type** .  <br/> |[Seção de marca de ação](action-tag-section.md) <br/> |
|Connections  <br/> |Uma coleção de propriedades que são usados para avaliação de fórmulas apenas. Ele deve ter um elemento de pai **ShapeSheet_Type** .  <br/> ||
|Controles  <br/> |Uma coleção de propriedades que são usados para avaliação de fórmulas apenas. Ele deve ter um elemento de pai **ShapeSheet_Type** .  <br/> |[Seção Controls](controls-section.md) <br/> |
|Hiperlink  <br/> |Uma coleção de propriedades relacionadas que especificam os hiperlinks da forma. Ele deve ter um elemento de pai **ShapeSheet_Type** .  <br/> |[Seção Hyperlinks](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Uma coleção de propriedades relacionadas que especificam os dados da forma. Ele deve ter um elemento de pai **ShapeSheet_Type** .  <br/> |[Seção Shape Data](shape-data-section.md) <br/> |
|Usuário  <br/> |Uma coleção de propriedades que são usados para avaliação de fórmulas. Ele deve ter um elemento de pai **DocumentSheet_Type**, **PageSheet_Type**ou **ShapeSheet_Type** .  <br/> |[Seção User-defined Cells](user-defined-cells-section.md) <br/> |
   
O atributo **IX** deste elemento de **seção** deve ser um conjunto limitado de valores que corresponde às células da **ShapeSheet** . Consulte a tabela abaixo para determinar os valores do atributo **IX** que são permitidos para esse elemento da **seção** . 
  
|**Valor**|**Descrição**|**Mais informações**|
|:-----|:-----|:-----|
|Annotation  <br/> |Uma coleção de propriedades que contêm informações sobre comentários inseridos na página de um documento.  <br/> |[Seção Annotation](annotation-section.md) <br/> |
|Caractere  <br/> |Uma coleção de propriedades relacionadas que especificam as propriedades de caractere do texto de uma forma. Ele deve ter um elemento de pai **ShapeSheet_Type** ou um elemento de pai **StyleSheet_Type** .  <br/> |[Seção Character](character-section.md) <br/> |
|Connections  <br/> |Uma coleção de propriedades que são usados para avaliação de fórmulas apenas. Ele deve ter um elemento de pai **ShapeSheet_Type** .  <br/> |[Seção Connection Points](connection-points-section.md) <br/> |
|Field  <br/> |Uma coleção de propriedades relacionadas que especificam os campos de texto de uma forma. Ele deve ter um elemento de pai **ShapeSheet_Type** .  <br/> |[Seção Text Fields](text-fields-section.md) <br/> |
|FillGradient  <br/> |Uma coleção de propriedades que especificam o gradiente de cor de preenchimento de uma forma. Ele deve ter um elemento de pai **ShapeSheet_Type** ou **StyleSheet_Type** .  <br/> |[Seção Fill Gradient](fill-gradient-section.md) <br/> |
|Geometry  <br/> |Uma coleção de propriedades relacionadas que especificam a visualização de geometria. Ele deve ter um elemento de pai **ShapeSheet_Type** . O primeiro elemento filho **Row_Type** deste elemento deve ser do tipo MoveTo, RelMoveTo, Ellipse ou InfiniteLine.  <br/> |[Seção Geometry](geometry-section.md) <br/> |
|Layers  <br/> |Uma coleção de propriedades que mostram todas as camadas definidas em uma página de desenho. Ela deve ser o filho de um elemento **PageSheet_Type** .  <br/> |[Seção Layers](layers-section.md) <br/> |
|Gradiente de linha  <br/> |Uma coleção de propriedades relacionadas que especificam um gradiente de cores de linha de uma forma. Ele deve ter um elemento de pai **ShapeSheet_Type** ou **StyleSheet_Type** .  <br/> |[Seção Line Gradient](line-gradient-section.md) <br/> |
|Paragraph  <br/> |Uma coleção de propriedades relacionadas que especificam as propriedades de parágrafo do texto de uma forma. Ele deve ter um elemento de pai **ShapeSheet_Type** ou um elemento de pai **StyleSheet_Type** .  <br/> |[Seção Paragraph](paragraph-section.md) <br/> |
|Reviewer  <br/> |Uma coleção de propriedades que são usados para avaliação de fórmulas. Ele deve ter um elemento de pai **DocumentSheet_Type** .  <br/> |[Seção Reviewer](reviewer-section.md) <br/> |
|Zero  <br/> |Uma coleção de propriedades que são usados para avaliação de fórmulas. Ele deve ter um elemento de pai **DocumentSheet_Type**, **PageSheet_Type**ou **ShapeSheet_Type** .  <br/> |[Seção Scratch](scratch-section.md) <br/> |
|Guias  <br/> |Uma coleção de propriedades relacionadas que especificam as propriedades de guias do texto de uma forma. Ele deve ter um elemento de pai **ShapeSheet_Type** ou um elemento de pai **StyleSheet_Type** .  <br/> |[Seção Tabs](tabs-section.md) <br/> |
   

