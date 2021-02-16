---
title: Elemento Shape (Shapes_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Contém elementos que definem uma forma em um elemento Master, Page ou group shape.
ms.openlocfilehash: aa7ffa539c9f82adc486bd0848dda66798bac165
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542069"
---
# <a name="shape-element-shapes_type-complextype-visio-xml"></a>Elemento Shape (Shapes_Type complexType) (XML do Visio)

Contém elementos que definem uma forma em um elemento **Master**, **Page** ou group shape.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de formas.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de formas.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma única propriedade.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contém um valor arbitrário de cadeia de caracteres usado para fornecer informações adicionais sobre uma forma.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contém um valor arbitrário de cadeia de caracteres usado para fornecer informações adicionais sobre uma forma.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contém um valor arbitrário de cadeia de caracteres usado para fornecer informações adicionais sobre uma forma.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Contém um BLOB codificado mime (Multipurpose Internet Mail Extensions) de dados de imagem, como metarquivo do Windows, bitmap ou dados OLE.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de propriedades relacionadas.  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de formas.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contém o texto de uma forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |opcional  <br/> |Um sinalizador indicando se o elemento é excluído localmente.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|FillStyle  <br/> |xsd:unsignedInt  <br/> ||A ID da StyleSheet da qual essa forma herda a formatação de preenchimento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |opcional  <br/> |Indica se o nome foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |opcional  <br/> |Indica se o nome universal foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> ||A ID da StyleSheet da qual essa forma herda a formatação de linha.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A ID do elemento Master do qual a forma herda seus dados.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|MasterShape  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A ID do elemento Master do qual a forma herda seus dados.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |xsd:string  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> ||A ID da StyleSheet da qual essa forma herda a formatação de texto.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Tipo  <br/> |xsd:token  <br/> |opcional  <br/> |O tipo de uma forma. Pode ser um dos seguintes valores: Grupo, Forma, Guia ou Externo.  <br/> |Valores do tipo xsd:token.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |opcional  <br/> |Um GUID (identificador global exclusivo) atribuído à forma.  <br/> |Valores do tipo xsd:string.  <br/> |
   

