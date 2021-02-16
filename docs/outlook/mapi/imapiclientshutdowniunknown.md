---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435331"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que um cliente MAPI realize o desligamento rápido do processo do cliente. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Exposto por:  <br/> |[Objeto IMAPISession](imapisessioniunknown.md)  <br/> |
|Implementado por:  <br/> |Subsistema MAPI  <br/> |
|Chamado por:  <br/> |Cliente MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |Consulta o subsistema mapi para suporte de desligamento rápido fornecido por provedores MAPI carregados.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Indica a intenção do cliente MAPI de prosseguir com o desligado.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Indica a intenção do cliente MAPI de sair do processo de cliente imediatamente.  <br/> |
   
## <a name="remarks"></a>Comentários

O objetivo do desligamento rápido é permitir um cliente MAPI e qualquer provedor MAPI carregado com o qual o cliente MAPI tenha uma sessão MAPI ativa para salvar dados e configurações de MAPI. Isso permite que o cliente MAPI desconecte todas as referências externas e saia sem causar perda de dados. Um cliente MAPI que precisa executar o desligamento rápido deve usar a interface **IMAPIClientShutdown.** O cliente MAPI pode obter um ponteiro para essa interface chamando o método IUnknown::QueryInterface em qualquer [objeto IMAPISession.](imapisessioniunknown.md) 
  
Um cliente MAPI sempre inicia um desligamento rápido chamando o método **IMAPIClientShutdown::QueryFastShutdown.** O subsistema de MAPI responde à consulta do cliente MAPI verificando se os provedores MAPI carregados suportam o desligamento rápido do cliente. O administrador pode usar as configurações do Registro do Windows para ajudar a determinar o nível de suporte do provedor necessário para que os clientes MAPI prossigam com o desligamento rápido. Para obter mais informações, consulte Opções [de Usuário de Desligamento Rápido.](fast-shutdown-user-options.md)
  
Para prosseguir com o desligamento rápido, o cliente chama o método **IMAPIClientShutdown::NotifyProcessShutdown** para indicar ao subsistema MAPI a intenção de desligar. Em seguida, o cliente chama o **método IMAPIClientShutdown::D oFastShutdown** para indicar que o processo do cliente está saindo imediatamente. 
  
Para obter mais informações sobre o desligamento rápido, consulte [Visão geral do desligamento rápido.](fast-shutdown-overview.md) Para obter informações sobre como executar o desligamento rápido com êxito, consulte As Práticas Recomendadas [para o Desligamento Rápido.](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)
  
[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)

