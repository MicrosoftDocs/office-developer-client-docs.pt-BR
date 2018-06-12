---
title: Elemento de texto (ShapeSheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contém o texto de uma forma.
ms.openlocfilehash: 636f349b0a93719cd157db563b238147af5584cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773105"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a>Elemento de texto (ShapeSheet_Type complexType) ('Visio XML')

Contém o texto de uma forma.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |página # XML, master. XML de #  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
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
|[CP](cp-element-text_type-complextypevisio-xml.md) <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |Marca o início das propriedades de um caractere ou seja executado formatado de acordo com o elemento Char correspondente.  <br/> |
|[FLD](fld-element-text_type-complextypevisio-xml.md) <br/> |[fld_Type](fld_type-complextypevisio-xml.md) <br/> |Indica um ponto de inserção do campo de texto para o elemento do campo correspondente.  <br/> |
|[PP](pp-element-text_type-complextypevisio-xml.md) <br/> |[pp_Type](pp_type-complextypevisio-xml.md) <br/> |Especifica o início das propriedades de um parágrafo é executado.  <br/> |
|[PA](tp-element-text_type-complextypevisio-xml.md) <br/> |[tp_Type](tp_type-complextypevisio-xml.md) <br/> |Especifica o início de propriedades guias executar.  <br/> |
   
### <a name="attributes"></a>Atributos

Nenhum.
  

