---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325764"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um repositório de mensagens e retorna um ponteiro [IMsgStore](imsgstoreimapiprop.md) para obter mais acesso. 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parâmetros

_ulUIParam_
  
> no Uma alça para a janela pai da caixa de diálogo endereço comum e outros vídeos relacionados.
    
_cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
_lpEntryID_
  
> no Um ponteiro para o identificador de entrada do repositório de mensagens a ser aberto. O parâmetro _lpEntryID_ não deve ser nulo. 
    
_lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o repositório de mensagens. Passar NULL faz com que o parâmetro _lppMDB_ retorne um ponteiro para a interface padrão de um repositório de mensagens (**IMsgStore**).
    
_ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o objeto é aberto. Os seguintes sinalizadores podem ser usados:
    
  - MAPI_BEST_ACCESS: solicita que o repositório de mensagens seja aberto com as permissões de rede máximas permitidas para o usuário e as permissões máximas do aplicativo cliente. Por exemplo, se o cliente tiver permissão de leitura/gravação, o repositório de mensagens deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver permissão somente leitura, o repositório de mensagens deverá ser aberto com permissão somente leitura. 
      
  - MAPI_DEFERRED_ERRORS: permite que o **OpenMsgStore** seja retornado com êxito, possivelmente antes que o repositório de mensagens esteja totalmente disponível para o cliente de chamada. Se o repositório de mensagens não estiver disponível, fazer uma chamada de objeto subsequente poderá gerar um erro. 
      
  - MDB\_NO_DIALOG: impede a exibição de caixas de diálogo de logon. Se esse sinalizador estiver definido, e **OpenMsgStore** tiver informações de configuração insuficientes para abrir o repositório de mensagens sem a ajuda do usuário, ele retornará MAPI_E_LOGON_FAILED. Se esse sinalizador não for definido, o provedor do repositório de mensagens poderá solicitar que o usuário corrija um nome ou senha ou execute outras ações necessárias para estabelecer uma conexão com o repositório de mensagens. 
      
  - MDB\_NO_MAIL: o repositório de mensagens não deve ser usado para enviar ou receber emails. Quando esse sinalizador é definido, o MAPI não notifica o spooler MAPI que este repositório de mensagens está sendo aberto.
      
  - MDB\_online: no modo cache do Exchange, um cliente ou provedor de serviços pode chamar esse método com MDB_ONLINE para substituir a conexão ao repositório de mensagens local e abrir o repositório no servidor remoto. Não é possível abrir um repositório do Exchange no modo de cache e no modo não armazenado em cache ao mesmo tempo na mesma sessão MAPI. Se você já tiver aberto o arquivo de cache mensagens, você deve fechar o repositório antes de abri-lo com esse sinalizador ou abrir uma nova sessão MAPI onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.
      
  - MDB_TEMPORARY: instrui o MAPI de que o repositório de mensagens não é permanente e não deve ser adicionado à tabela do repositório de mensagens. Esse sinalizador é usado para fazer logon no repositório de mensagens para que as informações possam ser recuperadas programaticamente da seção perfil. 
      
  - MDB_WRITE: solicita permissão de leitura/gravação para o repositório de mensagens.
    
_lppMDB_
  
> bota Ponteiro para um ponteiro do repositório de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O repositório de mensagens foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um repositório de mensagens para o qual o usuário tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> O repositório de mensagens indicado pelo _lpEntryID_ não existe. 
    
MAPI_E_UNKNOWN_CPID 
  
> O servidor não está configurado para dar suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> O servidor não está configurado para dar suporte às informações de localidade do cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada teve êxito, mas o provedor do repositório de mensagens tem informações de erro disponíveis. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para obter as informações de erro do provedor, chame o método [IMAPISession:: GetLastError](imapisession-getlasterror.md) . Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPISession:: OpenMsgStore** abre um repositório de mensagens específico. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O nível de permissão padrão para repositórios de mensagens é somente leitura. Se você definir o sinalizador MDB_WRITE, ainda poderá não receber permissão de leitura/gravação. O nível final de acesso que o MAPI atribui ao repositório de mensagens depende do seu nível de permissão, do próprio repositório de mensagens e do provedor de armazenamento de mensagens. 
  
Se você chamar **OpenMsgStore** para abrir um repositório de mensagens com permissão somente leitura, ocorrerá o seguinte: 
  
- A propriedade **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) da loja não terá seus bits de\_armazenamento MODIFY_OK e\_Store CREATE_OK definidos. 
    
- As chamadas para abrir uma das mensagens ou pastas do repositório de mensagens usando o [IMAPISession:: OpenEntry](imapisession-openentry.md) com o sinalizador de MAPI_MODIFY falharão. 
    
- Chamadas para abrir uma das propriedades das mensagens ou pastas do repositório de mensagens usando [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) com o sinalizador MAPI_MODIFY falharão. 
    
- As chamadas para qualquer um dos seguintes métodos falharão: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- As chamadas para os seguintes métodos falharão se o destino da mensagem copiada for somente leitura, se o destino for o mesmo que o repositório de mensagens de origem ou se for outro repositório somente leitura.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIStoreFunctions. cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI usa o método **IMAPISession:: OpenMsgStore** para abrir um repositório de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
- [Usando macros para tratamento de erros](using-macros-for-error-handling.md)

