---
title: Elemento ForeignData (ShapeSheet_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Contém um BLOB codificado mime (Multipurpose Internet Mail Extensions) de dados de imagem, como metarquivo do Windows, bitmap ou dados OLE.
ms.openlocfilehash: 6b130b5a50a51d5d909b843e805d197735dc7146
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539839"
---
# <a name="foreigndata-element-shapesheet_type-complextype-visio-xml"></a>Elemento ForeignData (ShapeSheet_Type complexType) (XML do Visio)

Contém um BLOB codificado mime (Multipurpose Internet Mail Extensions) de dados de imagem, como metarquivo do Windows, bitmap ou dados OLE.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contém elementos que definem uma forma em um elemento **Master**, **Page** ou group shape.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica uma relação com uma parte que contém os dados da imagem.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica o nível de compactação aplicado ao arquivo. Esse atributo só será significativo se os dados externos for um objeto externo baseado em rasteres, como um arquivo DIB, JPG, PNG, TIFF ou GIF.  <br/> |Valores do tipo xsd:double.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |opcional  <br/> |Especifica o tipo de compactação aplicada ao arquivo. Esse atributo só será significativo se os dados externos for um objeto externo baseado em rasteres, como um arquivo DIB, JPG, PNG, TIFF ou GIF  <br/> |Valores do tipo xsd:token.  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica a extensão horizontal do metadado. Esse atributo só será significativo se os dados externos for um metadado.  <br/> |Valores do tipo xsd:double.  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica a extensão vertical do metadado. Esse atributo só será significativo se os dados externos for um metadado.  <br/> |Valores do tipo xsd:double.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |obrigatório  <br/> |Indica o tipo de metadado, EnhMetaFile, Bitmap, Objeto ou Tinta.  <br/> |Valores do tipo xsd:token.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Especifica o modo de mapeamento de metadados. Esse atributo só será significativo se os dados externos for um metadado.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica a altura do objeto em unidades de página. Esse atributo só será significativo se os dados externos for um objeto incorporado OLE2.  <br/> |Valores do tipo xsd:double.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Um indicador inteiro do tipo de objeto. Usado quando o tipo Externo é um objeto.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |opcional  <br/> |Especifica a largura do objeto em unidades de página. Esse atributo só será significativo se os dados externos for um objeto incorporado OLE2.  <br/> |Valores do tipo xsd:double.  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |opcional  <br/> |Indica se é para mostrar ou não dados incorporados como um ícone.  <br/> |Valores do tipo xsd:boolean.  <br/> |
   

