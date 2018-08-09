---
title: Elemento FaceName (FaceNames_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contém informações sobre uma fonte.
ms.openlocfilehash: 8a66d5294e239e4540939cc7053e1f67a777144d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771824"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>Elemento FaceName (FaceNames_Type complexType) ('Visio XML')

Contém informações sobre uma fonte.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contém uma coleção de elementos de **FaceName** .  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|CharSets  <br/> |XSD: String  <br/> |opcional  <br/> |Os conjuntos de caracteres com suporte da fonte.  <br/> |Valores do tipo xsd: String.  <br/> |
|Sinalizadores  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Sinalizadores que indicam o seguinte: ausentes fonte, fonte padrão, fonte asiática, fonte complexa, fonte vertical e tipo de fonte.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|NameU  <br/> |XSD: String  <br/> |obrigatório  <br/> |O nome da fonte como uma cadeia de caracteres Unicode UTF-16.  <br/> ||
|Panos  <br/> |XSD: String  <br/> |opcional  <br/> |A assinatura panose para a fonte. Panose é um sistema de classificação para faces de tipos que categoriza-los com base nas suas características visuais.  <br/> |Valores do tipo xsd: String.  <br/> |
|UnicodeRanges  <br/> |XSD: String  <br/> |opcional  <br/> |Os intervalos de Unicode com suporte da fonte.  <br/> |Valores do tipo xsd: String.  <br/> |
   

