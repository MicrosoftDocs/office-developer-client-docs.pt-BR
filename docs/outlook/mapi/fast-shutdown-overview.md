---
title: Visão geral do desligamento rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a7830d73-427c-4f8b-86f4-51e040c142c3
description: 'Última modificação: 26 de junho de 2012'
ms.openlocfilehash: 8c33214b04e7c41eab173196c09f145c20ddf219
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427203"
---
# <a name="fast-shutdown-overview"></a>Visão geral do desligamento rápido

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O desligamento rápido é um mecanismo para que um cliente de MAPI inicie um desligamento rápido do processo do cliente, notificando todos os provedores com os quais o cliente tem uma sessão MAPI ativa para salvar dados e configurações antes que o processo do cliente seja fechado. Este tópico descreve o mecanismo básico de desligamento rápido. 

A partir do Microsoft Outlook 2010 e agora incluindo o Microsoft Outlook 2013, o subsistema de MAPI fornece a interface [IMAPIClientShutdown : IUnknown.](imapiclientshutdowniunknown.md) O Outlook e outros clientes MAPI podem adotar o desligamento rápido como o mecanismo padrão para sair do processo do cliente. Uma configuração de nível de usuário no Registro do Windows do computador cliente controla a adoção do desligamento rápido para todos os clientes MAPI para esse usuário nesse computador. Para obter detalhes sobre as configurações do Registro, consulte [Opções do Usuário de Desligamento Rápido.](fast-shutdown-user-options.md)
  
Se um cliente de MAPI precisar adotar o desligamento rápido, ele deverá usar a interface **IMAPIClientShutdown : IUnknown.** A seguir está o curso típico de eventos quando o cliente tenta desligar: 
  
1. O cliente MAPI inicia o desligamento chamando o método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) para determinar se o subsistema de MAPI dá suporte ao desligamento rápido. 
    
2. O subsistema de MAPI responde com o suporte de desligamento rápido disponível à chamada **IMAPIClientShutdown::QueryFastShutdown** do cliente usando o seguinte procedimento: 
    
    1. O subsistema de MAPI chama o método [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para cada provedor de MAPI com o qual o processo de cliente MAPI tem uma sessão MAPI ativa, se o provedor implementou o [IMAPIProviderShutdown : interface IUnknown.](imapiprovidershutdowniunknown.md) 
        
       > [!NOTE]
       >  O subsistema de MAPI sempre consulta e notifica os provedores MAPI por meio do **IMAPIProviderShutdown : interface IUnknown** dentro de cada sessão MAPI na seguinte ordem:
       > 1. Provedores de transporte
       > 2. Provedores de lista de endereços
       > 3. Provedores da Loja 
    
    2. Dependendo da configuração do Registro de desligamento rápido desse usuário no computador cliente, o subsistema de MAPI especifica o código de retorno apropriado para **IMAPIClientShutdown::QueryFastShutdown**. O código de retorno é S_OK ou MAPI_E_NO_SUPPORT.
        
    3. O cliente MAPI chama o método [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) para indicar ao subsistema de MAPI a intenção de desligar. 
        
    4. O subsistema MAPI indica a cada provedor MAPI carregado que o cliente MAPI desligará. Para os provedores que implementaram a interface **IMAPIProviderShutdown : IUnknown,** o subsistema de MAPI chama o método [IMAPIProviderShutdown::NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) correspondente. 
        
    5. O cliente MAPI chama o [método IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) para indicar ao subsistema MAPI que o processo do cliente está saindo imediatamente. 
        
    6. O subsistema MAPI indica a cada provedor MAPI carregado que o processo de cliente MAPI está sendo finalizado. Para os provedores que implementaram a interface **IMAPIProviderShutdown : IUnknown,** o subsistema de MAPI chama o [IMAPIProviderShutdown::D oFastShutdown](imapiprovidershutdown-dofastshutdown.md) método. Neste ponto, esses provedores de MAPI devem verificar se todas as ações necessárias, como salvar dados e configurações, estão concluídas em preparação para o cliente MAPI desconectar imediatamente todas as referências e sair. 
    
## <a name="see-also"></a>Confira também

- [Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)
- [Opções de usuário de desligamento rápido](fast-shutdown-user-options.md)
- [Práticas recomendadas para o desligamento rápido](best-practices-for-fast-shutdown.md)

