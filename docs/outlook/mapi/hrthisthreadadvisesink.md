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
ms.openlocfilehash: 3df5e012867623d1c5e8fb5c3c93103548ab97be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588381"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um coletor de advise que dispõe de um coletor advise existente para a segurança do thread. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parâmetros

 _lpAdviseSink_
  
> [in] Ponteiro para o coletor de eventos advise para ser quebradas. 
    
 _lppAdviseSink_
  
> [out] Ponteiro para um ponteiro para um novo coletor de advise que envolve o coletor de eventos advise apontado pelo parâmetro _lpAdviseSink_ . 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

A finalidade do wrapper é certificar-se de que a notificação é chamada no mesmo thread que a chamada de função **HrThisThreadAdviseSink** . Essa função é usada para proteger os retornos de chamada de notificação que devem ser executado em um determinado segmento. 
  
Aplicativos cliente devem usar **HrThisThreadAdviseSink** para restringir quando as notificações são geradas, ou seja, quando chamadas forem feitas para o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do objeto coletor advise passado pelo cliente em uma **anterior Advise **chamada. Se as notificações são permitidas a serem gerados arbitrariamente uma implementação de notificação pode forçar um cliente em operação multithreaded quando que não ser apropriada. Por exemplo, um cliente pode usar uma biblioteca, como um das bibliotecas de classes do Microsoft Foundation, que não oferece suporte a chamadas multithread. Notificação em um segmento diferente tornaria tal um cliente difícil testar e propenso a erros. 
  
 **HrThisThreadAdviseSink** certifica-se de que as chamadas **OnNotify** ocorrem apenas nesses momentos apropriado: 
  
- Durante o processamento de uma chamada para qualquer método MAPI. 
    
- Durante o processamento de mensagens do Windows. 
    
Quando **HrThisThreadAdviseSink** é implementado, quaisquer chamadas ao método de **OnNotify** do coletor de advise novo em qualquer segmento fazer com que o método de notificação original a ser executado no thread no qual **HrThisThreadAdviseSink** foi chamado. 
  
Para obter mais informações sobre a notificação e receptores de aviso, consulte a [Notificação de evento em MAPI](event-notification-in-mapi.md) e a [implementação de um objeto coletor de aviso](implementing-an-advise-sink-object.md). 
  

