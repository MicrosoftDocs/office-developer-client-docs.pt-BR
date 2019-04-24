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
  
A notificação de eventos é a comunicação de informações entre dois objetos MAPI. Por meio de um dos objetos, um cliente ou provedor de serviços registra para notificação de uma alteração ou erro, chamada de evento, que pode ocorrer no outro objeto. Após o evento ocorrer, o primeiro objeto é notificado da alteração ou erro. O objeto que recebe a notificação é chamado de coletor de aviso; o objeto responsável pela notificação é chamado de fonte de aviso.
  
Há três tipos de objetos de coletor de aviso (todos os tipos são objetos MAPI padrão):
  
- Avisar objetos de coletor.   
- Objetos do coletor de aviso de formulário.  
- Exibir objetos do coletor de aviso.
    
Os objetos de coletor de aviso são o tipo mais comum. Os coletores de aviso geralmente são implementados por aplicativos cliente para receber notificações de catálogo de endereços e repositório de mensagens e dão suporte à interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) . **IMAPIAdviseSink** contém um único método, [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md). Os coletores de aviso de formulário e de exibição são menos comuns; Eles são implementados para receber notificações sobre alterações em formulários personalizados. Coletores de aviso de formulário suportam a interface [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) e os coletores de aviso de exibição dão suporte à interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) . Como a maioria dos clientes implementam objetos de coletor de aviso padrão, considere que as discussões de notificações se relacionam às notificações de catálogo de endereços e de mensagens, em vez de notificações de formulários. Para obter mais informações sobre notificações de formulários, consulte [MAPI Forms Notifications](mapi-forms-notifications.md) e [Writing Form Server Code](writing-form-server-code.md).
  
Os objetos de origem de aviso são implementados por provedores de serviço e por MAPI. Nem todos os provedores de serviços dão suporte à notificação de eventos; é opcional, mas é altamente recomendável. O repositório de mensagens e os provedores de catálogo de endereços geralmente dão suporte a notificações de objeto em vários de seus objetos e notificações de tabela em suas tabelas de conteúdo e hierarquia. Os provedores de transporte não dão suporte a notificações diretamente; Eles dependem de métodos alternativos de comunicação com clientes.
  
Ao contrário dos coletores de aviso, os objetos de origem de aviso não são um tipo exclusivo de objeto MAPI. Muitos objetos MAPI, como repositórios de mensagens e tabelas, podem assumir a função da fonte de aviso. Uma fonte de aviso é qualquer objeto MAPI que faz o seguinte:
  
- Implementa um método **Advise** para receber registros de notificação. 
    
- Implementa um método **Unadvise** para receber cancelamentos de notificação. 
    
- Gera notificações do tipo apropriado para os objetos de coletor de aviso apropriados que foram registrados chamando seus métodos **IMAPIAdviseSink:: OnNotify** . 
    
Os clientes que implementam os objetos **** de coletor de aviso de chamada avisam quando querem se registrar em uma notificação, na maioria dos casos, passando o identificador de entrada do objeto com o qual o registro deve ocorrer e **Unadvise** quando deseja cancelar o registro. Os clientes passam um parâmetro para **avisar** que indica quais dos vários tipos de eventos que desejam monitorar. **Advise** retorna um número diferente de zero que representa uma conexão bem-sucedida entre o coletor de aviso e a fonte de aviso. 
  
Antes de chamar **avisar**, os clientes podem determinar se um provedor de repositório de mensagens oferece suporte à notificação verificando se o sinalizador STORE_NOTIFY_OK está definido na **PR_STORE_SUPPORT_MASK** do repositório de mensagens ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) Propriedades. Não há uma maneira de os clientes determinarem com antecedência se um provedor de catálogo de endereços oferece ou não suporte a notificações. Os clientes devem tentar registrar e, se a tentativa falhar, eles podem supor que as notificações não são suportadas.
  
Quando um evento para o qual um cliente registrou ocorre, a fonte de aviso notifica o coletor de aviso chamando o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) com uma estrutura de dados de notificação que contém informações sobre o evento. Uma implementação do onNotify do **** coletor de avisos pode executar tarefas em resposta à notificação, como atualizar dados na memória ou atualizar uma exibição de tela. 
  
Os provedores de serviços podem implementar o suporte para notificações manualmente ou aproveitar a ajuda fornecida em três métodos do **IMAPISupport** : [IMAPISupport:: Subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)e [IMAPISupport:: Notify ](imapisupport-notify.md). Os métodos de **assinatura** e cancelamento de **assinatura** cuidam do registro e cancelamento de registro de notificações para provedores o método **Notify** trata de enviar notificações quando apropriado. 
  
Para usar os métodos de objeto de suporte para registro de notificação, os provedores de serviços chamam [IMAPISupport:: inscrever-se](imapisupport-subscribe.md) em seus métodos de **aviso** e passar para **inscrever** o ponteiro do coletor de aviso que os clientes passam para **avisar**. Se um identificador de entrada for passado como um parâmetro de entrada para especificar uma fonte de aviso, os provedores de serviços o converterão em uma chave binária. **Subscribe** cria um número de conexão exclusivo e é esse número que os provedores de serviço retornam aos clientes. Os provedores de serviços podem liberar o ponteiro do objeto do coletor de aviso do cliente a qualquer momento depois que a chamada de **aviso** tiver sido concluída. 
  
Quando os clientes chamam o **aviso** para cancelar um registro, os provedores de serviços decrementam a contagem de referência no ponteiro de coletor de aviso do cliente ou solicitam o cancelamento da **assinatura** para fazer o mesmo. 
  
Quando é hora de gerar uma notificação, os provedores de serviços realizam qualquer processamento interno relacionado à notificação e Inicializa uma estrutura de [notificação](notification.md) definindo todos os membros não usados como zero. Essa técnica de inicialização da estrutura de **notificação** pode ajudar os clientes a criar implementações de OnNotify, **** menores, mais rápidas e menos sujeitas a erros. 
  
A ilustração a seguir mostra a comunicação entre os objetos do coletor de aviso, os objetos de origem do aviso e o MAPI. O MAPI é envolvido somente quando a fonte de aviso chama os métodos **IMAPISupport** para obter suporte para notificação. 
  
**Event notification calls**
  
![Chamadas de notificação de eventos] (media/amapi_51.gif "Chamadas de notificação de eventos")
  
A classe MFCMAPI **CAdviseSink** (usando os arquivos AdviseSink. h e AdviseSink. cpp) implementa o objeto de coletor de aviso para todas as chamadas para **Advise**. Para obter mais informações sobre o MFCMAPI, consulte [MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md) e [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

