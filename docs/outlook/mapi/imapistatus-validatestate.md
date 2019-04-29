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
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438145"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Confirma as informações de status externas disponíveis para o recurso MAPI ou provedor de serviços. Este método é suportado em todos os objetos status. 
  
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
  
> no Uma bitmask de sinalizadores que controlam a validação. Os seguintes sinalizadores podem ser definidos:
    
ABORT_XP_HEADER_OPERATION
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo correspondente. O objeto status tem duas opções: 
    
   - Continuar a trabalhar na operação.
    
   - Interrompa a operação e retorne o MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Uma ou mais das propriedades de configuração do objeto status foram alteradas. Os clientes podem definir esse sinalizador para permitir que o spooler MAPI corrija dinamicamente as falhas críticas do provedor de transporte. 
    
FORCE_XP_CONNECT 
  
> O objeto status deve executar uma conexão. Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a conexão ocorre sem cache.
    
FORCE_XP_DISCONNECT 
  
> O objeto status deve executar uma operação de desconexão. Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a desconexão ocorre sem cache.
    
PROCESS_XP_HEADER_CACHE 
  
> As entradas na tabela de cache de cabeçalho devem ser processadas, todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DOWNLOAD devem ser baixadas e todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DELETE devem ser excluídas. As mensagens que têm o conjunto MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE devem ser movidas.
    
REFRESH_XP_HEADER_CACHE 
  
> Para um provedor de transporte remoto, uma nova lista de cabeçalhos de mensagens deve ser baixada e todos os sinalizadores que marcam o status da mensagem devem ser desmarcados.
    
SUPPRESS_UI 
  
> Impede que o objeto de status exiba uma interface do usuário como parte da operação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A validação foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento; Ele deve ter permissão para ser concluído ou deve ser interrompido antes da operação ser iniciada.
    
MAPI_E_NO_SUPPORT 
  
> O objeto status não é compatível com o método de validação, conforme indicado pela ausência do sinalizador STATUS_VALIDATE_STATE na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação de validação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. Esse valor é retornado apenas pelos provedores de transporte remoto. 
    
## <a name="remarks"></a>Comentários

O método **IMAPIStatus:: ValidateState** verifica o estado de um recurso que está associado a um objeto status. **ValidateState** é o único método na interface [IMAPIStatus](imapistatusimapiprop.md) que é necessário para todos os objetos status. O comportamento exato desse método depende da implementação. A tabela a seguir descreve a implementação de cada um dos diferentes tipos de objetos status. 
  
|**Objeto status**|ValidateState * * implementação * *|
|:-----|:-----|
|Subsistema MAPI  <br/> |Valida o estado de todos os recursos que os provedores de serviço ativos atualmente e o subsistema.  <br/> |
|Spooler MAPI  <br/> |Executa um logon de todos os provedores de transporte, independentemente de estarem ou não conectados.  <br/> |
|Catálogo de endereços MAPI  <br/> |Verifica as entradas em sua seção de perfil.  <br/> |
|Provedor de serviços  <br/> |A implementação depende do tipo de provedor e dos sinalizadores definidos no parâmetro _parâmetroulflags_ .  <br/> |
   
## <a name="notes-to-implementers"></a>Observações para implementadores

Os aplicativos cliente remotos **** chamam o método ValidateState para iniciar o processamento remoto para várias ações. Esse método existe principalmente para definir que os bits de status se comuniquem com o spooler MAPI, em vez de para realmente realizar qualquer trabalho. Normalmente, o provedor de transporte define sinalizadores em sua linha de status que indicam ao spooler MAPI quais ações precisam ser iniciadas para concluir a solicitação do cliente. 

Nesse modelo de interação do Client-Transport-spooler, as ações solicitadas pelo cliente são assíncronas, pois **ValidateState** retorna antes que as ações solicitadas sejam concluídas. No enTanto, as ações que não envolvem necessariamente o sistema de mensagens subjacente ou que envolvem uma interface específica de transporte podem ser síncronas. O aplicativo cliente passa em uma bitmask dos seguintes sinalizadores para especificar quais ações o provedor de transporte remoto deve executar. 
  
ABORT_XP_HEADER_OPERATION 
  
> Se possível, o provedor de transporte remoto deve cancelar as operações que envolvem o download de cabeçalhos. Para fazer isso, o provedor de transporte deve definir os valores de propriedade a seguir na linha de status do objeto de logon:
    
   - DesMarque os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE da propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) para INSTRUIr o spooler MAPI a interromper o processo de liberação de entrada para este provedor de transporte.
    
   - Defina o bit STATUS_OFFLINE na propriedade **PR_STATUS_CODE** . 
    
   - Defina a propriedade **PR_REMOTE_VALIDATE_OK** ([PIDTAGREMOTEVALIDATEOK](pidtagremotevalidateok-canonical-property.md)) como true.
    
   - Defina a propriedade **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário.
    
   - Retorne S_OK. No enTanto, se a operação em andamento não puder **** ser cancelada, ValidateState deverá retornar MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Um provedor de transporte remoto nunca deve estabelecer uma conexão com um recurso compartilhado (por exemplo, um modem ou uma porta COM) fora do contexto da interação MAPI spooler-transporte envolvida no método [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) . Se **ValidateState** for chamado com esse sinalizador, o provedor de transporte deverá fazer o seguinte: 
    
   - Defina um sinalizador de status interno para indicar que a conexão remota deve ser estabelecida quando o método **IXPLogon:: FlushQueues** for chamado. 
    
   - Defina os valores corretos na tabela de status para fazer com que o spooler MAPI inicie o processo de liberação de fila.
    
   - Quando a liberação de filas estiver concluída, libere o recurso compartilhado.
    
   - Limpe o bit STATUS_OFFLINE na propriedade **PR_STATUS_CODE** . 
    
   - Retorne S_OK.
    
FORCE_XP_DISCONNECT 
  
> O provedor de transporte remoto deve liberar sua conexão com os recursos do sistema de mensagens. Depois disso, ele deve definir o bit STATUS_OFFLINE na propriedade **PR_STATUS_CODE** e retornar S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> O provedor de transporte remoto deve processar mensagens remotas e carregar todas as mensagens que foram adiadas. Para fazer isso, o provedor de transporte deve definir os valores de propriedade a seguir na linha de status do objeto de logon:
    
   - Defina a propriedade **PR_STATUS_STRING** como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário. 
    
   - Defina os bits STATUS_OUTBOUND_ENABLED e STATUS_OUTBOUND_ACTIVE na propriedade **PR_STATUS_CODE** . 
    
   - Defina a propriedade **PR_REMOTE_VALIDATE_OK** na linha de status do provedor de transporte para false. 
    
   - Se outra operação estiver em andamento (como baixar cabeçalhos) quando **ValidateState** for chamado, **ValidateState** deverá retornar MAPI_E_BUSY. 
    
   - Execute também o código para processar o sinalizador REFRESH_XP_HEADER_CACHE, para atender aos requisitos do cliente do Microsoft Exchange.
    
REFRESH_XP_HEADER_CACHE 
  
> O provedor de transporte remoto deve recuperar novos cabeçalhos de mensagem do sistema de mensagens. Para fazer isso, o provedor de transporte deve fazer o seguinte:
    
   - Defina a propriedade **PR_STATUS_STRING** como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário. 
    
   - Defina os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE na propriedade **PR_STATUS_CODE** . 
    
   - Limpe o bit STATUS_OFFLINE na propriedade **PR_STATUS_CODE** . 
    
   - Defina o bit STATUS_ONLINE na propriedade **PR_STATUS_CODE** . 
    
   - Defina a propriedade **PR_REMOTE_VALIDATE_OK** na linha de status do provedor de transporte para false. 
    
SHOW_XP_SESSION_UI 
  
> Se o seu provedor de transporte tiver qualquer trecho de interface do usuário para processar os cabeçalhos da mensagem (como uma caixa de diálogo que confirma o download de mensagens), essa caixa de diálogo deverá ser exibida. Caso contrário **** , ValidateState poderá retornar MAPI_E_NO_SUPPORT. 
    
Se qualquer sinalizador que não forem passados, ValidateState **** deverá retornar MAPI_E_UNKNOWN_FLAGS. 
  
A chamada do cliente para o provedor de transporte geralmente será para o método **IMAPIStatus:: ValidateState** . Durante o processamento de **ValidateState**, o provedor de transporte não deve executar qualquer ação que aloque recursos de sistema escassos, como um modem ou uma porta com. Isso ocorre porque o spooler MAPI às vezes precisará liberar filas em mais de um provedor de transporte. No enTanto, o cliente pode chamar qualquer método **ValidateState** do provedor de transporte a qualquer momento. Se o seu provedor de transporte tentar alocar um recurso escasso durante o **** processamento de ValidateState, um erro poderá ocorrer devido a um conflito com outro provedor de transporte que o spooler MAPI tenha instruído a liberar suas filas. Se você permitir que todas as alocações de recursos escassos ocorram na direção do spooler MAPI, você pode evitar conflitos. O provedor de transporte deve oferecer suporte à propriedade **PR_REMOTE_VALIDATE_OK** para que os aplicativos clientes possam detectar quando o provedor de transporte está ocupado ou aguardando que o spooler MAPI inicie uma ação. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como esse método pode fazer com que outras chamadas potencialmente demoradas sejam **** feitas, ValidateState pode retornar MAPI_E_BUSY para informá-lo de que esse método está aguardando a conclusão de outra operação. Você deve aguardar até que a operação pendente seja concluída antes de tentar outra tarefa. 
  
Você tem mais controle sobre suas chamadas para transportar objetos de status do provedor. Você pode passar um ou mais sinalizadores para **ValidateState** que afetam as operações do provedor de transporte. Por exemplo, o sinalizador ABORT_XP_HEADER_OPERATION indica que o usuário cancelou a validação. Os provedores de transporte podem decidir anular, retornar MAPI_E_USER_CANCELED ou podem continuar. 
  
Você pode definir o sinalizador CONFIG_CHANGED em uma chamada para o objeto status de um provedor de serviços ou o spooler MAPI para indicar que uma opção de configuração foi alterada. Você pode usar o CONFIG_CHANGED para reconfigurar dinamicamente um provedor de transporte. Quando você define CONFIG_CHANGED em uma chamada para um objeto status do provedor de serviço, o provedor responde com uma chamada para [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) para alertar o spooler MAPI da alteração. Quando você define CONFIG_CHANGED em uma chamada para o objeto status do spooler MAPI, o spooler chama [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) para cada provedor de transporte ativo. **AddressTypes** informa o spooler MAPI dos tipos de endereço com suporte de transporte. Alguns provedores de serviços também exibem um indicador de progresso se a validação for esperada por muito tempo. Exibir um indicador de progresso é útil, mas não é necessário. 
  
Quando o sinalizador SUPPRESS_UI é definido, nenhuma das folhas de propriedades de configuração ou caixas de diálogo de progresso podem ser exibidas. 
  
## <a name="see-also"></a>Confira também

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Propriedade canônica PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)
- [Propriedade canônica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
- [Propriedade canônica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
- [Propriedade canônica PidTagStatusString](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

