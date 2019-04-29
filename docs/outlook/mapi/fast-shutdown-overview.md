---
title: Visão geral do desLigamento rápido
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
# <a name="fast-shutdown-overview"></a>Visão geral do desLigamento rápido

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O desligamento rápido é um mecanismo para um cliente MAPI para iniciar um desligamento rápido do processo de cliente, notificando todos os provedores com os quais o cliente tem uma sessão MAPI ativa para salvar dados e configurações antes de o processo cliente sair. Este tópico descreve o mecanismo básico de desligamento rápido. 

A partir do Microsoft Outlook 2010 e agora incluindo o Microsoft Outlook 2013, o subsistema MAPI fornece a interface [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) . O Outlook e outros clientes MAPI podem adotar o desligamento rápido como o mecanismo padrão para sair do processo de cliente. Uma configuração de nível de usuário no registro do Windows do computador cliente controla a adoção do desligamento rápido para todos os clientes MAPI desse usuário nesse computador. Para obter detalhes sobre as configurações do registro, consulte [Opções do usuário](fast-shutdown-user-options.md)de desligamento rápido.
  
Se um cliente MAPI precisar adotar um desligamento rápido, ele deverá usar a interface **IMAPIClientShutdown: IUnknown** . Este é o curso típico de eventos quando o cliente tenta desligar: 
  
1. O cliente MAPI inicia o desligamento chamando o método [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) para determinar se o subsistema MAPI oferece suporte ao desligamento rápido. 
    
2. O subsistema MAPI responde com o suporte de desligamento rápido disponível para a chamada **IMAPIClientShutdown:: QueryFastShutdown** do cliente usando o seguinte procedimento: 
    
    1. O subsistema MAPI chama o método [IMAPIProviderShutdown:: QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) para cada provedor MAPI com o qual o processo de cliente MAPI tem uma sessão MAPI ativa, se o provedor tiver implementado o [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) interface. 
        
       > [!NOTE]
       >  O subsistema MAPI sempre consulta e notifica provedores MAPI através da interface **IMAPIProviderShutdown: IUnknown** dentro de cada sessão MAPI na seguinte ordem:
       > 1. Provedores de transporte
       > 2. Provedores de catálogo de endereços
       > 3. Provedores de repositório 
    
    2. Dependendo da configuração do registro de desligamento rápido para esse usuário no computador cliente, o subsistema MAPI especifica o código de retorno apropriado para **IMAPIClientShutdown:: QueryFastShutdown**. O código de retorno é S_OK ou MAPI_E_NO_SUPPORT.
        
    3. O cliente MAPI chama o método [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) para indicar ao subsistema MAPI a intenção de desligar. 
        
    4. O subsistema MAPI indica a cada provedor MAPI carregado que o cliente MAPI desligará. Para os provedores que implementaram a interface **IMAPIProviderShutdown: IUnknown** , o subsistema MAPI chama o método [IMAPIProviderShutdown:: NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) correspondente. 
        
    5. O cliente MAPI chama o método [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) para indicar ao subsistema MAPI que o processo cliente está saindo imediatamente. 
        
    6. O subsistema MAPI indica a cada provedor MAPI carregado que o processo de cliente MAPI está saindo. Para os provedores que implementaram a interface **IMAPIProviderShutdown: IUnknown** , o subsistema MAPI chama o método [IMAPIProviderShutdown::D ofastshutdown](imapiprovidershutdown-dofastshutdown.md) correspondente. Neste ponto, esses provedores MAPI devem verificar se todas as ações necessárias, como salvar dados e configurações, estão completas em preparação para o cliente MAPI para desconectar imediatamente todas as referências e sair. 
    
## <a name="see-also"></a>Confira também

- [Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)
- [Opções do usuário de desLigamento rápido](fast-shutdown-user-options.md)
- [Práticas recomendadas para o desligamento rápido](best-practices-for-fast-shutdown.md)

