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
  
Confirma as informações de status externas disponíveis para o recurso MAPI ou o provedor de serviços. Esse método é suportado em todos os objetos de status. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

_ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
_ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a validação. Os sinalizadores a seguir podem ser definidos:
    
ABORT_XP_HEADER_OPERATION
  
> O usuário cancelou a operação, normalmente clicando no botão **Cancelar** na caixa de diálogo correspondente. O objeto de status tem duas opções: 
    
   - Continue trabalhando na operação.
    
   - Pare a operação e retorne MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Uma ou mais das propriedades de configuração do objeto de status foram alteradas. Os clientes podem definir esse sinalizador para permitir que o spooler MAPI corrija dinamicamente falhas críticas do provedor de transporte. 
    
FORCE_XP_CONNECT 
  
> O objeto de status deve executar uma conexão. Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a conexão ocorre sem armazenamento em cache.
    
FORCE_XP_DISCONNECT 
  
> O objeto de status deve executar uma operação de desconexão. Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a desconexão ocorre sem armazenamento em cache.
    
PROCESS_XP_HEADER_CACHE 
  
> As entradas na tabela de cache de MSGSTATUS_REMOTE_DOWNLOAD devem ser processadas, todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DOWNLOAD devem ser baixadas e todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DELETE devem ser excluídas. As mensagens que possuem MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE definidas devem ser movidas.
    
REFRESH_XP_HEADER_CACHE 
  
> Para um provedor de transporte remoto, uma nova lista de headers de mensagem deve ser baixada e todos os sinalizadores que marcam o status da mensagem devem ser limpos.
    
SUPPRESS_UI 
  
> Impede que o objeto de status exibir uma interface do usuário como parte da operação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A validação foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento; ela deve ter permissão para ser concluída, ou deve ser interrompida, antes que essa operação seja iniciada.
    
MAPI_E_NO_SUPPORT 
  
> O objeto de status não dá suporte ao método de validação, conforme indicado pela ausência do sinalizador STATUS_VALIDATE_STATE na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação de validação, normalmente clicando no **botão Cancelar** em uma caixa de diálogo. Esse valor é retornado apenas por provedores de transporte remoto. 
    
## <a name="remarks"></a>Comentários

O **método IMAPIStatus::ValidateState** verifica o estado de um recurso associado a um objeto de status. **ValidateState** é o único método na interface [IMAPIStatus](imapistatusimapiprop.md) necessário para todos os objetos de status. O comportamento exato desse método depende da implementação. A tabela a seguir descreve a implementação de cada um dos diferentes tipos de objetos de status. 
  
|**Objeto Status**|Implementação de ValidateState**|
|:-----|:-----|
|Subsistema MAPI  <br/> |Valida o estado de todos os recursos que os provedores de serviços ativos no momento e o próprio subsistema possui.  <br/> |
|Spooler MAPI  <br/> |Executa um logon de todos os provedores de transporte, independentemente de eles já estar conectados.  <br/> |
|MapI address book  <br/> |Verifica as entradas em sua seção de perfil.  <br/> |
|Provedor de serviços  <br/> |A implementação depende do tipo de provedor e dos sinalizadores definidos no _parâmetro ulFlags._  <br/> |
   
## <a name="notes-to-implementers"></a>Observações para implementadores

Os aplicativos cliente remotos chamam **o método ValidateState** para iniciar o processamento remoto de várias ações. Esse método existe principalmente para definir bits de status para se comunicar com o spooler MAPI, em vez de realmente fazer qualquer trabalho. Normalmente, o provedor de transporte define sinalizadores em sua linha de status que indicam ao spooler MAPI quais ações precisam ser iniciadas para concluir a solicitação do cliente. 

Nesse modelo de interação client-transport-spooler, as ações solicitadas pelo cliente são assíncronas, pois **ValidateState** retorna antes que as ações solicitadas sejam concluídas. No entanto, ações que não necessariamente envolvem o sistema de mensagens subjacente, ou que envolvem uma interface específica de transporte, podem ser síncronas. O aplicativo cliente passa uma máscara de bits dos sinalizadores a seguir para especificar quais ações o provedor de transporte remoto deve tomar. 
  
ABORT_XP_HEADER_OPERATION 
  
> Se possível, o provedor de transporte remoto deve cancelar qualquer operação que envolva o download de headers. Para fazer isso, o provedor de transporte deve definir os seguintes valores de propriedade na linha de status do objeto de logon:
    
   - Limpe os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) para dizer ao spooler MAPI para interromper o processo de liberação de entrada para este provedor de transporte.
    
   - De definida STATUS_OFFLINE bit na **PR_STATUS_CODE** propriedade. 
    
   - Definir a **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) como VERDADEIRO.
    
   - Definir a **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário.
    
   - Retorne S_OK. No entanto, se a operação em andamento não puder ser cancelada, **ValidateState** deverá retornar MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Um provedor de transporte remoto nunca deve estabelecer uma conexão com um recurso compartilhado (por exemplo, um modem ou porta COM) fora do contexto da interação de transporte spooler MAPI envolvido no método [IXPLogon::FlushQueues.](ixplogon-flushqueues.md) Se **ValidateState** for chamado com esse sinalizador, seu provedor de transporte deverá fazer o seguinte: 
    
   - Definir um sinalizador de status interno para indicar que a conexão remota deve ser estabelecida quando o método **IXPLogon::FlushQueues** for chamado. 
    
   - De definir os valores corretos na tabela de status para fazer com que o spooler MAPI inicie o processo de liberação de filas.
    
   - Quando a liberação de filas estiver concluída, libere o recurso compartilhado.
    
   - Limpe o STATUS_OFFLINE bit na **propriedade PR_STATUS_CODE** trabalho. 
    
   - Retorne S_OK.
    
FORCE_XP_DISCONNECT 
  
> O provedor de transporte remoto deve liberar sua conexão com os recursos do sistema de mensagens. Depois de fazer isso, ele deve definir o STATUS_OFFLINE bit na propriedade **PR_STATUS_CODE** e retornar S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> O provedor de transporte remoto deve processar mensagens remotas e carregar todas as mensagens que tenham sido adiadas. Para fazer isso, o provedor de transporte deve definir os seguintes valores de propriedade na linha de status do objeto de logon:
    
   - De definida **PR_STATUS_STRING** propriedade como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário. 
    
   - De definida STATUS_OUTBOUND_ENABLED bits STATUS_OUTBOUND_ACTIVE bits na **PR_STATUS_CODE** bits. 
    
   - De definida **PR_REMOTE_VALIDATE_OK** propriedade na linha de status do provedor de transporte como FALSE. 
    
   - Se outra operação estiver em andamento (como baixar os headers) quando **ValidateState** for chamado, **ValidateState** deverá retornar MAPI_E_BUSY. 
    
   - Execute o código para processar o sinalizador REFRESH_XP_HEADER_CACHE, também, para atender aos requisitos do cliente Microsoft Exchange.
    
REFRESH_XP_HEADER_CACHE 
  
> O provedor de transporte remoto deve recuperar quaisquer novos headers de mensagens do sistema de mensagens. Para fazer isso, o provedor de transporte deve fazer o seguinte:
    
   - De definida **PR_STATUS_STRING** propriedade como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário. 
    
   - De definida STATUS_INBOUND_ENABLED bits STATUS_INBOUND_ACTIVE bits na **propriedade PR_STATUS_CODE** configuração. 
    
   - Limpe o STATUS_OFFLINE bit na **propriedade PR_STATUS_CODE** trabalho. 
    
   - De definida STATUS_ONLINE bit na **PR_STATUS_CODE** propriedade. 
    
   - De definida **PR_REMOTE_VALIDATE_OK** propriedade na linha de status do provedor de transporte como FALSE. 
    
SHOW_XP_SESSION_UI 
  
> Se o provedor de transporte tiver partes da interface do usuário para processar os headers de mensagem (como uma caixa de diálogo que confirma o download de mensagens), essa caixa de diálogo deverá ser exibida. Caso contrário, **ValidateState** poderá retornar MAPI_E_NO_SUPPORT. 
    
Se qualquer sinalizador diferente desses for passado, **ValidateState** deverá retornar MAPI_E_UNKNOWN_FLAGS. 
  
A chamada do cliente para o provedor de transporte geralmente será para o **método IMAPIStatus::ValidateState.** Durante o processamento de **ValidateState**, o provedor de transporte não deve executar ações que aloquem recursos de sistema fracos, como um modem ou uma porta COM. Isso acontece porque, às vezes, o spooler MAPI precisará liberar filas em mais de um provedor de transporte. No entanto, o cliente pode chamar qualquer método **ValidateState** do provedor de transporte a qualquer momento. Se seu provedor de transporte tentar alocar um recurso fraco durante o processamento de **ValidateState**, um erro pode resultar em conflito com outro provedor de transporte que o spooler MAPI instrutou para liberar suas filas. Se você permitir que todas as alocações de recursos desaquedos ocorram sob a direção do spooler MAPI, poderá evitar esses conflitos. Seu provedor de transporte deve dar suporte à propriedade **PR_REMOTE_VALIDATE_OK** para que os aplicativos cliente possam detectar quando seu provedor de transporte está ocupado ou aguardando o spooler MAPI iniciar uma ação. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como esse método pode fazer com que outras chamadas potencialmente longas sejam feitas, **ValidateState** pode retornar MAPI_E_BUSY para informá-lo de que esse método está aguardando a conclusão de outra operação. Você deve aguardar até que a operação pendente seja concluída antes de tentar outra tarefa. 
  
Você tem mais controle sobre suas chamadas para objetos de status do provedor de transporte. Você pode passar um ou mais sinalizadores para **ValidateState** que afetam as operações do provedor de transporte. Por exemplo, o ABORT_XP_HEADER_OPERATION sinalizador indica que o usuário cancelou a validação. Os provedores de transporte podem optar por cancelar, retornar MAPI_E_USER_CANCELED ou podem continuar. 
  
Você pode definir o sinalizador CONFIG_CHANGED em uma chamada para o objeto de status de um provedor de serviços ou o spooler MAPI para indicar que uma opção de configuração foi alterada. Você pode usar o CONFIG_CHANGED para reconfigurar dinamicamente um provedor de transporte. Quando você CONFIG_CHANGED em uma chamada para o objeto de status de um provedor de serviços, o provedor responde com uma chamada para [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) para alertar o spooler MAPI da alteração. Quando você CONFIG_CHANGED em uma chamada para o objeto de status do spooler MAPI, o spooler chama [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para cada provedor de transporte ativo. **AddressTypes** informa ao spooler MAPI os tipos de endereço com suporte de um transporte. Alguns provedores de serviços também exibem um indicador de progresso se a validação demorar muito. Exibir um indicador de progresso é útil, mas não necessário. 
  
Quando o SUPPRESS_UI sinalizador estiver definido, nenhuma das folhas de propriedades de configuração ou caixas de diálogo de progresso poderá ser exibida. 
  
## <a name="see-also"></a>Confira também

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Propriedade canônica PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)
- [Propriedade canônica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
- [Propriedade canônica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
- [Propriedade canônica PidTagStatusString](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

