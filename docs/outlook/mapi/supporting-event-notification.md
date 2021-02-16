---
title: Suporte à notificação de evento
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
# <a name="supporting-event-notification"></a>Suporte à notificação de evento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como o suporte à notificação de evento pode ser complicado, o MAPI fornece três métodos de objeto de suporte que implementam as partes mais difíceis do processo. Esses métodos funcionam como uma unidade, e um provedor deve usar todos os três ou nenhum deles.
  
Os métodos de suporte MAPI usam chaves de notificação para gerenciar as conexões entre os sinks de aviso e os objetos que geram as notificações. Uma chave de notificação é [uma estrutura NOTIFKEY](notifkey.md) que contém dados binários que identificam um objeto entre processos. Uma chave de notificação normalmente é copiada do identificador de entrada de longo prazo do objeto de origem de aviso. Se o cliente tiver fornecido um identificador de entrada na chamada para **Aviso,** você poderá usá-lo para a chave de notificação. Se o  _parâmetro lpEntryID_ para **Advise** for NULL, use o identificador de entrada do objeto de contêiner mais externo possível, como o armazenamento de mensagens. 
  
Para usar os métodos de suporte, chame [IMAPISupport::Subscribe](imapisupport-subscribe.md) sempre que um cliente chamar o método **Advise** para se registrar para uma notificação. Aloce uma [estrutura NOTIFKEY](notifkey.md) e crie uma chave de notificação exclusiva para o objeto de origem de aviso. Por exemplo, um provedor de armazenamento de mensagens que é solicitado a notificar um cliente quando uma mensagem é recebida em uma pasta específica cria uma chave de notificação para essa pasta. Passe um ponteiro para a **estrutura NOTIFKEY** na chamada para Se **inscrever** junto com um ponteiro para o cliente do sink de consultoria. **Subscribe** calls the advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method to increment its reference count and MAPI retains the pointer until the registration is canceled. 
  
Você pode passar o sinalizador  NOTIFY_SYNC para  Assinar para solicitar que a notificação se comporte de forma síncrona e não retorne até que ele tenha feito todas as chamadas para os métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de sinks de aviso registrados. De definir esse sinalizador somente para seu próprio uso interno. Não de definida quando você responder a uma chamada de **Advise do** cliente. A notificação de evento entre clientes e provedores é sempre assíncrona. Ou seja, o MAPI garante que a chamada durante a qual um evento ocorre retornará ao cliente antes que qualquer uma das chamadas **OnNotify** seja feita. 
  
Se você definir o sinalizador NOTIFY_SYNC, não faça alterações em nenhum dos objetos sink de consultoria e não passe um invólucro de alerta criado por [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para **assinar.** **HrThisThreadAdviseSink** cria uma versão thread-safe de um evento de aviso a ser usado somente com notificação assíncrona. 
  
Se um evento de aviso registrado para notificação síncrona retornar de **OnNotify** com o sinalizador CALLBACK_DISCONTINUE definido, [IMAPISupport::Notify](imapisupport-notify.md) define o sinalizador NOTIFY_CANCELED e retorna sem fazer chamadas para **OnNotify**. 
  
Depois **que** Subscribe tiver retornado, você não terá mais a necessidade de manter sua cópia do sink de consultoria do cliente. Chame seu [método IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberá-lo. **Subscribe** retorna um número de conexão que você deve retornar para o cliente. O número de conexão representa o vínculo entre a fonte de consultoria e o sink de consultoria. Ele permanece válido até que o cliente faça uma chamada bem-sucedida para **Unadvise**. 
  
Quando o cliente estiver pronto para cancelar um registro, ele chamará o **método Unadvise.** Passe o número de conexão da **chamada Unadvise** para [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md). **Unsubscribe** calls the advise sink's **IUnknown::Release** method. Assim como **com Advise** e **Unadvise**, as chamadas para **Assinar** e **Cancelar** Assinatura devem ser emparelhadas. Você deve fazer uma chamada para **cancelar a assinatura** de cada chamada feita para **assinar.** No entanto, você não precisa chamar **Subscribe** sempre que o **método Advise** for chamado. Por outro lado, você pode chamá-lo para configurar notificações internas. 
  
Quando ocorrer um evento, aloce uma ou mais estruturas [de](notification.md) NOTIFICAÇÃO do tipo apropriado para o evento e chame [IMAPISupport::Notify](imapisupport-notify.md). **A** notificação gera uma notificação para cada pia de aviso registrado. Você deve definir todos os membros não em uso da estrutura [NOTIFICATION](notification.md) como zero. Essa técnica para inicializar a estrutura **NOTIFICATION** pode ajudar os clientes a criar implementações **OnNotify** menores, mais rápidas e menos propensas a erros. 
  
Observe que uma estrutura **DE NOTIFICAÇÃO** separada é necessária para cada evento, mesmo para vários eventos do mesmo tipo. Por exemplo, se três clientes são registrados para notificação de tabela em uma tabela  específica e cinco linhas são adicionadas à tabela, você deve criar cinco estruturas de OBJECT_NOTIFICATION para sua chamada de **notificação.** Uma notificação em lote, como essa, resulta em melhor desempenho do que chamar o **Notify** cinco vezes. Para cada **chamada de** notificação, MAPI chama o [método IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de cada pia de aviso registrado. Se não houver nenhum pia de alerta registrado, o MAPI ignorará a chamada. 
  
Os provedores de serviços que enviam notificações em lote devem ordenar para que possam ser interpretados da primeira para a última. Essa ordenação é especialmente necessária quando um lote de notificação contém uma série de eventos, como TABLE_ROW_ADDED com um evento que se refere a uma linha anterior que foi adicionada em outro evento no mesmo lote.
  
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

