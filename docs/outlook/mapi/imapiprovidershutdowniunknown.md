---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 81b7b0c235f610e7aaa0c17ecd1760df5d382552
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587968"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que o subsistema MAPI informar um provedor MAPI do desligamento rápido de um cliente MAPI, para que o provedor MAPI possa atender ao desligamento.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos do provedor: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md) <br/> |
|Implementada por:  <br/> |Provedor MAPI  <br/> |
|Chamado pelo:  <br/> |Subsistema MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Suporte a consultas o provedor MAPI para o desligamento rápido.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Indica o provedor MAPI que um cliente MAPI irá fazer um rápido desligamento, para que o provedor pode executar ações para evitar a perda de dados.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Indica o provedor MAPI que o cliente MAPI está deixando imediatamente, para que o provedor MAPI persistirá alterações para evitar a perda de dados.  <br/> |
   
## <a name="remarks"></a>Comentários

Desligamento rápido permite que um cliente MAPI sair seu processo de dentro de um curto período de tempo, espera-se após o cliente e carregado provedores MAPI tem salvado dados e configurações de MAPI. O cliente MAPI sempre inicia um desligamento rápido e deve consultar o subsistema MAPI para suporte de desligamento rápido dos provedores MAPI carregados. Um administrador pode definir o registro do Windows no nível do usuário para especificar o nível de suporte do provedor que é necessário para permitir que o desligamento rápido de todos os clientes MAPI. Para obter mais informações sobre as configurações do registro, consulte [Opções de usuário de desligamento Fast](fast-shutdown-user-options.md). No entanto, para o desligamento rápido ocorra com êxito sem perda de dados, provedores MAPI devem implementar a interface de **IMAPIProviderShutdown** . 
  
Um provedor MAPI que precisa suportar desligamento rápido do cliente deve retornar S_OK no subsistema de MAPI no método **IMAPIProviderShutdown::QueryFastShutdown** . Quando o subsistema de MAPI subsequentemente chama os métodos **IMAPIProviderShutdown::NotifyProcessShutdown** e **IMAPIProviderShutdown::DoFastShutdown** , o provedor MAPI deve levar ações necessárias para salvar as configurações de MAPI e dados e Prepare para sair do cliente. 
  
Provedores MAPI que não é necessário para suportar o desligamento rápido do cliente ainda devem implementar a interface **IMAPIProviderShutdown** e têm o método **IMAPIProviderShutdown::QueryFastShutdown** retornar MAPI_E_NO_SUPPORT. Para o Outlook como um cliente MAPI, isso faz com que o Outlook esperar por todas as referências externas ser liberada antes de sair. 
  
Dependendo do registro do Windows do usuário configuração para fast desligamento, não Implementando a interface de **IMAPIProviderShutdown** não necessariamente impede que um desligamento rápido de cliente. 
  
Para obter mais informações sobre o processo de desligamento rápido, consulte [Visão geral rápida de desligamento](fast-shutdown-overview.md). Para obter informações sobre como realizar o desligamento rápido com êxito, consulte [Best Practices for desligamento rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)
  
[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)

