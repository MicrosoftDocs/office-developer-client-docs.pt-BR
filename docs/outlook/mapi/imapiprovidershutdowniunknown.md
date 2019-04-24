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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322399"
---
# <a name="imapiprovidershutdown--iunknown"></a>IMAPIProviderShutdown : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que o subsistema MAPI informe um provedor MAPI do desligamento rápido de um cliente MAPI, para que o provedor MAPI possa responder ao desligamento.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Objetos do provedor: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md) <br/> |
|Implementado por:  <br/> |Provedor MAPI  <br/> |
|Chamado por:  <br/> |Subsistema MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIProviderShutdown  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIPROVIDERSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) <br/> |Consulta o provedor MAPI para obter suporte para desligamento rápido.  <br/> |
|[NotifyProcessShutdown](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |Indica ao provedor MAPI que um cliente MAPI fará um desligamento rápido, para que o provedor possa realizar ações para evitar a perda de dados.  <br/> |
|[DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) <br/> |Indica ao provedor MAPI que o cliente MAPI está saindo imediatamente, para que o provedor MAPI persista as alterações para evitar a perda de dados.  <br/> |
   
## <a name="remarks"></a>Comentários

O desligamento rápido permite que um cliente MAPI saia do processo dentro de um curto período de tempo, espero que o cliente e os provedores MAPI carregados tenham salvado as configurações e os dados MAPI. O cliente MAPI sempre inicia um desligamento rápido e deve consultar o subsistema MAPI para obter suporte de desligamento rápido dos provedores MAPI carregados. Um administrador pode definir o registro do Windows no nível do usuário para especificar o nível de suporte do provedor que é necessário para permitir o desligamento rápido de todos os clientes MAPI. Para obter mais informações sobre as configurações do registro, consulte [Opções do usuário](fast-shutdown-user-options.md)de desligamento rápido. No enTanto, para que o desligamento rápido ocorra com êxito sem perda de dados, os provedores MAPI devem implementar a interface **IMAPIProviderShutdown** . 
  
Um provedor MAPI que precisa dar suporte ao desligamento rápido do cliente deve retornar S_OK ao subsistema MAPI no método **IMAPIProviderShutdown:: QueryFastShutdown** . Quando o subsistema MAPI chama os métodos **IMAPIProviderShutdown:: NotifyProcessShutdown** e **IMAPIProviderShutdown::D ofastshutdown** , o provedor MAPI deve tomar as ações necessárias para salvar as configurações e os dados de MAPI e Prepare-se para a saída do cliente. 
  
Os provedores MAPI que não precisam dar suporte ao desligamento rápido do cliente ainda devem implementar a interface **IMAPIProviderShutdown** e fazer com que o método **IMAPIProviderShutdown:: QUERYFASTSHUTDOWN** retorne MAPI_E_NO_SUPPORT. Para o Outlook como um cliente MAPI, isso faz com que o Outlook espere que todas as referências externas sejam liberadas antes de sair. 
  
Dependendo da configuração do registro do Windows do usuário para desligamento rápido, não implementar a interface **IMAPIProviderShutdown** não necessariamente impede um desligamento rápido do cliente. 
  
Para obter mais informações sobre o processo de desligamento rápido, consulte [visão geral](fast-shutdown-overview.md)de desligamento rápido. Para obter informações sobre como executar o desligamento rápido com êxito, consulte [práticas recomendadas para](best-practices-for-fast-shutdown.md)o desligamento rápido.
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)
  
[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)

