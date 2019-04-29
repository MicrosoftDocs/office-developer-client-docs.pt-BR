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
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419587"
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
  
> no Um ponteiro para o nome do perfil a ser excluído.
    
 _ulFlags_
  
> no Sempre nulo. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O perfil foi excluído com êxito.
    
MAPI_E_NOT_FOUND 
  
> O perfil especificado não existe.
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin::D eleteprofile** exclui um perfil. Se o perfil a ser excluído estiver em uso quando **DeleteProfile** for chamado, **DeleteProfile** retornará S_OK, mas não excluirá o perfil imediatamente. Em vez disso, o **DeleteProfile** marca o perfil para exclusão e o exclui depois que ele não está mais sendo usado, quando todas as sessões ativas terminam. 
  
A função de ponto de entrada para cada serviço de mensagens no perfil é chamada com o valor MSG_SERVICE_DELETE definido no parâmetro _ulContext_ . Primeiro, a função exclui o serviço e, em seguida, exclui a seção de perfil do serviço. A função de ponto de entrada do serviço de mensagem não é chamada novamente depois que o serviço é excluído. 
  
Nenhuma senha é necessária para excluir um perfil.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI usa o método **IProfAdmin::D eleteprofile** para excluir o perfil selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

