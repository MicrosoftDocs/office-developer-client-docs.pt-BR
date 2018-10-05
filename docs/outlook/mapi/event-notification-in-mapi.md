---
title: Notificação de evento em MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 30d4ad5e0fc1ecdc4c8eb06f75d39e38dd481269
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389971"
---
# <a name="event-notification-in-mapi"></a>Notificação de evento em MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notificação de evento é a comunicação de informações entre dois objetos MAPI. Por meio de um dos objetos, um provedor de cliente ou serviço registra para a notificação de uma alteração ou erro, chamados de um evento, que pode ocorrer no outro objeto. Depois que o evento ocorre, o primeiro objeto é notificado da alteração ou erro. O objeto que receber a notificação é chamado o coletor de eventos advise; o objeto responsável por notificação é chamado a fonte advise.
  
Existem três tipos de advise objetos coletor de eventos (todos os tipos são objetos MAPI padrão):
  
- Aconselhe os objetos de coletor de eventos.   
- Objetos de coletor de eventos de aviso de formulário.  
- Exibir objetos de coletor de eventos de aviso.
    
Aconselhe os objetos de coletor de eventos são o tipo mais comum. Receptores são geralmente implementados pelos aplicativos de cliente para receber o catálogo de endereços e notificações de repositório de mensagens e suporte de aviso o [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interface. **IMAPIAdviseSink** contém um único método, [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). Receptores são menos comuns; de aviso de formulário e modo de exibição eles são implementados para receber notificações sobre alterações formulários personalizados. Suporte de receptores de aviso de formulário a [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) receptores de suporte de aviso de interface e exibir o [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interface. Porque os objetos de coletor de eventos de aviso de padrão de implementar a maioria dos clientes, suponha que as discussões sobre notificações se relacionam com o catálogo de endereços e notificações de repositório de mensagens em vez de notificações de formulários. Para obter mais informações sobre as notificações de formulários, consulte [à escrita de código de servidor de formulário](writing-form-server-code.md)e [Notificações de formulários de MAPI](mapi-forms-notifications.md) .
  
Aconselhe os objetos são implementados por provedores de serviços e MAPI de origem. Nem todos os provedores de serviço oferecem suporte a notificação de evento; é opcional, mas altamente recomendado. Endereço e armazenamento de mensagens do livro provedores geralmente notificações de objeto do suporte em vários dos seus objetos e as notificações de tabela em seus conteúdos e tabelas de hierarquias. Provedores de transporte não oferecem suporte a notificações diretamente; contam com os métodos alternativos de comunicação com os clientes.
  
Diferentemente advise PIAs, aconselhe os objetos de origem não são um único tipo de objeto MAPI. Muitos objetos MAPI, como repositórios de mensagem e tabelas, podem levar o papel de origem advise. Uma fonte de advise é qualquer objeto MAPI que faz o seguinte:
  
- Implementa um método **Advise** para receber os registros de notificação. 
    
- Implementa um método **Unadvise** para receber cancelamentos de notificação. 
    
- Gera notificações do tipo apropriado aos objetos advise apropriado coletor de eventos que foram registrados chamando os métodos **IMAPIAdviseSink::OnNotify** . 
    
Objetos de coletor chamar **Advise** quando eles desejam registrar para uma notificação, na maioria dos casos, passando o identificador de entrada do objeto com o qual registro deve ocorrer e **Unadvise** quando eles desejam Cancelar de aviso de clientes que implementam o Registro. Clientes passam um parâmetro para **Advise** que indica qual dos vários tipos de eventos que eles desejam monitorar. **Advise** retorna um número diferente de zero que representa uma conexão bem-sucedida entre o coletor de eventos advise e advise fonte. 
  
Antes de chamar **Advise**, clientes podem determinar se um provedor de armazenamento de mensagens oferece suporte a notificação, verificando o sinalizador STORE_NOTIFY_OK definido no **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) da loja mensagem propriedade. Há um meio para clientes determinar antecipadamente ou não um provedor de catálogo de endereços dá suporte a notificações. Os clientes devem tentar registrar e se a tentativa falhar, eles supõem notificações não são suportadas.
  
Quando ocorre um evento para o qual um cliente foi registrado, a fonte advise notifica o coletor de eventos advise chamando seu método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) com uma estrutura de dados de notificação que contém informações sobre o evento. Implementação de um advise do coletor de **OnNotify** pode executar tarefas em resposta à notificação, como atualização de dados na memória ou atualizando uma exibição da tela. 
  
Provedores de serviço podem implementar o suporte para notificações manualmente ou aproveitar a Ajuda fornecida nos três métodos de **IMAPISupport** : [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)e [IMAPISupport::Notify ](imapisupport-notify.md). Os métodos **Subscribe** e o **cancelamento da assinatura** lidar com o registro de notificação e cancelamento do registro para provedores; o método **Notify** manipula notificações de envio quando apropriado. 
  
Para usar os métodos do objeto de suporte para o registro de notificação, provedores de serviços de chamada [IMAPISupport::Subscribe](imapisupport-subscribe.md) nos seus métodos **Advise** e passarem para **inscrever-se** o ponteiro do coletor de eventos advise que clientes passam para **Advise**. Se um identificador de entrada é passado como um parâmetro de entrada para especificar uma fonte de advise, provedores de serviços convertê-lo a uma chave binária. **Inscrever-se** cria um número exclusivo de conexão e é esse número que retornam de provedores de serviços aos clientes. Provedores de serviços podem liberar o cliente ponteiro de objeto de coletor de eventos de aviso a qualquer momento após a chamada **Advise** foi concluída. 
  
Quando clientes chama **Unadvise** para cancelar um registro, provedores de serviços de qualquer um dos diminuição a contagem de referência no cliente do ponteiro coletor de eventos de aviso ou ligue para o **cancelamento da assinatura** para fazer o mesmo. 
  
Quando é hora de gerar uma notificação, provedores de serviços de executam qualquer processamento interno que se refere à notificação e inicializa uma estrutura de [notificação](notification.md) , definindo todos os seus membros não utilizados como zero. Essa técnica para inicializar a estrutura de **notificação** pode ajudar os clientes a criar menor, mais rápido e menos propenso implementações de **OnNotify** . 
  
A ilustração a seguir mostra a comunicação entre os objetos de coletor de eventos de aviso, o aviso de objetos source e MAPI. MAPI está envolvido somente quando a fonte de advise chama os métodos de **IMAPISupport** para suporte de notificação. 
  
**Event notification calls**
  
![Chamadas de notificação de evento] (media/amapi_51.gif "Chamadas de notificação de evento")
  
A classe MFCMAPI **CAdviseSink** (usando os arquivos AdviseSink.h e AdviseSink.cpp) implementa o objeto coletor de eventos de advise para todas as chamadas para **Advise**. Para obter mais informações sobre MFCMAPI, consulte [MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md) e [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

