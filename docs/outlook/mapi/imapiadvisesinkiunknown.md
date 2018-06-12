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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766924"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink: IUnknown

  
  
**Aplica-se a**: Outlook 
  
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

