---
title: Elemento HeaderFooterFont (HeaderFooter_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Especifica a fonte usada para o texto de cabeçalho e rodapé.
ms.openlocfilehash: 249040702b1594cc650ccf1304ed7c1c79581ea3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771999"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>Elemento HeaderFooterFont (HeaderFooter_Type complexType) ('Visio XML')

Especifica a fonte usada para o texto de cabeçalho e rodapé.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Contém os elementos de cabeçalho e rodapé de um documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> |Especifica o conjunto de caracteres da fonte. Equivalente ao campo LOGFONTlfCharSet GDI.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> |Especifica a precisão de corte da fonte. Equivalente ao campo LOGFONTlfClipPrecision GDI.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Escape  <br/> |XSD:int  <br/> |opcional  <br/> |Especifica o atributo de escape da fonte. Equivalente ao campo LOGFONTlfEscapement GDI.  <br/> |Valores do tipo xsd:int.  <br/> |
|FaceName  <br/> |XSD: String  <br/> |opcional  <br/> |Contém informações sobre uma fonte.  <br/> |Valores do tipo xsd: String.  <br/> |
|Altura  <br/> |XSD:int  <br/> |opcional  <br/> |Especifica a altura da forma em unidades de desenho.  <br/> |Valores do tipo xsd:int.  <br/> |
|Itálico  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> |Especifica se a fonte está em itálico. Equivalente ao campo LOGFONTlfItalic GDI.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Orientation  <br/> |XSD:int  <br/> |opcional  <br/> |Especifica a orientação da fonte. Equivalente ao campo LOGFONTlfOrientation GDI.  <br/> |Valores do tipo xsd:int.  <br/> |
|OutPrecision  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> |Especifica o atributo de precisão de saída da fonte. Equivalente ao campo LOGFONTlfOutPrecision GDI.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> |Especifica a densidade e família da fonte. Equivalente ao campo LOGFONTlfPitchAndFamily GDI.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Quality  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> |Especifica a qualidade de saída da fonte. Equivalente ao campo LOGFONTlfQuality GDI.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Riscado  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> |Especifica se a fonte é uma fonte riscado. Equivalente ao campo LOGFONTlfStrikeOut GDI.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Sublinhado  <br/> |XSD:unsignedByte  <br/> |opcional  <br/> |Especifica se a fonte estiver sublinhada. Equivalente ao campo LOGFONTlfUnderline GDI.  <br/> |Valores do tipo xsd:unsignedByte.  <br/> |
|Peso  <br/> |XSD:int  <br/> |opcional  <br/> |Especifica a espessura da fonte. Equivalente ao campo LOGFONTlfWeight GDI.  <br/> |Valores do tipo xsd:int.  <br/> |
|Largura  <br/> |XSD:int  <br/> |opcional  <br/> |Contém a largura da forma associada em unidades de desenho.  <br/> |Valores do tipo xsd:int.  <br/> |
   

