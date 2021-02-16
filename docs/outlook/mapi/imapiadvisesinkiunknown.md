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
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409563"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementa um objeto sink de aviso para manipular a notificação. Um ponteiro para um objeto sink de aviso é passado em uma chamada para o método **Advise** de um provedor de serviços, o mecanismo usado para registrar para notificação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Exposto por:  <br/> |Avisar objetos sink  <br/> |
|Implementado por:  <br/> |Aplicativos cliente e MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços e MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Responde a uma notificação executando uma ou mais tarefas. As tarefas executadas dependem do tipo de evento e do objeto que gera a notificação.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

