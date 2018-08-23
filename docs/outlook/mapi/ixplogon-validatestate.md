---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4fd0dd02c5cf6f6a49b782d06c02e373dcfc3327
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577482"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Verifica o status de externo do provedor de transporte. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a verificação de status é executada e os resultados da verificação de status. Sinalizadores a seguir podem ser definidos:
    
ABORT_XP_HEADER_OPERATION 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. O provedor de transporte tem a opção para continuar trabalhando com a operação, ou pode anular a operação e retornar MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Valida o estado dos provedores de transporte carregado no momento, fazendo com que o MAPI spooler ao chamar o método seus [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . Esse sinalizador também oferece o MAPI spooler uma oportunidade para corrigir falhas de provedor de transporte crítico sem forçar os aplicativos cliente de fazer logoff e logon novamente. 
    
FORCE_XP_CONNECT 
  
> O usuário selecionou uma operação de conexão. Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, ocorre a ação de conectar sem cache.
    
FORCE_XP_DISCONNECT 
  
> O usuário selecionou uma operação de desconexão. Quando esse sinalizador é usado com REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, ocorre a ação de desconexão sem cache.
    
PROCESS_XP_HEADER_CACHE 
  
> As entradas da tabela de cache de cabeçalho devem ser processadas, todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DOWNLOAD devem ser baixadas e todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DELETE devem ser excluídas. Mensagens que tenham MSGSTATUS_REMOTE_DOWNLOAD e o MSGSTATUS_REMOTE_DELETE definido devem ser movidas.
    
REFRESH_XP_HEADER_CACHE 
  
> Uma nova lista de cabeçalhos de mensagem deve ser baixada e status de mensagem de todos os sinalizadores de marcação deve ser limpo.
    
SUPPRESS_UI 
  
> Impede que o provedor de transporte exiba uma interface do usuário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento. ele deve ter permissão para concluir ou deve ser interrompido antes que esta operação é tentada.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de transporte remoto envolvido não dá suporte a uma interface do usuário e do próprio aplicativo cliente deve exibir a caixa de diálogo.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método de **IXPLogon::ValidateState** para oferecer suporte a chamadas para o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para o objeto de status. O provedor de transporte deve responder à chamada **IXPLogon::ValidateState** exatamente como se o MAPI spooler tinha aberto de um objeto de status para a sessão de logon atual e, em seguida, chamado **IMAPIStatus::ValidateState** nesse objeto. 
  
Para suportar sua implementação do **IMAPIStatus::ValidateState**, o MAPI spooler chama **IXPLogon::ValidateState** em todos os objetos de logon para todos os provedores de transporte ativo que estão executando em uma sessão de perfil. 
  
## <a name="see-also"></a>Confira também



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

