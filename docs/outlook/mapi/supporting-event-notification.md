---
title: Notificação de evento de suporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 83c102c25b17b6769c0c676bbadd874224f75cf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327423"
---
# <a name="supporting-event-notification"></a>Notificação de evento de suporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como a notificação de evento de suporte pode ser complicada, o MAPI fornece três métodos de objeto de suporte que implementam as partes mais difíceis do processo. Esses métodos funcionam como uma unidade, e um provedor deve usar todos os três ou nenhum deles.
  
Os métodos de suporte MAPI usam chaves de notificação para gerenciar as conexões entre os coletores de aviso e os objetos que geram notificações. Uma chave de notificação é uma estrutura [NOTIFKEY](notifkey.md) que contém dados binários que identificam um objeto entre processos. Uma chave de notificação é normalmente copiada do identificador de entrada de longo prazo do objeto de origem de aviso. Se o cliente tiver fornecido um identificador de entrada na chamada para **Advise**, você poderá usá-lo para a chave de notificação. Se o parâmetro _lpEntryID_ como **Advise** for NULL, use o identificador de entrada do objeto Container mais externo possível, como o repositório de mensagens. 
  
Para usar os métodos de suporte, chame [IMAPISupport:: Subscribe](imapisupport-subscribe.md) sempre que um cliente chama seu método **Advise** para se registrar para uma notificação. Aloque uma estrutura [NOTIFKEY](notifkey.md) e crie uma chave de notificação exclusiva para o seu objeto de origem de aviso. Por exemplo, um provedor de armazenamento de mensagens que é solicitado a notificar um cliente quando uma mensagem é recebida em uma determinada pasta cria uma chave de notificação para essa pasta. Passe um ponteiro para a estrutura **NOTIFKEY** na chamada para **inscrever-se** junto com um ponteiro para o coletor de aviso do cliente. **Subscribe** chama o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) do coletor de aviso para incrementar sua contagem de referência e MAPI retém o ponteiro até que o registro seja cancelado. 
  
Você pode passar o sinalizador NOTIFY_SYNC para **inscrever-** se **** para solicitar que notificar o comportamento de forma síncrona e não retornar até que tenha feito todas as chamadas para os métodos [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) dos coletores de aviso registrados. Defina esse sinalizador somente para seu próprio uso interno. Não o defina quando responder a uma chamada de **aviso** de cliente. A notificação de eventos entre clientes e provedores é sempre assíncrona. Ou seja, o MAPI garante que a chamada durante a qual um evento ocorre retornará ao cliente antes que qualquer uma **** das chamadas OnNotify sejam feitas. 
  
Se você definir o sinalizador NOTIFY_SYNC, não faça qualquer alteração em qualquer um dos objetos de coletor de aviso e não passe um coletor de aviso de wrapper criado pelo [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para **se inscrever**. **HrThisThreadAdviseSink** cria uma versão de thread seguro de um coletor de aviso a ser usada somente com a notificação assíncrona. 
  
Se um coletor de aviso registrado para a notificação síncrona **** retornar de OnNotify com o sinalizador CALLBACK_DISCONTINUE definido, [IMAPISupport:: Notify](imapisupport-notify.md) define o sinalizador NOTIFY_CANCELED e retorna sem fazer chamadas **** para OnNotify. 
  
Após a **assinatura** ter sido retornada, você não terá mais a necessidade de manter a sua cópia do coletor de aviso do cliente. Chame seu método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberá-lo. **Subscribe** retorna um número de conexão diferente de zero que você deve retornar ao cliente. O número de conexão representa o link entre a fonte de aviso e o coletor de aviso. Ele permanece válido até que o cliente faça uma chamada bem-sucedida para **Unadvise**. 
  
Quando o cliente está pronto para cancelar um registro, ele chama o método **Unadvise** . Passe o número de conexão da chamada **Unadvise** para [IMAPISupport:: cancelar assinatura](imapisupport-unsubscribe.md). **Cancelar assinatura** chama o método **IUnknown:: Release** do coletor de avisos. Como com **Advise** e **Unadvise**, as chamadas **** para inscrever e **cancelar assinatura** devem estar emparelhadas. Você deve fazer uma chamada para cancelar a **assinatura** de cada chamada feita para **inscrever-** se. No enTanto, não é necessário chamar **inscrever** sempre que o método **Advise** for chamado. Por outro lado, você pode chamá-lo para configurar notificações internas. 
  
Quando ocorre um evento, aloque uma ou mais estruturas de [notificação](notification.md) do tipo apropriado para o evento e chame [IMAPISupport:: Notify](imapisupport-notify.md). **Notificar** gera uma notificação para cada coletor de aviso registrado. Você deve definir todos os membros não utilizados da estrutura de [notificação](notification.md) como zero. Essa técnica de inicialização da estrutura de **notificação** pode ajudar os clientes a criar implementações de OnNotify, **** menores, mais rápidas e menos sujeitas a erros. 
  
Observe que uma estrutura de **notificação** separada é necessária para cada evento, mesmo para vários eventos do mesmo tipo. Por exemplo, se três clientes são registrados para a notificação de tabela em uma tabela específica e cinco linhas são adicionadas à tabela, você deve criar cinco estruturas **OBJECT_NOTIFICATION** para sua chamada de **notificação** . Uma notificação em lotes, como isso resulta em um melhor desempenho **** do que chamar notificar cinco vezes. Para cada chamada de **notificação** , o MAPI chama o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) de cada coletor de aviso registrado. Se não houver nenhum coletor de aviso registrado, o MAPI ignorará a chamada. 
  
Os provedores de serviços que enviam notificações em lote devem solicitar que eles possam ser interpretados da primeira notificação para a última. Essa ordenação é especialmente necessária quando um lote de notificação contém uma série de eventos, como TABLE_ROW_ADDED, com um evento referente a uma linha anterior que foi adicionada a outro evento no mesmo lote.
  
## <a name="see-also"></a>Confira também



[Provedores de serviço MAPI](mapi-service-providers.md)

