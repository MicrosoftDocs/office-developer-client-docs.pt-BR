---
title: Elemento HeaderFooterFont (HeaderFooter_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Especifica a fonte utilizada no texto do cabeçalho e do rodapé.
ms.openlocfilehash: b87ba96d551bf943dd330aa428f2c943c9d29269
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541082"
---
# <a name="headerfooterfont-element-headerfooter_type-complextype-visio-xml"></a>Elemento HeaderFooterFont (HeaderFooter_Type complexType) (XML do Visio)

Especifica a fonte utilizada no texto do cabeçalho e do rodapé.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Contém elementos para o rodapé e o rodapé de um documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica o conjunto de caracteres da fonte. Equivalente ao campo GDI LOGLFTlfCharSet.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica a precisão de recorte da fonte. Equivalente ao campo GDI LOGCUNTlfClipPrecision.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Escape  <br/> |xsd:int  <br/> |opcional  <br/> |Especifica o atributo de escape da fonte. Equivalente ao campo GDI LOGLFTlfEscapement.  <br/> |Valores do tipo xsd:int.  <br/> |
|FaceName  <br/> |xsd:string  <br/> |opcional  <br/> |Contém informações sobre uma fonte.  <br/> |Valores do tipo xsd:string.  <br/> |
|Altura  <br/> |xsd:int  <br/> |opcional  <br/> |Especifica a altura da forma em unidades de desenho.  <br/> |Valores do tipo xsd:int.  <br/> |
|Itálico  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica se a fonte está em itálico. Equivalente ao campo GDI LOGLFTlfItalic.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Orientação  <br/> |xsd:int  <br/> |opcional  <br/> |Especifica a orientação da fonte. Equivalente ao campo GDI LOGPOTTlfOrientation.  <br/> |Valores do tipo xsd:int.  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica o atributo de precisão de saída da fonte. Equivalente ao campo GDI LOGLFTlfOutPrecision.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica a pitch e a família da fonte. Equivalente ao campo GDI LOGLFTlfPitchAndFamily.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Qualidade  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica a qualidade de saída da fonte. Equivalente ao campo GDI LOGLFTlfQuality.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica se a fonte é uma fonte em strikeout. Equivalente ao campo GDI LOGLFTlfStrikeOut.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Sublinhado  <br/> |xsd:unsignedByte  <br/> |opcional  <br/> |Especifica se a fonte é sublinhada. Equivalente ao campo GDI LOGLFTlfUnderline.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Peso  <br/> |xsd:int  <br/> |opcional  <br/> |Especifica o peso da fonte. Equivalente ao campo GDI LOG LOGINTlfWeight.  <br/> |Valores do tipo xsd:int.  <br/> |
|Largura  <br/> |xsd:int  <br/> |opcional  <br/> |Contém a largura da forma associada em unidades de desenho.  <br/> |Valores do tipo xsd:int.  <br/> |
   

