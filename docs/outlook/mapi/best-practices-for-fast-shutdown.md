---
title: Práticas recomendadas para o desligamento rápido
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
# <a name="best-practices-for-fast-shutdown"></a>Práticas recomendadas para o desligamento rápido

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico recomenda práticas recomendadas para administradores, clientes MAPI e provedores MAPI usarem as configurações do Registro do Windows e as interfaces de desligamento rápido para minimizar a perda de dados durante o desligamento do cliente.
  
- Para que um cliente de MAPI realize o desligamento rápido com êxito para que os processos do provedor não incorrem em perda de dados, o cliente MAPI deve primeiro chamar o método [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Em seguida, o cliente deve prosseguir com os métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) com base no suporte do subsistema de MAPI para desligamento rápido, conforme indicado pelo valor de retorno **de IMAPIClientShutdown::QueryFastShutdown**. Como um cliente MAPI, o Microsoft Outlook não chama **IMAPIClientShutdown::NotifyProcessShutdown** ou **IMAPIClientShutdown::D oFastShutdown** se **IMAPIClientShutdown::QueryFastShutdown** retornar um erro. Se o administrador tiver desabilitado o desligamento rápido no Registro do Windows, o subsistema de MAPI retornará MAPI_E_NO_SUPPORT para **IMAPIClientShutdown::QueryFastShutdown**. Nesse caso, o subsistema de MAPI não informaria os provedores de MAPI sobre uma saída imediata do processo de cliente. Portanto, se um cliente MAPI desconsiderar esse código de retorno de erro, continuar a fazer o desligamento rápido e desconectar todas as referências externas, todos os provedores de MAPI carregados terão perda de dados. 
    
- Os provedores de MAPI devem implementar a interface [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) para executar as etapas oportunas e necessárias para evitar a perda de dados devido à desconexão de referências externas do cliente antes de o cliente sair. Um provedor deve adiar todo o resto que não seja fundamental para salvar dados em seu armazenamento de dados primário. Por exemplo, um provedor de transporte deve adiar operações em segundo plano desnecessárias que verificam novos emails, um provedor de agendamento deve adiar o download de alterações recentes de seu servidor e um provedor de armazenamento deve adiar tarefas de manutenção, como compactação ou indexação. 
    
- Os usuários que quiserem que os clientes MAPI saiam assim que os fecharem devem usar a configuração padrão do Registro que permite o desligamento rápido, a menos que um provedor a retiver.
    
- Depois que um cliente MAPI chama **IMAPIClientShutdown::D oFastShutdown**, ele não deve fazer nenhuma chamada adicional para MAPI, incluindo a função [MAPIUninitialize.](mapiuninitialize.md) O cliente não deve usar MAPI para o restante do tempo de vida do processo do cliente. 
    
- Um cliente MAPI nunca deve chamar diretamente a interface **IMAPIProviderShutdown de um** provedor. Os clientes MAPI sempre devem usar [a interface IMAPIClientShutdown : IUnknown.](imapiclientshutdowniunknown.md) 
    
- Se um provedor de MAPI precisar garantir que o desligamento rápido não seja usado durante o carregamento, ele deverá implementar a interface **IMAPIProviderShutdown** e retornar MAPI_E_NO_SUPPORT para o método **IMAPIProviderShutdown::QueryFastShutdown.** No entanto, para clientes MAPI, como o Outlook, isso fará com que o cliente abandone o desligamento rápido e leve mais tempo para desligar. 
    
## <a name="see-also"></a>Confira também



[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)
  
[Visão geral do desligamento rápido](fast-shutdown-overview.md)
  
[Opções de usuário de desligamento rápido](fast-shutdown-user-options.md)

