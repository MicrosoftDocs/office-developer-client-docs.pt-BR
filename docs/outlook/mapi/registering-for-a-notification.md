---
title: Registrar-se para receber uma notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5a35add66fb685b3c17464269456edf6b456711e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570209"
---
# <a name="registering-for-a-notification"></a>Registrar-se para receber uma notificação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode registrar para notificações de repositório de catálogo ou mensagem de endereço como parte do seu processo de inicialização.
  
MAPI oferece suporte a notificação no catálogo de endereços, independentemente se qualquer um dos provedores de catálogo de endereços o suporte. Suporte para fins de notificação em repositórios de mensagem depende do provedor de armazenamento de mensagem específica. Para determinar se o provedor de armazenamento de uma determinada mensagem dá suporte a notificações, verifique sua propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Se o armazenamento de mensagens oferece suporte a notificações, será definido o bit STORE_NOTIFY_OK. 
  
Registrar para notificações chamando o método **Advise** do objeto de origem uma advise. Muitos objetos implementam **Advise** e os clientes podem se inscrever com esses objetos de várias maneiras. 
  
 **Para registrar para uma notificação**
  
1. Criar um MAPI objeto coletor de eventos de aviso e incrementar sua contagem de referência.
    
2. Se apropriado, chame [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) para criar um objeto de coletor de eventos de advise que envolve o seu coletor de advise original e solte o coletor de eventos original conselhos.. 
    
3. Ligue para um dos seguintes métodos para concluir o registro **Advise** : 
    
  - Chame [IMAPISession::Advise](imapisession-advise.md) para registrar para notificações de sessão ou para notificações em um objeto de repositório de catálogo ou mensagem de endereço. 
    
  - Chame [IAddrBook::Advise](iaddrbook-advise.md) para registrar para notificações do catálogo de endereços ou para notificações em uma lista de distribuição, contêiner ou usuário de mensagens. 
    
  - Chame [IABLogon::Advise](iablogon-advise.md) para registrar diretamente com um provedor de catálogo de endereços para notificações em uma lista de distribuição, contêiner ou usuário de mensagens. 
    
  - Chame [IMsgStore::Advise](imsgstore-advise.md) para registrar para notificações do repositório de mensagens ou para notificações em uma pasta ou mensagem. 
    
  - Chame [IMSLogon::Advise](imslogon-advise.md) para registrar diretamente com um provedor de armazenamento de mensagem para notificações em uma pasta ou mensagem. 
    
  - Chame [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações de tabela. 
    
4. Armazena em cache o número de conexão retornado da **Advise**.
    
5. Se estiver usando um coletor advise com quebra, liberá-la. Depois que o coletor de eventos com quebra advise é registrado, você não precisa mais dela.
    
Chamar * * IMAPISession::Advise * * permite que você registre para notificações de erro crítico na sessão geral ou para várias notificações em objetos individuais. Sessões de enviar notificações de erro crítico aos clientes conectados ao sessões compartilhadas quando outro cliente usando a sessão compartilhada chama o método [IMAPISession::Logoff](imapisession-logoff.md) . Para registrar para notificações de sessão, passe NULL para o parâmetro do identificador de entrada. Para registrar para notificações de um objeto individual, passe o identificador de entrada do objeto. O método **IMAPISession** encaminha a chamada para o provedor de serviço apropriado, conforme determinado pela parte **MAPIUID** do identificador de entrada. Chamar **IMAPISession::Advise** para registrar para notificações do objeto é mais simples do que chamar o método **Advise** de um provedor de serviços. 
  
Registrando com o catálogo de endereços é semelhante ao Registrando com a sessão. Para registrar para fins de notificação de erro crítico do catálogo de endereços, passe NULL para o identificador de entrada. Para registrar para notificações em um objeto de catálogo de endereço específica, especifique o identificador de entrada apropriada e o evento ou eventos de interesse. Lembre-se de que muitos provedores de catálogo de endereços não oferecem suporte a notificações em objetos individuais. Em vez disso, eles oferecem suporte a notificações de tabela em seus conteúdos e tabelas de hierarquias. 
  
É uma boa prática para liberar o coletor de eventos advise implementar ou criado com [HrAllocAdviseSink](hrallocadvisesink.md) imediatamente após um retorno bem-sucedida de uma chamada **Advise** . Isso ocorre porque é possível para provedores de serviços liberar seu coletor advise após a chamada **Advise** , mas antes de um **Unadvise** chamada é feita. Depois que você concedeu a fonte advise um ponteiro para seu coletor advise e a contagem de referência foi incrementada no coletor de eventos advise, é aconselhável liberá-la, a menos que tenha um longo prazo usar para ela. 
  
> [!NOTE]
> Todos os números de conexão que representam os registros de consultoria válidos não serão liberados até que a chamada **Unadvise** é feita. 
  

