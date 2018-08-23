---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aa3c010eafeba7908498965bc0491c993a4a9120
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572078"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui um perfil.
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpszProfileName_
  
> [in] Um ponteiro para o nome do perfil a ser excluído.
    
 _ulFlags_
  
> [in] Sempre nulo. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O perfil foi excluído com êxito.
    
E_NOT_FOUND 
  
> O perfil especificado não existe.
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin::DeleteProfile** exclui um perfil. Se o perfil para excluir estiver em uso quando **DeleteProfile** é chamado, **DeleteProfile** Retorna S_OK, mas não exclui o perfil imediatamente. Em vez disso, o **DeleteProfile** marca o perfil para exclusão e exclui-la depois que ele não é mais sendo usado, quando todas as suas sessões ativas tiverem terminado. 
  
A função do ponto de entrada para cada serviço de mensagem no perfil é chamada com o valor MSG_SERVICE_DELETE definido no parâmetro _ulContext_ . Primeiro, a função exclui o serviço e, em seguida, ele exclui a seção de perfil do serviço. A função de ponto de entrada de serviço de mensagem não é chamada novamente depois que o serviço foi excluído. 
  
Nenhuma senha é necessária para excluir um perfil.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI usa o método **IProfAdmin::DeleteProfile** para excluir o perfil selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

