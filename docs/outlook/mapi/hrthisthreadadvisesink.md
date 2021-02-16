---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427723"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um sink de aconselhagem que envolve um sink de aconselhação existente para segurança de thread. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parâmetros

 _lpAdviseSink_
  
> [in] Ponteiro para o sink advise a ser empacotado. 
    
 _lppAdviseSink_
  
> [out] Ponteiro para um ponteiro para um novo sink advise que quebra o sink advise apontado pelo parâmetro _lpAdviseSink._ 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

O objetivo do wrapper é garantir que a notificação seja chamada no mesmo thread que chamou a **função HrThisThreadAdviseSink.** Essa função é usada para proteger retornos de chamada de notificação que devem ser executados em um thread específico. 
  
Os aplicativos cliente devem usar **HrThisThreadAdviseSink** para restringir quando as notificações são geradas, ou seja, quando as chamadas são feitas para o  método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do objeto sink de aviso passado pelo cliente em uma chamada de Aviso anterior. Se as notificações têm permissão para serem geradas arbitrariamente, uma implementação de notificação pode forçar um cliente em uma operação multithread quando isso não seria apropriado. Por exemplo, um cliente pode usar uma biblioteca, como uma das Bibliotecas de Classes do Microsoft Foundation, que não dá suporte a chamadas multithread. A notificação em um thread diferente dificulta o teste de um cliente e fica propenso a erros. 
  
 **HrThisThreadAdviseSink** garante que as chamadas **OnNotify** ocorram apenas nestes horários apropriados: 
  
- Durante o processamento de uma chamada para qualquer método MAPI. 
    
- Durante o processamento de mensagens do Windows. 
    
Quando **HrThisThreadAdviseSink** é implementado, todas as chamadas para o novo método **OnNotify** do sink de aviso em qualquer thread faz com que o método de notificação original seja executado no thread no qual **HrThisThreadAdviseSink** foi chamado. 
  
For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md). 
  

