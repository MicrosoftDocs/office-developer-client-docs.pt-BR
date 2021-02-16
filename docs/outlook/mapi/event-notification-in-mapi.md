---
title: Notificações de eventos no MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 30d4ad5e0fc1ecdc4c8eb06f75d39e38dd481269
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321390"
---
# <a name="event-notification-in-mapi"></a>Notificações de eventos no MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notificação de evento é a comunicação de informações entre dois objetos MAPI. Por meio de um dos objetos, um cliente ou provedor de serviços registra-se para notificação de uma alteração ou erro, chamada de evento, que pode ocorrer no outro objeto. Depois que o evento ocorre, o primeiro objeto é notificado sobre a alteração ou o erro. O objeto que recebe a notificação é chamado de sink advise; o objeto responsável pela notificação é chamado de fonte de aviso.
  
Há três tipos de objetos sink de alerta (todos os tipos são objetos MAPI padrão):
  
- Aconselhá objetos sink.   
- Form advise sink objects.  
- Exibir objetos de aconselhá-los.
    
Avisar objetos sink são o tipo mais comum. Os sinks de aviso são normalmente implementados por aplicativos cliente para receber notificações do address book e do armazenamento de mensagens e dar suporte à interface [IMAPIAdviseSink : IUnknown.](imapiadvisesinkiunknown.md) **IMAPIAdviseSink** contém um único método, [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). Os sinks de consultoria de formulário e exibição são menos comuns; eles são implementados para receber notificações sobre alterações em formulários personalizados. Os sinks de consultoria de formulário suportam [o IMAPIFormAdviseSink : interface IUnknown](imapiformadvisesinkiunknown.md) e os sinks de alerta de exibição suportam a interface [IMAPIViewAdviseSink : IUnknown.](imapiviewadvisesinkiunknown.md) Como a maioria dos clientes implementa objetos sink de aviso padrão, pressupõe que as discussões de notificações estão relacionadas às notificações do address book e do armazenamento de mensagens, em vez de notificações de formulários. For more information about forms notifications, see [MAPI Forms Notifications](mapi-forms-notifications.md) and [Writing Form Server Code](writing-form-server-code.md).
  
Os objetos de origem de consultoria são implementados por provedores de serviços e por MAPI. Nem todos os provedores de serviços suportam a notificação de evento; é opcional, mas altamente recomendável. Os provedores de armazenamento de mensagens e de agendas geralmente suportam notificações de objeto em vários de seus objetos e notificações de tabela em seus conteúdos e tabelas de hierarquia. Os provedores de transporte não suportam notificações diretamente; eles dependem de métodos alternativos de comunicação com clientes.
  
Ao contrário de aconselhá-los, os objetos de origem de consultoria não são um tipo exclusivo de objeto MAPI. Muitos objetos MAPI, como armazenamentos de mensagens e tabelas, podem assumir a função de fonte de consultoria. Uma fonte de conselhos é qualquer objeto MAPI que faz o seguinte:
  
- Implementa um método **Advise** para receber registros de notificação. 
    
- Implementa um **método Unadvise** para receber cancelamentos de notificação. 
    
- Gera notificações do tipo apropriado para os objetos de pia de aviso apropriados que foram registrados chamando seus métodos **IMAPIAdviseSink::OnNotify.** 
    
Os clientes que implementam o aviso de objetos de pia chamam Aviso quando querem se registrar para uma  notificação, na maioria dos casos, passando o identificador de entrada do objeto com o qual o registro deve ocorrer e Não é provável quando eles querem cancelar o registro.  Os clientes passam um parâmetro **para Advise** que indica qual dos vários tipos de eventos eles querem monitorar. **Advise** retorna um número que não é zero que representa uma conexão bem-sucedida entre o sink de aconselhá-los e a fonte de aconselhação. 
  
Antes de chamar **o Aviso,** os clientes podem determinar se um provedor de repositório de mensagens oferece suporte à notificação verificando se o sinalizador STORE_NOTIFY_OK está definido na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)do repositório de mensagens. Não há como os clientes determinarem com antecedência se um provedor de agendas de endereços oferece suporte ou não a notificações. Os clientes devem tentar se registrar e, se a tentativa falhar, eles podem supor que as notificações não são compatíveis.
  
Quando ocorre um evento para o qual um cliente registrou, a fonte de aviso notifica o sink de aviso chamando seu método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) com uma estrutura de dados de notificação que contém informações sobre o evento. A implementação de **OnNotify** de um evento de aviso pode executar tarefas em resposta à notificação, como atualizar dados na memória ou atualizar uma exibição de tela. 
  
Os provedores de serviços podem implementar o suporte para notificações manualmente ou tirar proveito da ajuda fornecida em três métodos **IMAPISupport:** [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)e [IMAPISupport::Notify](imapisupport-notify.md). Os **métodos Subscribe** e **Unsubscribe** lidam com o registro de notificação e o cancelamento de registro para provedores; o **método Notify** trata do envio de notificações quando apropriado. 
  
To use the support object methods for notification registration, service providers call [IMAPISupport::Subscribe](imapisupport-subscribe.md) in their Advise methods and pass to **Subscribe** the **advise** sink pointer that clients pass to **Advise**. Se um identificador de entrada for passado como um parâmetro de entrada para especificar uma fonte de consultoria, os provedores de serviços o converterão em uma chave binária. **Subscribe** cria um número de conexão exclusivo e é esse número que os provedores de serviços retornam aos clientes. Os provedores de serviços podem liberar o ponteiro do objeto de pia de alerta do cliente a qualquer momento após **a conclusão da chamada Advise.** 
  
Quando os clientes chamam **Unadvise** para cancelar um registro, os provedores de serviços rebaixam a contagem de referência no ponteiro do pia de alerta do cliente ou chamam **Unsubscribe** para fazer o mesmo. 
  
Quando é hora de gerar uma notificação, os provedores de serviços executam [](notification.md) qualquer processamento interno relacionado à notificação e inicializam uma estrutura notification definindo todos os seus membros não em uso como zero. Essa técnica para inicializar a estrutura **NOTIFICATION** pode ajudar os clientes a criar implementações **OnNotify** menores, mais rápidas e menos propensas a erros. 
  
A ilustração a seguir mostra a comunicação entre os objetos de aconselhá-los, avisar objetos de origem e MAPI. MAPI is involved only when the advise source calls the **IMAPISupport** methods for notification support. 
  
**Event notification calls**
  
![Notificação de evento chama chamadas]de(media/amapi_51.gif "notificação de evento")
  
A classe **CAdviseSink** MFCMAPI (usando os arquivos AdviseSink.h e AdviseSink.cpp) implementa o objeto sink advise para todas as chamadas a **Advise**. Para obter mais informações sobre MFCMAPI, consulte [MFCMAPI como um exemplo de](mfcmapi-as-a-code-sample.md) código e [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

