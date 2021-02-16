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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412524"
---
# <a name="imapisessionshowform"></a>IMAPISession::ShowForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um alça para a janela pai do formulário.
    
 _lpMsgStore_
  
> [in] Um ponteiro para o armazenamento de mensagens que contém a pasta apontada pelo _parâmetro lpParentFolder._ 
    
 _lpParentFolder_
  
> [in] Um ponteiro para a pasta na qual a mensagem associada ao  _parâmetro ulMessageToken_ foi criada. 
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a mensagem exibida no formulário. O  _parâmetro lpInterface_ deve ser NULL ou IID_IMessage. Passar resultados NULL na interface padrão, [IMessage](imessageimapiprop.md), sendo usado. 
    
 _ulMessageToken_
  
> [in] O token associado à mensagem a ser exibida no formulário. O  _parâmetro ulMessageToken_ deve ser definido como o conteúdo do parâmetro  _lpulMessageToken_ da chamada anterior para [IMAPISession::P repareForm](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> [in] Reservado; deve ser NULL. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como e se a mensagem é salva. Os sinalizadores a seguir podem ser definidos:
    
MAPI_NEW_MESSAGE 
  
> A mensagem nunca foi salva (ou seja, seu [método IMAPIProp::SaveChanges](imapiprop-savechanges.md) nunca foi chamado). 
    
MAPI_POST_MESSAGE 
  
> A mensagem deve ser salva em sua pasta pai. A mensagem não é processada para envio, mas é postada na pasta. Se esse sinalizador não estiver definido, a mensagem será copiada para a Caixa de Saída e será processada para envio. 
    
 _ulMessageStatus_
  
> [in] Uma bitmask de sinalizadores copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem associada ao token no _parâmetro ulMessageToken._ Os sinalizadores fornecem informações sobre o estado da mensagem. 
    
 _ulMessageFlags_
  
> [in] Uma bitmask de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem associada ao token no _parâmetro ulMessageToken._ Esses sinalizadores fornecem mais informações sobre o estado da mensagem. 
    
 _ulAccess_
  
> [in] Um sinalizador que indica o nível de permissão para a mensagem exibida no formulário. Essas informações são copiadas da **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) da mensagem associada ao token no _parâmetro ulMessageToken._ 
    
 _lpszMessageClass_
  
> [in] Um ponteiro para a classe de mensagem da mensagem que está sendo exibida no formulário, copiado da propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem associada ao token no parâmetro _ulMessageToken._ 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário foi exibido com êxito.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::ShowForm** exibe um formulário de mensagem que foi preparado pelo **método IMAPISession::P repareForm.** 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você deve ter apenas uma única referência à mensagem passada no parâmetro _lpMessage_ do método **PrepareForm.** 
  
Esteja ciente de que as implementações de formulário podem retornar valores de erro diferentes dos documentados por MAPI. Se você puder usar esses valores de erro para fazer uma determinação mais precisa da condição de erro, faça-o. Caso contrário, lidar com esses erros como você trataria MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI usa o método **IMAPISession::ShowForm,** juntamente com o **método PrepareForm,** para exibir uma mensagem em um formulário modal.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

