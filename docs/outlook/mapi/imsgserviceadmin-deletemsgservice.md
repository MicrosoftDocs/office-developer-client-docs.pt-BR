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
ms.openlocfilehash: e0d3d669982bee309901f913612ac1fb1622e60a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571140"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui um serviço de mensagem de um perfil.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Parâmetros

 _lpuid_
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem a ser excluído. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O serviço de mensagem foi excluído.
    
E_NOT_FOUND 
  
> **MAPIUID** apontado pela _lpuid_ não corresponde a um serviço de mensagem existente. 
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::DeleteMsgService** exclui um serviço de mensagem de um perfil. **DeleteMsgService** remove todas as seções de perfil relacionadas ao serviço de mensagem. 
  
 **DeleteMsgService** executa as seguintes etapas para excluir o serviço de mensagem: 
  
1. Chama a função de ponto de entrada do serviço de mensagem com o parâmetro _ulContext_ definido como MSG_SERVICE_DELETE antes que as seções de perfil são removidas. Isso permite que o serviço de realizar tarefas específicas do serviço. 
    
2. Exclui o serviço de mensagem.
    
3. Exclui a seção de perfil do serviço na mensagem.
    
Função do ponto de entrada do serviço de mensagem não é chamada novamente depois que o serviço foi excluído.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar a estrutura **MAPIUID** para o serviço de mensagem excluir, recupere a coluna de propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagem da tabela de serviço de mensagem. Para obter mais informações, consulte o procedimento descrito no método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **IMsgServiceAdmin::DeleteMsgService** para excluir o serviço selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

