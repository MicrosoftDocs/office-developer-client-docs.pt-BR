---
title: Elemento do Windows ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contém os elementos de janela para um documento.
ms.openlocfilehash: 70746ccfa2d99a9fdd5b3a91320c9372aa233c7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773280"
---
# <a name="windows-element-visio-xml"></a>Elemento do Windows ('Visio XML')

Contém os elementos de **janela** para um documento. 
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Windows.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

Nenhum.
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Representa uma janela aberta em uma estância do Microsoft Visio.
  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Propriedades ClientHeight  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |Representa a dimensão de altura de uma área de exibição  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|ClientWidth  <br/> |XSD:unsignedShort  <br/> |opcional  <br/> |Representa a dimensão de largura de uma área de exibição  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
   

