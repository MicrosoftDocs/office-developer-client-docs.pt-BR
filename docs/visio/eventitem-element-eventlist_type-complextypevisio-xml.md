---
title: Elemento EventItem (EventList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula um código de evento.
ms.openlocfilehash: dcdd3aa264e8ddfb1aa6f2e908f1c43a0d470872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771818"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>Elemento EventItem (EventList_Type complexType) ('Visio XML')

Encapsula um código de evento.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Ação  <br/> |XSD:unsignedShort  <br/> |obrigatório  <br/> |Especifica o código de ação do elemento **EventItem** pai.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|Habilitado  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Representa um sinalizador que indica se o evento está habilitado ou desabilitado.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|EventCode  <br/> |XSD:unsignedShort  <br/> |obrigatório  <br/> |Um código que indica o evento que dispara o complemento.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A ID do evento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Destino  <br/> |XSD: String  <br/> |obrigatório  <br/> |Especifica o destino de um evento.  <br/> |Valores do tipo xsd: String.  <br/> |
|TargetArgs  <br/> |XSD: String  <br/> |obrigatório  <br/> |Especifica uma cadeia de caracteres que contém os argumentos a serem enviados para o destino de um evento.  <br/> |Valores do tipo xsd: String.  <br/> |
   

