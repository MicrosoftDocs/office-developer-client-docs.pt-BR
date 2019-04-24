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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351566"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Verifica o status externo do provedor de transporte. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Uma alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a verificação de status é executada e os resultados da verificação de status. Os seguintes sinalizadores podem ser definidos:
    
ABORT_XP_HEADER_OPERATION 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. O provedor de transporte tem a opção de continuar trabalhando na operação ou pode anular a operação e retornar MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Valida o estado dos provedores de transporte atualmente carregados, fazendo com que o spooler MAPI chame o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . Esse sinalizador também fornece ao spooler MAPI uma oportunidade de corrigir falhas críticas do provedor de transporte sem forçar os aplicativos cliente a fazer logoff e, em seguida, fazer logon novamente. 
    
FORCE_XP_CONNECT 
  
> O usuário selecionou uma operação de conexão. Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a ação de conexão ocorre sem cache.
    
FORCE_XP_DISCONNECT 
  
> O usuário selecionou uma operação de desconexão. Quando esse sinalizador é usado com REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a ação de desconexão ocorre sem cache.
    
PROCESS_XP_HEADER_CACHE 
  
> As entradas na tabela de cache de cabeçalho devem ser processadas, todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DOWNLOAD devem ser baixadas e todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DELETE devem ser excluídas. As mensagens que têm o conjunto MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE devem ser movidas.
    
REFRESH_XP_HEADER_CACHE 
  
> Uma nova lista de cabeçalhos de mensagens deve ser baixada e todos os sinalizadores de marcação de status de mensagens devem ser apagados.
    
SUPPRESS_UI 
  
> Impede que o provedor de transporte exiba uma interface do usuário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento; Ele deve ter permissão para ser concluído ou deve ser interrompido antes que esta operação seja tentada.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de transporte remoto envolvido não oferece suporte a uma interface de usuário e o próprio aplicativo cliente deve exibir a caixa de diálogo.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon:: ValidateState** para dar suporte às chamadas para o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) para o objeto status. O provedor de transporte deve responder à chamada **IXPLogon:: ValidateState** exatamente como se o spooler MAPI tivesse aberto um objeto status para a sessão de logon atual e, em seguida, chamou **IMAPIStatus:: ValidateState** nesse objeto. 
  
Para dar suporte à implementação de **IMAPIStatus:: ValidateState**, o spooler MAPI chama **IXPLogon:: ValidateState** em todos os objetos de logon para todos os provedores de transporte ativos que estão sendo executados em uma sessão de perfil. 
  
## <a name="see-also"></a>Confira também



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

