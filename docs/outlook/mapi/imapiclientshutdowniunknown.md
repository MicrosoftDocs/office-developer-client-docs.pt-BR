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
ms.openlocfilehash: e68211049bc0f958ae24975f4ab4063953eef567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766956"
---
# <a name="imapiclientshutdown--iunknown"></a>IMAPIClientShutdown : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Permite que um cliente MAPI realizar o desligamento rápido do processo de cliente. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objeto [IMAPISession](imapisessioniunknown.md)  <br/> |
|Implementada por:  <br/> |Subsistema MAPI  <br/> |
|Chamado pelo:  <br/> |Cliente MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIClientShutdown  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPICLIENTSHUTDOWN  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) <br/> |O subsistema MAPI para desligamento rápido de consultas suporte que é fornecido por provedores MAPI carregados.  <br/> |
|[NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) <br/> |Indica a intenção do cliente MAPI para prosseguir com desligado.  <br/> |
|[DoFastShutdown](imapiclientshutdown-dofastshutdown.md) <br/> |Indica a intenção do cliente MAPI para sair do processo de cliente imediatamente.  <br/> |
   
## <a name="remarks"></a>Comentários

A finalidade do desligamento rápido é permitir que um cliente MAPI e qualquer provedor MAPI carregado com o qual o cliente MAPI tem uma sessão MAPI ativa para salvar os dados e configurações de MAPI. Isso permite que o cliente MAPI desconectar todas as referências externas e sair sem causar perda de dados. Um cliente MAPI que precisa para executar um desligamento rápido deve usar a interface de **IMAPIClientShutdown** . O cliente MAPI pode obter um ponteiro para essa interface chamando o método IUnknown:: QueryInterface em qualquer objeto [IMAPISession](imapisessioniunknown.md) . 
  
Um cliente MAPI sempre inicia um desligamento rápido chamando o método **IMAPIClientShutdown::QueryFastShutdown** . O subsistema de MAPI responde à consulta do cliente MAPI verificando se os provedores de MAPI carregados suportam para desligamento rápido do cliente. O administrador pode usar as configurações do registro do Windows para ajudar a determinar o nível de suporte do provedor que é necessário para clientes MAPI prosseguir com o desligamento rápido. Para obter mais informações, consulte [Opções de usuário de desligamento Fast](fast-shutdown-user-options.md).
  
Para prosseguir com o desligamento rápido, o cliente chama o método de **IMAPIClientShutdown::NotifyProcessShutdown** para indicar ao subsistema de MAPI a intenção para serem desligados. O cliente chama o método **IMAPIClientShutdown::DoFastShutdown** para indicar que o processo de cliente está deixando imediatamente. 
  
Para obter mais informações sobre o desligamento rápido, consulte [Visão geral rápida de desligamento](fast-shutdown-overview.md). Para obter informações sobre como executar o desligamento rápido com êxito, consulte [Práticas recomendadas para desligamento rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)
  
[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)

