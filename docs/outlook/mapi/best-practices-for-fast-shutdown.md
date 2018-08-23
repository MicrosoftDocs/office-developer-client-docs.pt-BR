---
title: Práticas recomendadas para o desligamento rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c92347ab1a786196e7f0d99b286e8f4134ce7c24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590698"
---
# <a name="best-practices-for-fast-shutdown"></a>Práticas recomendadas para o desligamento rápido

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico fornece práticas recomendadas para os administradores, os clientes MAPI e provedores MAPI usar configurações de registro do Windows e as interfaces de desligamento rápido para minimizar a perda de dados durante o desligamento do cliente.
  
- Para um cliente MAPI realizar desligamento rápido com êxito, para que os processos de provedor não provocam perda de dados, o cliente MAPI do primeiro deve chamar o método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . O cliente deve então prosseguir com os métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) com base no suporte do subsistema MAPI para fast desligamento, conforme indicado pelo valor de retorno de ** IMAPIClientShutdown::QueryFastShutdown**. Como um cliente MAPI, o Microsoft Outlook não chama **IMAPIClientShutdown::NotifyProcessShutdown** ou **IMAPIClientShutdown::DoFastShutdown** se **IMAPIClientShutdown::QueryFastShutdown** retornará um erro. Se o administrador tiver desabilitado o desligamento rápido no registro do Windows, o subsistema de MAPI retornaria MAPI_E_NO_SUPPORT para **IMAPIClientShutdown::QueryFastShutdown**. Nesse caso, o subsistema de MAPI não seria informe sair de provedores de MAPI de um processo de cliente imediata. Portanto, se um cliente MAPI ignora este código de retorno de erro, prossegue para rápida desligamento e desconecta todas as referências externas, todos os provedores MAPI carregados terá a perda de dados. 
    
- Provedores MAPI deverá implementar o [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) interface para realizar as etapas necessárias e em tempo hábil para evitar a perda de dados por cliente desconectando as referências externas antes de que sai do cliente. Um provedor deve adiar tudo que é não essenciais ao salvar dados em seu repositório de dados primário. Por exemplo, um provedor de transporte deve adiar operações de plano de fundo desnecessárias que procurar por novos email, que um provedor de catálogo de endereços deve adiar baixando alterações recentes do seu servidor, e um provedor de armazenamento deve adiar tarefas de manutenção, como compactação ou indexação. 
    
- Os usuários que desejem que os clientes MAPI para sair assim que eles fechá-los devem usar a configuração do registro padrão que permite o desligamento rápido, a menos que um provedor recusa.
    
- Depois que um cliente MAPI chama **IMAPIClientShutdown::DoFastShutdown**, ele não verifique todas as chamadas adicionais para MAPI, incluindo a função [MAPIUninitialize](mapiuninitialize.md) . O cliente não deve usar o MAPI para o restante do tempo de vida do processo do cliente. 
    
- Um cliente MAPI nunca diretamente deve chamar a interface de **IMAPIProviderShutdown** de um provedor. Clientes MAPI sempre devem usar o [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) interface. 
    
- Se precisar de um provedor MAPI garantir que desligamento rápido não seja usado enquanto ele for carregado, ele deve implementar a interface **IMAPIProviderShutdown** e retornar MAPI_E_NO_SUPPORT para o método **IMAPIProviderShutdown::QueryFastShutdown** . No entanto, para clientes MAPI, como o Outlook, isso fará com que o cliente abandonar desligamento rápido e levar mais tempo para serem desligados. 
    
## <a name="see-also"></a>Confira também



[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)
  
[Visão geral do desligamento rápido](fast-shutdown-overview.md)
  
[Opções de usuário do desligamento rápido](fast-shutdown-user-options.md)

