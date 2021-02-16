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
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409654"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que o subsistema de MAPI informe um provedor de MAPI sobre o desligamento rápido de um cliente MAPI, para que o provedor de MAPI possa responder ao desligamento.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Exposto por:  <br/> |Objetos de provedor: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md) <br/> |
|Implementado por:  <br/> |Provedor MAPI  <br/> |
|Chamado por:  <br/> |Subsistema MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Consulta o provedor mapi para suporte de desligamento rápido.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Indica ao provedor de MAPI que um cliente MAPI fará um desligamento rápido, para que o provedor possa tomar medidas para evitar a perda de dados.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Indica ao provedor de MAPI que o cliente MAPI está saindo imediatamente, para que o provedor de MAPI persista nas alterações para evitar a perda de dados.  <br/> |
   
## <a name="remarks"></a>Comentários

O desligamento rápido permite que um cliente MAPI saia do processo em um curto período de tempo, com sorte, depois que o cliente e os provedores de MAPI carregados salvam dados e configurações de MAPI. O cliente MAPI sempre inicia um desligamento rápido e deve consultar o subsistema de MAPI para suporte de desligamento rápido dos provedores de MAPI carregados. Um administrador pode definir o Registro do Windows no nível do usuário para especificar o nível de suporte do provedor necessário para permitir o desligamento rápido de todos os clientes MAPI. Para obter mais informações sobre as configurações do Registro, consulte [Opções de Usuário de Desligamento Rápido.](fast-shutdown-user-options.md) No entanto, para que o desligamento rápido ocorra com êxito sem perda de dados, os provedores de MAPI devem implementar a interface **IMAPIProviderShutdown.** 
  
Um provedor de MAPI que precisa dar suporte ao desligamento rápido do cliente deve retornar S_OK para o subsistema de MAPI no método **IMAPIProviderShutdown::QueryFastShutdown.** Quando o subsistema de MAPI chama subsequentemente os métodos **IMAPIProviderShutdown::NotifyProcessShutdown** e **IMAPIProviderShutdown::D oFastShutdown,** o provedor de MAPI deve tomar as ações necessárias para salvar dados e configurações de MAPI e preparar a saída do cliente. 
  
Os provedores de MAPI que não precisam dar suporte ao desligamento rápido do cliente ainda devem implementar a interface **IMAPIProviderShutdown** e fazer com que o método **IMAPIProviderShutdown::QueryFastShutdown** retorne MAPI_E_NO_SUPPORT. Para o Outlook como um cliente MAPI, isso faz com que o Outlook aguarde até que todas as referências externas sejam lançadas antes de sair. 
  
Dependendo da configuração do Registro do Windows do usuário para o desligamento rápido, não implementar a interface **IMAPIProviderShutdown** não necessariamente impede o desligamento rápido de um cliente. 
  
Para obter mais informações sobre o processo de desligamento rápido, consulte [Visão geral do desligamento rápido.](fast-shutdown-overview.md) Para obter informações sobre como realizar o desligamento rápido com êxito, consulte Práticas recomendadas [para o desligamento rápido.](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)
  
[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)

