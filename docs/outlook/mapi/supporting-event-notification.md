---
title: Suporte à notificação de eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 45bfe9f9314a154bd5f096ac20f76f6bf4f259c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770512"
---
# <a name="supporting-event-notification"></a>Suporte à notificação de eventos

  
  
**Aplica-se a**: Outlook 
  
Como suporte a notificação de evento pode ser complicado, MAPI fornece três métodos de objeto de suporte que implementem as partes mais difíceis do processo. Esses métodos funcionam como uma unidade e um provedor deve usar todos os três ou nenhum deles.
  
Métodos de suporte a MAPI usam chaves de notificação para gerenciar as conexões entre receptores de advise e os objetos que geram as notificações. Uma chave de notificação é uma estrutura [NOTIFKEY](notifkey.md) que contém dados binários que identifica um objeto através dos processos. Uma chave de notificação geralmente é copiada do identificador de entrada de longo prazo do objeto de origem advise. Se o cliente tem fornecido um identificador de entrada na chamada a **Advise**, você pode usá-lo para a chave de notificação. Se o parâmetro _lpEntryID_ **Advise** é NULL, use o identificador de entrada do objeto container possíveis mais externa, como o armazenamento de mensagens. 
  
Para usar os métodos de suporte, chame [IMAPISupport::Subscribe](imapisupport-subscribe.md) sempre que um cliente chama o método **Advise** para registrar para uma notificação. Alocar uma estrutura [NOTIFKEY](notifkey.md) e crie uma chave exclusiva de notificação para seu objeto de origem advise. Por exemplo, um provedor de armazenamento de mensagem que será solicitado para notificar um cliente quando uma mensagem é recebida em uma pasta particular cria uma chave de notificação para essa pasta. Coletor de eventos de aviso de passagem um ponteiro para a estrutura **NOTIFKEY** na chamada a **Subscribe** junto com um ponteiro para o cliente. **Inscrever-se** chama o método de [AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) do coletor de eventos advise para incrementar sua contagem de referência e MAPI retém o ponteiro até que o registro será cancelado. 
  
Você pode passar o sinalizador NOTIFY_SYNC para **inscrever-se** à solicitação **Notify** se comportam de maneira síncrona e não o retorno até que ele tornou todas as chamadas para os métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) registrado receptores de aviso. Defina esse sinalizador apenas para seu próprio uso interno. Não defina-lo ao responder a um cliente **Advise** chamada. Notificação de evento entre clientes e provedores é sempre assíncrona. Ou seja, a MAPI garante a que a chamada durante o qual um evento acontece irá retornar ao cliente antes que qualquer uma das chamadas **OnNotify** sejam feita. 
  
Se você definir o sinalizador NOTIFY_SYNC, não faça qualquer alteração dos objetos advise coletor de eventos e não passar um coletor de advise wrapper criado por [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para **inscrever-se**. **HrThisThreadAdviseSink** cria uma versão de thread-safe do coletor de eventos de um advise para ser usado com apenas a notificação assíncrona. 
  
Se um coletor de advise registrado para notificação síncrona retorna de **OnNotify** com o sinalizador CALLBACK_DISCONTINUE definido, o [IMAPISupport::Notify](imapisupport-notify.md) define o sinalizador NOTIFY_CANCELED e retorna sem fazer quaisquer chamadas para **OnNotify**. 
  
Depois que **Subscribe** tiver retornado, você não terá mais necessidade mantenha sua cópia do coletor de eventos de aviso do cliente. Chame o método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberá-la. **Inscrever-se** retorna um número diferente de zero conexão que você deve retornar ao cliente. O número de conexão representa o vínculo entre a fonte de advise e o coletor de eventos advise. Permanece válido até que o cliente faz uma chamada bem sucedida a **Unadvise**. 
  
Quando o cliente estiver pronto para cancelar um registro, ele chama o método **Unadvise** . Passe o número de conexão da chamada **Unadvise** para [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md). **Cancelar inscrição** chama o método de **IUnknown:: Release** do coletor de eventos advise. Assim como acontece com **Advise** e **Unadvise**, chamadas para **inscrever-se** e o **cancelamento da assinatura** devem ser combinadas. Você deve fazer uma chamada de **cancelamento da assinatura** para cada chamada feita para **inscrever-se**. No entanto, você não precisará chamar **Subscribe** toda vez que seu método **Advise** é chamado. Por outro lado, você poderá chamá-lo para Configurando notificações internas. 
  
Quando um evento ocorre, alocar uma ou mais estruturas de [notificação](notification.md) do tipo apropriado para o evento e chame [IMAPISupport::Notify](imapisupport-notify.md). **Notificar** gera uma notificação para cada coletor de eventos registrados advise. Você deve definir todos os membros não usados da estrutura de [notificação](notification.md) como zero. Essa técnica para inicializar a estrutura de **notificação** pode ajudar os clientes a criar menor, mais rápido e menos propenso implementações de **OnNotify** . 
  
Observe que uma estrutura de **notificação** separada é necessária para cada evento, mesmo para vários eventos do mesmo tipo. Por exemplo, se três clientes registrados para fins de notificação de tabela em uma tabela específica e cinco linhas são adicionadas à tabela, você deverá criar estruturas de cinco **OBJECT_NOTIFICATION** da sua chamada **Notify** . Uma notificação de lote como isso resulta em desempenho melhor do que chamar **Notify** cinco vezes. Para cada chamada **Notify** , MAPI chama o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos cada advise registrados. Se houver não registrado receptores de aviso MAPI ignora a chamada. 
  
Provedores de serviços que enviar notificações em lote devem solicitá-los para que eles podem ser interpretados a primeira notificação para o último. Essa ordenação é especialmente necessária quando um lote de notificação contém uma série de eventos, como TABLE_ROW_ADDED com um evento que se refere a uma linha anterior que foi adicionada no evento outro no mesmo lote.
  
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

