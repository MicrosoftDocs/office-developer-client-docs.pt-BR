---
title: Visão geral do desligamento rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Modificado pela última vez: 26 de junho de 2012'
ms.openlocfilehash: 17b1307427af2c35fe9ba8ee40dc78958e6b4a21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766520"
---
# <a name="fast-shutdown-overview"></a>Visão geral do desligamento rápido

**Aplica-se a**: Outlook 
  
Desligamento rápido é um mecanismo para um cliente MAPI iniciar um desligamento rápido do processo do cliente, informando todos os provedores com o qual o cliente tem uma sessão MAPI ativa para salvar os dados e configurações antes do processo de cliente for encerrado. Este tópico descreve o mecanismo básico de desligamento rápido. 

Iniciando no Microsoft Outlook 2010 e agora, incluindo Microsoft Outlook 2013, o subsistema de MAPI fornece o [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) interface. Outlook e outros clientes MAPI podem adotar o desligamento rápido como o mecanismo de padrão para sair do processo de cliente. Uma configuração de nível de usuário no registro do Windows do computador cliente controla a adoção de desligamento rápido para todos os clientes MAPI para o usuário no computador. Para obter detalhes sobre as configurações do registro, consulte [Opções de usuário de desligamento Fast](fast-shutdown-user-options.md).
  
Se um cliente MAPI precisa adotar o desligamento rápido, ela deve usar o **IMAPIClientShutdown: IUnknown** interface. Este é o curso típico de eventos quando o cliente tenta desligar: 
  
1. O cliente MAPI inicia o desligamento chamando o método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) para determinar se o subsistema de MAPI suporta desligamento rápido. 
    
2. O subsistema de MAPI responde com o suporte de desligamento rápido disponível a chamada de **IMAPIClientShutdown::QueryFastShutdown** do cliente usando o procedimento a seguir: 
    
    1. O subsistema de MAPI chama o método de [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para cada provedor MAPI com o qual o processo de cliente MAPI tem uma sessão MAPI ativa, se o provedor tiver implementado o [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) interface. 
        
       > [!NOTE]
       >  O subsistema de MAPI sempre consultas e notifica provedores MAPI por meio do **IMAPIProviderShutdown: IUnknown** interface dentro de cada sessão MAPI na seguinte ordem:
       > 1. Provedores de transporte
       > 2. Provedores de catálogo de endereços
       > 3. Provedores de armazenamento 
    
    2. Dependendo da configuração do registro de desligamento rápido para o usuário no computador cliente, o subsistema de MAPI Especifica que o código de retorno apropriado para **IMAPIClientShutdown::QueryFastShutdown**. O código de retorno é S_OK ou MAPI_E_NO_SUPPORT.
        
    3. O cliente MAPI chama o método de [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) para indicar ao subsistema de MAPI a intenção para serem desligados. 
        
    4. O subsistema de MAPI indica cada provedor MAPI carregado que desligará o cliente MAPI. Para os provedores que tenham implementado o **IMAPIProviderShutdown: IUnknown** interface, o subsistema de MAPI chama o método [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) correspondente. 
        
    5. O cliente MAPI chama o método de [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) para indicar ao subsistema de MAPI que o processo de cliente está deixando imediatamente. 
        
    6. O subsistema de MAPI indica cada provedor MAPI carregado saindo do processo do cliente MAPI. Para os provedores que tenham implementado o **IMAPIProviderShutdown: IUnknown** interface, o subsistema de MAPI chama o método [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) correspondente. Neste ponto, esses provedores MAPI devem verificar se todas as ações necessárias, como a salvando dados e configurações, forem concluídas em preparação para o cliente MAPI imediatamente desconectar todas as referências e sair. 
    
## <a name="see-also"></a>Confira também

- [Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)
- [Opções de usuário do desligamento rápido](fast-shutdown-user-options.md)
- [Práticas recomendadas para o desligamento rápido](best-practices-for-fast-shutdown.md)

