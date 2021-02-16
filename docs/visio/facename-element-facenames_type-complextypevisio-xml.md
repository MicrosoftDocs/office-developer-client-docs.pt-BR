---
title: Elemento FaceName (FaceNames_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contém informações sobre uma fonte.
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541012"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a>Elemento FaceName (FaceNames_Type complexType) (XML do Visio)

Contém informações sobre uma fonte.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Contém uma coleção de elementos **FaceName**.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|CharSets  <br/> |xsd:string  <br/> |opcional  <br/> |Os conjuntos de caracteres compatíveis com a fonte.  <br/> |Valores do tipo xsd:string.  <br/> |
|Sinalizadores  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Sinalizadores que indicam o seguinte: fonte ausente, fonte padrão, fonte asiática, fonte complexa, fonte vertical e tipo de fonte.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|NameU  <br/> |xsd:string  <br/> |obrigatório  <br/> |O nome da fonte como uma cadeia de caracteres UTF-16 Unicode.  <br/> ||
|Panos  <br/> |xsd:string  <br/> |opcional  <br/> |A assinatura panose da fonte. Panose é um sistema de classificação de tipos de fonte que as categoriza com base nas características visuais.  <br/> |Valores do tipo xsd:string.  <br/> |
|UnicodeRanges  <br/> |xsd:string  <br/> |opcional  <br/> |Os intervalos Unicode compatíveis com a fonte.  <br/> |Valores do tipo xsd:string.  <br/> |
   

