---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: d20c8e7432903ef9334f066df31694752384d034
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767202"
---
# <a name="imapisessionshowform"></a>IMAPISession:: ShowForm

  
  
**Aplica-se a**: Outlook 
  
Exibe um formulário.
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a>Par�metros

 _ulUIParam_
  
> [in] Uma alça para a janela pai do formulário.
    
 _lpMsgStore_
  
> [in] Um ponteiro para o armazenamento de mensagens que contém a pasta apontado pelo parâmetro _lpParentFolder_ . 
    
 _lpParentFolder_
  
> [in] Um ponteiro para a pasta na qual a mensagem associada com o parâmetro _ulMessageToken_ foi criada. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a mensagem que é exibida no formulário. O parâmetro _lpInterface_ deve ser NULL ou IID_IMessage. Passagem nula resulta na interface padrão, [IMessage](imessageimapiprop.md), sendo usada. 
    
 _ulMessageToken_
  
> [in] O token que está associado com a mensagem a ser exibido no formulário. O parâmetro _ulMessageToken_ deve ser definido como o conteúdo do parâmetro _lpulMessageToken_ da chamada anterior para [PrepareForm](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> [in] Reservado; deve ser NULL. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como e se a mensagem será salva. Sinalizadores a seguir podem ser definidos:
    
MAPI_NEW_MESSAGE 
  
> A mensagem nunca tiver sido salvo (ou seja, seu método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) tem nunca foi chamado). 
    
MAPI_POST_MESSAGE 
  
> A mensagem deve ser salvo em sua pasta pai. A mensagem não é processada para enviar, mas é postada para a pasta. Se esse sinalizador não estiver definida, a mensagem é copiada para a caixa de saída e é processada para enviar. 
    
 _ulMessageStatus_
  
> [in] Uma bitmask dos sinalizadores copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem associada com o token no parâmetro _ulMessageToken_ . Os sinalizadores fornecem informações sobre o estado da mensagem. 
    
 _ulMessageFlags_
  
> [in] Uma bitmask dos sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem associada com o token no parâmetro _ulMessageToken_ . Esses sinalizadores fornecem mais informações sobre o estado da mensagem. 
    
 _ulAccess_
  
> [in] Um sinalizador que indica o nível de permissão para a mensagem que é exibida no formulário. Essa informação é copiada da propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) da mensagem associada com o token no parâmetro _ulMessageToken_ . 
    
 _lpszMessageClass_
  
> [in] Um ponteiro para a classe de mensagem da mensagem que está sendo exibida no formulário, copiado da propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem associada com o token no parâmetro _ulMessageToken_ . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O formulário foi exibido com êxito.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISession:: ShowForm** exibe um formulário de mensagem que foi preparado pelo método **PrepareForm** . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você deve ter uma única referência à mensagem passada no parâmetro de _lpMessage_ do método **PrepareForm** . 
  
Lembre-se de que as implementações de formulário podem retornar valores de erro diferentes das documentados por MAPI. Se você pode usar estes valores de erro para tomar uma decisão mais precisa da condição de erro, fazê-lo. Caso contrário, lidar com esses erros ocorram conforme você usaria MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI usa o método **IMAPISession:: ShowForm** , junto com o método **PrepareForm** , exiba uma mensagem em um formulário restrito.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

