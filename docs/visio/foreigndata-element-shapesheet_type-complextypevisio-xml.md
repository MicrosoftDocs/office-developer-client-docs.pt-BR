---
title: Elemento ForeignData (ShapeSheet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Contém um BLOB codificado de MIME (Multipurpose Internet Mail Extensions) de dados de imagem, como metarquivo do Windows, bitmap ou dados OLE.
ms.openlocfilehash: cce7665230fb9e68bf37002e1953944a5b8f8082
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346029"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>Elemento ForeignData (ShapeSheet_Type complexType) (' Visio XML ')

Contém um BLOB codificado de MIME (Multipurpose Internet Mail Extensions) de dados de imagem, como metarquivo do Windows, bitmap ou dados OLE.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|CompressionLevel  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica o nível de compactação aplicado ao arquivo. Este atributo só será significativo se os dados externos forem um objeto estrangeiro baseado em raster, como um arquivo DIB, JPG, PNG, TIFF ou GIF.  <br/> |Valores do tipo xsd: Double.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |opcional  <br/> |Especifica o tipo de compactação aplicada ao arquivo. Este atributo só será significativo se os dados externos forem um objeto estrangeiro baseado em raster, como um arquivo DIB, JPG, PNG, TIFF ou GIF  <br/> |Valores do tipo xsd:token.  <br/> |
|ExtentX  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica a extensão horizontal do metarquivo. Este atributo só será significativo se os dados externos forem um metarquivo.  <br/> |Valores do tipo xsd: Double.  <br/> |
|Extensão  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica a extensão vertical do metarquivo. Este atributo só será significativo se os dados externos forem um metarquivo.  <br/> |Valores do tipo xsd: Double.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |obrigatório  <br/> |Indica o metarquivo, EnhMetaFile, bitmap, objeto ou tipo de tinta.  <br/> |Valores do tipo xsd:token.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Especifica o modo de mapeamento de metarquivo. Este atributo só será significativo se os dados externos forem um metarquivo.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica a altura do objeto em unidades de página. Esse atributo só será significativo se os dados externos forem um objeto incorporado OLE2.  <br/> |Valores do tipo xsd: Double.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Um indicador inteiro de tipo de objeto. Usado quando o tipo Foreign é Object.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd: Double  <br/> |opcional  <br/> |Especifica a largura do objeto em unidades de página. Esse atributo só será significativo se os dados externos forem um objeto incorporado OLE2.  <br/> |Valores do tipo xsd: Double.  <br/> |
|{AsIc  <br/> |xsd:boolean  <br/> |opcional  <br/> |Indica se os dados inseridos devem ser mostrados ou não como um ícone.  <br/> |Valores do tipo xsd:boolean.  <br/> |
   

