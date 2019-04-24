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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346834"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um coletor de aviso que quebra um coletor de aviso existente para segurança de thread. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parâmetros

 _lpAdviseSink_
  
> no Ponteiro para o coletor de aviso a ser quebrado. 
    
 _lppAdviseSink_
  
> bota Ponteiro para um ponteiro para um novo coletor de aviso que envolve o coletor de avisos apontado pelo parâmetro _lpAdviseSink_ . 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

O objetivo do wrapper é certificar-se de que a notificação é chamada no mesmo thread que chamou a função **HrThisThreadAdviseSink** . Essa função é usada para proteger os retornos de chamada de notificação que devem ser executados em um thread específico. 
  
Os aplicativos cliente devem usar **HrThisThreadAdviseSink** para restringir quando as notificações são geradas, ou seja, quando as chamadas são feitas para o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do objeto de coletor de aviso passado pelo cliente em um **aviso anterior **chamada. Se as notificações tiverem permissão para serem geradas arbitrariamente, uma implementação de notificação poderá forçar um cliente a executar uma operação multithread quando não for apropriado. Por exemplo, um cliente pode usar uma biblioteca, como uma das bibliotecas de classe Microsoft Foundation, que não oferece suporte a chamadas multi-threaded. A notificação em um thread diferente faria com que um cliente fosse difícil de testar e propenso a erros. 
  
 O **HrThisThreadAdviseSink** garante que as chamadas OnNotify ocorram somente nos seguintes horários apropriados: **** 
  
- Durante o processamento de uma chamada para qualquer método MAPI. 
    
- Durante o processamento de mensagens do Windows. 
    
Quando o **HrThisThreadAdviseSink** é implementado, todas as chamadas para o novo método **OnNotify** do coletor de avisos em qualquer thread fazem com que o método de notificação original seja executado no thread no qual o **HrThisThreadAdviseSink** foi chamado. 
  
Para obter mais informações sobre notificações e coletores de aviso, consulte [Event Notification in MAPI](event-notification-in-mapi.md) e [implementar um objeto de coletor de aviso](implementing-an-advise-sink-object.md). 
  

