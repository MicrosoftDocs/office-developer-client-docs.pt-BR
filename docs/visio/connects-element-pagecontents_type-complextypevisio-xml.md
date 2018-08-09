---
title: Conecta o elemento (PageContents_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contém um elemento Connect para cada conexão entre duas formas em um desenho.
ms.openlocfilehash: 93930a8f21f9d250bf24d821b0eeb4036f6fe187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771591"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a>Conecta o elemento (PageContents_Type complexType) ('Visio XML')

Contém um elemento **Connect** para cada conexão entre duas formas em um desenho. 
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |página # XML, master. XML de #  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[MasterContents](mastercontents-elementvisio-xml.md) <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |Especifica as informações sobre as formas em uma página mestra ou desenho de um desenho.  <br/> |
|[PageContents](pagecontents-elementvisio-xml.md) <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |Especifica as informações sobre as formas em uma página mestra ou desenho de um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Connect](connect-element-connects_type-complextypevisio-xml.md) <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
			Representa uma conexão entre duas formas em um desenho, como uma linha e uma caixa em um organograma.
  <br/> |
   
### <a name="attributes"></a>Atributos

Nenhum.
  

