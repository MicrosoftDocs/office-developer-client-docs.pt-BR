---
title: Elemento ForeignData (ShapeSheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Contém um BLOB codificado de MIME (Multipurpose Internet Mail Extensions) de dados de imagem, como dados OLE, bitmap ou metarquivo do Windows.
ms.openlocfilehash: cce7665230fb9e68bf37002e1953944a5b8f8082
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382678"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>Elemento ForeignData (ShapeSheet_Type complexType) ('Visio XML')

Contém um BLOB codificado de MIME (Multipurpose Internet Mail Extensions) de dados de imagem, como dados OLE, bitmap ou metarquivo do Windows.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |página # XML, master. XML de #  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Contém os elementos que definem a uma forma em um **mestre**, **página**ou elemento de forma do grupo.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica uma relação a uma parte contendo os dados de imagem.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD:Double  <br/> |opcional  <br/> |Especifica o nível de compactação aplicada ao arquivo. Este atributo só é significativo se os dados externos são um objeto estranho baseado em varredura, de como um arquivo GIF, JPG, PNG, TIFF ou DIB.  <br/> |Valores do tipo xsd:double.  <br/> |
|CompressionType  <br/> |XSD:token  <br/> |opcional  <br/> |Especifica o tipo de compactação aplicada ao arquivo. Este atributo só é significativo se os dados externos são um objeto estranho baseado em varredura, de como um arquivo GIF, JPG, PNG, TIFF ou DIB  <br/> |Valores do tipo xsd:token.  <br/> |
|ExtentX  <br/> |XSD:Double  <br/> |opcional  <br/> |Especifica a extensão horizontal do metarquivo. Este atributo só é significativo se os dados externos forem um metarquivo.  <br/> |Valores do tipo xsd:double.  <br/> |
|ExtentY  <br/> |XSD:Double  <br/> |opcional  <br/> |Especifica a extensão vertical do metarquivo. Este atributo só é significativo se os dados externos forem um metarquivo.  <br/> |Valores do tipo xsd:double.  <br/> |
|ForeignType  <br/> |XSD:token  <br/> |obrigatório  <br/> |Indica o tipo de Bitmap, objeto ou tinta metarquivo, EnhMetaFile.  <br/> |Valores do tipo xsd:token.  <br/> |
|MappingMode  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |Especifica o modo de mapeamento de metarquivo. Este atributo só é significativo se os dados externos forem um metarquivo.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |XSD:Double  <br/> |opcional  <br/> |Especifica a altura do objeto em unidades de página. Este atributo só é significativo se os dados externos são um objeto incorporado do OLE2.  <br/> |Valores do tipo xsd:double.  <br/> |
|ObjectType  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Um indicador de inteiro do tipo de objeto. Usado quando o tipo estrangeiro é object.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |XSD:Double  <br/> |opcional  <br/> |Especifica a largura do objeto em unidades de página. Este atributo só é significativo se os dados externos são um objeto incorporado do OLE2.  <br/> |Valores do tipo xsd:double.  <br/> |
|ShowAsIcon  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Indica se deve mostrar ou não mostrar dados incorporados como um ícone.  <br/> |Valores do tipo xsd:boolean.  <br/> |
   

