---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407379"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui um serviço de mensagens de um perfil.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Parâmetros

 _lpuid_
  
> [in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo do serviço de mensagens a ser excluído. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O serviço de mensagens foi excluído.
    
MAPI_E_NOT_FOUND 
  
> O **MAPIUID** apontado por  _lpuid_ não combina com um serviço de mensagens existente. 
    
## <a name="remarks"></a>Comentários

O **método IMsgServiceAdmin::D eleteMsgService** exclui um serviço de mensagem de um perfil. **DeleteMsgService** remove todas as seções de perfil relacionadas ao serviço de mensagens. 
  
 **DeleteMsgService** executa as seguintes etapas para excluir o serviço de mensagens: 
  
1. Chama a função de ponto de entrada do serviço de mensagens com o  _parâmetro ulContext_ definido como MSG_SERVICE_DELETE antes que as seções de perfil sejam removidas. Isso permite que o serviço execute qualquer tarefa específica do serviço. 
    
2. Exclui o serviço de mensagens.
    
3. Exclui a seção de perfil do serviço de mensagens.
    
A função de ponto de entrada do serviço de mensagens não é chamada novamente depois que o serviço é excluído.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar a estrutura **MAPIUID** do serviço de mensagens **a ser** excluído, recupere a coluna da propriedade PR_SERVICE_UID ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagens na tabela de serviço de mensagens. Para obter mais informações, consulte o procedimento descrito no [método IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o **método IMsgServiceAdmin::D eleteMsgService** para excluir o serviço selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

