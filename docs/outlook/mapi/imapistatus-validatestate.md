---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5ab459239bdcdcad30c4b6c82d5a3f8641bd4aca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567801"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Confirma as informações de status externos disponíveis para o recurso MAPI ou o provedor de serviço. Esse método é suportado em todos os objetos de status. 
  
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
  
> [in] Uma bitmask dos sinalizadores que controla a validação. Sinalizadores a seguir podem ser definidos:
    
ABORT_XP_HEADER_OPERATION
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo correspondente. O objeto de status tem duas opções: 
    
   - Continue trabalhando na operação.
    
   - Interromper a operação e retornar MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Um ou mais das propriedades de configuração do objeto status é alterado. Clientes podem definir esse sinalizador para permitir que o spooler MAPI para dinamicamente corrigir falhas de provedor de transporte crítico. 
    
FORCE_XP_CONNECT 
  
> O objeto de status deve realizar uma conexão. Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a conexão ocorre sem cache.
    
FORCE_XP_DISCONNECT 
  
> O objeto de status deve realizar uma operação de desconexão. Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a desconexão ocorre sem cache.
    
PROCESS_XP_HEADER_CACHE 
  
> As entradas da tabela de cache de cabeçalho devem ser processadas, todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DOWNLOAD devem ser baixadas e todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DELETE devem ser excluídas. Mensagens que tenham MSGSTATUS_REMOTE_DOWNLOAD e o MSGSTATUS_REMOTE_DELETE definido devem ser movidas.
    
REFRESH_XP_HEADER_CACHE 
  
> Para um provedor de transporte remoto, uma nova lista de cabeçalhos de mensagem deve ser baixada e todos os sinalizadores que marcam o status da mensagem devem ser desmarcados.
    
SUPPRESS_UI 
  
> Impede que o objeto de status exiba uma interface do usuário como parte da operação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A validação foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento. ele deve ter permissão para concluir ou ele deve ser interrompido, antes que esta operação seja iniciada.
    
MAPI_E_NO_SUPPORT 
  
> O objeto status não suporta o método de validação, conforme indicado pela ausência do sinalizador STATUS_VALIDATE_STATE na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação de validação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. Esse valor será retornado somente por provedores de transporte remoto. 
    
## <a name="remarks"></a>Comentários

O método **IMAPIStatus::ValidateState** verifica o estado de um recurso que está associado um objeto de status. **ValidateState** é o único método na interface do [IMAPIStatus](imapistatusimapiprop.md) que é necessário para todos os objetos de status. O comportamento exato desse método depende da implementação. A tabela a seguir descreve a implementação de cada um dos diferentes tipos de objetos de status. 
  
|**Objeto de status**|ValidateState * * implementação * *|
|:-----|:-----|
|Subsistema MAPI  <br/> |Valida o estado de todos os recursos que possuem os provedores de serviço ativas no momento e o subsistema em si.  <br/> |
|Spooler MAPI  <br/> |Executa um logon de todos os provedores de transporte, independentemente dos se eles já estão conectados.  <br/> |
|Catálogo de endereços MAPI  <br/> |Verifica se as entradas em sua seção de perfil.  <br/> |
|Provedor de serviços  <br/> |Implementação depende do tipo de provedor e os sinalizadores definidos no parâmetro _ulFlags_ .  <br/> |
   
## <a name="notes-to-implementers"></a>Notas para implementadores

Aplicativos de cliente remoto chamam o método de **ValidateState** para iniciar remoto de processamento para várias ações. Este método existe principalmente para definir os bits de status para se comunicar com o spooler MAPI, em vez de realmente fazer qualquer trabalho. Normalmente, o provedor de transporte define sinalizadores em sua linha de status que indicam como o spooler MAPI quais ações precisam ser iniciadas a fim de concluir a solicitação do cliente. 

Nesse modelo de interação spooler de transporte de cliente, as ações solicitadas pelo cliente são assíncronas, que **ValidateState** retorna antes das ações solicitadas tiverem sido concluídas. No entanto, ações que não envolvem necessariamente o sistema de mensagens subjacente ou que envolvem uma interface específico de transporte, podem ser sincronizadas. O aplicativo cliente passa em uma bitmask dos sinalizadores a seguir para especificar quais ações o provedor de transporte remoto deve ser adotada. 
  
ABORT_XP_HEADER_OPERATION 
  
> Se possível, o provedor de transporte remoto deve cancelar qualquer operação que envolvem o download de cabeçalhos. Para fazer isso, o provedor de transporte deve definir os seguintes valores de propriedade na linha de status do objeto logon:
    
   - Desmarque os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) para informar o spooler MAPI para interromper o processo de liberação de entrada para esse provedor de transporte.
    
   - Defina o STATUS_OFFLINE bit na propriedade **PR_STATUS_CODE** . 
    
   - Defina a propriedade **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) como TRUE.
    
   - Defina a propriedade de **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário.
    
   - Retorne S_OK. No entanto, se a operação em andamento não pode ser cancelada, **ValidateState** deve retornar MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Um provedor de transporte remoto nunca deve estabelecer uma conexão a um recurso compartilhado (por exemplo, um modem ou porta COM) fora do contexto da interação spooler-transporte MAPI envolvida no método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) . Se **ValidateState** for chamado com esse sinalizador, seu provedor de transporte deve fazer o seguinte: 
    
   - Defina um sinalizador interno de status para indicar que a conexão remota deve ser estabelecida quando o método **IXPLogon::FlushQueues** é chamado. 
    
   - Defina os valores corretos na tabela de status para fazer com que o MAPI spooler iniciar a fila de liberação do processo.
    
   - Quando estiver concluída liberação de filas, libere o recurso compartilhado.
    
   - Desmarque o STATUS_OFFLINE bit na propriedade **PR_STATUS_CODE** . 
    
   - Retorne S_OK.
    
FORCE_XP_DISCONNECT 
  
> O provedor de transporte remoto deve liberar a sua conexão aos recursos do sistema de mensagens. Depois de fazer isso, ele deve definido o bit STATUS_OFFLINE na propriedade **PR_STATUS_CODE** e retornar S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> O provedor de transporte remoto deve processam remoto e carregar todas as mensagens que tenham sido adiadas. Para fazer isso, o provedor de transporte deve definir os seguintes valores de propriedade na linha de status do objeto logon:
    
   - Defina a propriedade **PR_STATUS_STRING** como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário. 
    
   - Defina os bits STATUS_OUTBOUND_ENABLED e STATUS_OUTBOUND_ACTIVE na propriedade **PR_STATUS_CODE** . 
    
   - Defina a propriedade **PR_REMOTE_VALIDATE_OK** na linha de status do provedor de transporte como FALSE. 
    
   - Se outra operação está em andamento (por exemplo, o download de cabeçalhos) quando **ValidateState** é chamado, **ValidateState** deve retornar MAPI_E_BUSY. 
    
   - Execute o código para processar o sinalizador REFRESH_XP_HEADER_CACHE, também, para atender aos requisitos do cliente do Microsoft Exchange.
    
REFRESH_XP_HEADER_CACHE 
  
> O provedor de transporte remoto deve recuperar quaisquer cabeçalhos de mensagens novas do sistema de mensagens. Para fazer isso, o provedor de transporte deve fazer o seguinte:
    
   - Defina a propriedade **PR_STATUS_STRING** como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário. 
    
   - Defina os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE na propriedade **PR_STATUS_CODE** . 
    
   - Desmarque o STATUS_OFFLINE bit na propriedade **PR_STATUS_CODE** . 
    
   - Defina o STATUS_ONLINE bit na propriedade **PR_STATUS_CODE** . 
    
   - Defina a propriedade **PR_REMOTE_VALIDATE_OK** na linha de status do provedor de transporte como FALSE. 
    
SHOW_XP_SESSION_UI 
  
> Se seu provedor de transporte tiver quaisquer partes da interface do usuário para processar os cabeçalhos de mensagem (por exemplo, uma caixa de diálogo que confirma que o download de mensagens), essa caixa de diálogo deve ser exibida. Caso contrário, **ValidateState** pode retornar MAPI_E_NO_SUPPORT. 
    
Se quaisquer sinalizadores diferentes desses sejam passados, **ValidateState** deve retornar MAPI_E_UNKNOWN_FLAGS. 
  
Chamada do cliente para o provedor de transporte frequentemente será para o método **IMAPIStatus::ValidateState** . Durante o processamento de **ValidateState**, o provedor de transporte não deve executar nenhuma ação que aloca recursos escassos do sistema, como um modem ou porta COM. Isso ocorre porque o MAPI spooler em alguns casos, será necessário liberar filas em mais de um provedor de transporte. No entanto, o cliente pode chamar o método de **ValidateState** de qualquer provedor de transporte a qualquer momento. Se seu provedor de transporte tentar alocar um recurso escasso durante o processamento de **ValidateState**, pode resultar em um erro devido a conflito com outro provedor de transporte que o MAPI spooler tem instruído a liberar seus filas. Se você permitir todas as alocações de recursos escassos ocorra sob a orientação do spooler MAPI, você pode evitar esses conflitos. Seu provedor de transporte deve oferecer suporte a propriedade **PR_REMOTE_VALIDATE_OK** para que aplicativos cliente podem detectar quando seu provedor de transporte está ocupado ou aguardando o MAPI spooler iniciar uma ação. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como este método pode causar outras potencialmente demoradas chamadas sejam feitas, **ValidateState** pode retornar MAPI_E_BUSY para informá-lo de que esse método está aguardando a conclusão de outra operação. Você deve aguardar até que a operação pendente seja concluída antes de tentar outra tarefa. 
  
Você tem mais controle sobre suas chamadas para objetos de status do provedor de transporte. Você pode passar um ou mais sinalizadores para **ValidateState** que afetam de operações o provedor de transporte. Por exemplo, o sinalizador ABORT_XP_HEADER_OPERATION indica que o usuário cancelou a validação. Provedores de transporte podem optar por anular, retornando MAPI_E_USER_CANCELED, ou podem continuar. 
  
Você pode definir o sinalizador CONFIG_CHANGED em uma chamada para o objeto de status de um provedor de serviço ou o spooler MAPI para indicar que uma opção de configuração foi alterada. Você pode usar CONFIG_CHANGED para reconfigurar dinamicamente um provedor de transporte. Quando você definir CONFIG_CHANGED em uma chamada para o objeto de status de um provedor de serviços, o provedor responde com uma chamada para [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) usado para alertar o MAPI spooler da alteração. Quando você definir CONFIG_CHANGED em uma chamada para o objeto de status do spooler MAPI, o spooler chama [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para cada provedor de transporte ativa. **AddressTypes** informa o MAPI spooler dos tipos de endereço com suporte de um transporte. Alguns provedores de serviços também exibem um indicador de progresso se a validação é esperada para levar muito tempo. Exibir um indicador de progresso é útil, mas não é necessário. 
  
Quando o sinalizador SUPPRESS_UI é definido, nenhum dos caixas de diálogo de progresso ou folhas de propriedades de configuração podem ser exibidas. 
  
## <a name="see-also"></a>Confira também

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Propriedade canônica PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)
- [Propriedade canônica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
- [Propriedade canônica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
- [Propriedade canônica PidTagStatusString](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

