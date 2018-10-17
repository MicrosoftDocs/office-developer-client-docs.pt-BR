---
title: Elemento EventItem (EventList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula um código de evento.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394395"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>Elemento EventItem (EventList_Type complexType) ('Visio XML')

Encapsula um código de evento.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Contém um elemento **EventItem** para cada evento ao qual um objeto deve responder.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Ação  <br/> |xsd:unsignedShort  <br/> |obrigatório  <br/> |Especifica o código de ação do elemento pai **EventItem**.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|Habilitado  <br/> |xsd:boolean  <br/> |opcional  <br/> |Representa um sinalizador que indica se o evento está ativado ou desativado.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |obrigatório  <br/> |Um código que indica o evento que aciona o complemento.  <br/> |Valores do tipo xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A ID do evento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Destino  <br/> |xsd:string  <br/> |obrigatório  <br/> |Especifica o destino de um evento.  <br/> |Valores do tipo xsd:string.  <br/> |
|TargetArgs  <br/> |xsd:string  <br/> |obrigatório  <br/> |Especifica uma cadeia de caracteres que contém os argumentos a serem enviados para o destino de um evento.  <br/> |Valores do tipo xsd:string.  <br/> |
   

