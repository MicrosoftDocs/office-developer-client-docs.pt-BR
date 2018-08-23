---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b9244e28337c74487562ec235f246559a49a390d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573800"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementa um objeto de coletor de eventos advise para tratamento de notificação. Um ponteiro para um objeto de coletor de eventos advise é passado em uma chamada ao método **Advise** de um provedor de serviços, o mecanismo usado para registrar a notificação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos de coletor de eventos de aviso  <br/> |
|Implementada por:  <br/> |Aplicativos cliente e MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Responde a uma notificação, executando uma ou mais tarefas. As tarefas realizadas dependem do tipo de evento e o objeto que gera a notificação.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

