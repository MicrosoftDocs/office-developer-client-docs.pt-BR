---
title: Práticas recomendadas para desLigamento rápido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ae8a9214-e53f-4c57-8dbe-aa7cc6903aa8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8c7225427b80d89c6dd8adfa85f7d91885850365
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426965"
---
# <a name="best-practices-for-fast-shutdown"></a>Práticas recomendadas para desLigamento rápido

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico recomenda as práticas recomendadas para administradores, clientes MAPI e provedores MAPI para usar as configurações do registro do Windows e as interfaces de desligamento rápido para minimizar a perda de dados durante o desligamento do cliente.
  
- Para que um cliente MAPI realize o desligamento rápido com êxito, de forma que os processos de provedor não provocam perda de dados, o cliente MAPI deve primeiro chamar o método [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . O cliente deve prosseguir com os métodos [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) com base no suporte do subsistema MAPI para o desligamento rápido, conforme indicado pelo valor de retorno de ** IMAPIClientShutdown:: QueryFastShutdown**. Como um cliente MAPI, o Microsoft Outlook não chama **IMAPIClientShutdown:: NotifyProcessShutdown** ou **IMAPIClientShutdown::D ofastshutdown** se **IMAPIClientShutdown:: QueryFastShutdown** retornar um erro. Se o administrador desabilitou o desligamento rápido no registro do Windows, o subsistema MAPI retornará MAPI_E_NO_SUPPORT a **IMAPIClientShutdown:: QueryFastShutdown**. Nesse caso, o subsistema MAPI não informa os provedores de MAPI de uma saída imediata do processo do cliente. Portanto, se um cliente MAPI ignora esse código de retorno de erro, prossegue com o desligamento rápido e desconecta todas as referências externas, todos os provedores MAPI carregados terão perda de dados. 
    
- Os provedores MAPI devem implementar a interface [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md) para executar as etapas oportunas e necessárias para evitar a perda de dados devido à desconexão de referências externas do cliente antes da saída do cliente. Um provedor deve adiar tudo o que não é essencial para salvar dados em seu repositório de dados principal. Por exemplo, um provedor de transporte deve adiar operações de fundo desnecessárias que verificam novas mensagens, um provedor de catálogo de endereços deve adiar o download de alterações recentes de seu servidor, e um provedor de repositório deve adiar tarefas de manutenção, como compactação ou indexação. 
    
- Os usuários que desejam que os clientes MAPI saiam assim que fechá-los devem usar a configuração padrão do registro que permite o desligamento rápido, a menos que um provedor seja desativado.
    
- Depois que um cliente MAPI chama **IMAPIClientShutdown::D ofastshutdown**, ele não deve fazer nenhuma chamada adicional para MAPI, incluindo a função [MAPIUninitialize](mapiuninitialize.md) . O cliente não deve usar o MAPI para o restante do tempo de vida do processo do cliente. 
    
- Um cliente MAPI nunca deve chamar diretamente uma interface de **IMAPIProviderShutdown** do provedor. Os clientes MAPI devem sempre usar a interface [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md) . 
    
- Se um provedor MAPI precisa garantir que o desligamento rápido não é usado enquanto é carregado, ele deve implementar a interface **IMAPIProviderShutdown** e retornar MAPI_E_NO_SUPPORT para o método **IMAPIProviderShutdown:: QueryFastShutdown** . No enTanto, para clientes MAPI como o Outlook, isso fará o cliente abandonar o desligamento rápido e levar mais tempo para desligar. 
    
## <a name="see-also"></a>Confira também



[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)
  
[Visão geral do desligamento rápido](fast-shutdown-overview.md)
  
[Opções do usuário de desLigamento rápido](fast-shutdown-user-options.md)

