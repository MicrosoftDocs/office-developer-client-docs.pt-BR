---
title: Elemento de forma (Shapes_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Contém os elementos que definem a uma forma em um mestre, página ou elemento de forma do grupo.
ms.openlocfilehash: 8c0a288858e2aaccbd3afadcdc1b057565dd30ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772891"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>Elemento de forma (Shapes_Type complexType) ('Visio XML')

Contém os elementos que definem a uma forma em um **mestre**, **página**ou elemento de forma do grupo.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |página # XML, master. XML de #  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica um conjunto de formas.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica um conjunto de formas.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Célula](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma única propriedade.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contém um valor de cadeia de caracteres arbitrária que é usado para fornecer informações adicionais sobre uma forma.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contém um valor de cadeia de caracteres arbitrária que é usado para fornecer informações adicionais sobre uma forma.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Contém um valor de cadeia de caracteres arbitrária que é usado para fornecer informações adicionais sobre uma forma.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Contém um BLOB codificado de MIME (Multipurpose Internet Mail Extensions) de dados de imagem, como dados OLE, bitmap ou metarquivo do Windows.  <br/> |
|[Seção](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Especifica uma coleção de propriedades relacionadas.  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Especifica um conjunto de formas.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contém o texto de uma forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|DEL  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Um sinalizador indicando se o elemento é excluído localmente.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|FillStyle  <br/> |XSD:unsignedInt  <br/> ||A identificação da folha de estilos da qual esta forma herda a formatação de preenchimento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Indica se o nome tiver sido personalizado pelo usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Indica se o nome universal foi personalizado pelo usuário..  <br/> |Valores do tipo xsd:boolean.  <br/> |
|LineStyle  <br/> |XSD:unsignedInt  <br/> ||A identificação da folha de estilos da qual esta forma herda a formatação de linha.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Master  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A ID do mestre elemento da qual a forma herda seus dados.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|MasterShape  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A ID do mestre elemento da qual a forma herda seus dados.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |XSD: String  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|TextStyle  <br/> |XSD:unsignedInt  <br/> ||A identificação da folha de estilos da qual esta forma herda a formatação de texto.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Tipo  <br/> |XSD:token  <br/> |opcional  <br/> |O tipo de uma forma. Pode ser um dos seguintes valores: forma, grupo, guia ou externo.  <br/> |Valores do tipo xsd:token.  <br/> |
|UniqueID  <br/> |XSD: String  <br/> |opcional  <br/> |Um GUID (identificador global exclusivo) atribuído à forma.  <br/> |Valores do tipo xsd: String.  <br/> |
   

