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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418019"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um repositório de mensagens e retorna um ponteiro [IMsgStore](imsgstoreimapiprop.md) para mais acesso. 
  
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
  
> [in] Um alça para a janela pai da caixa de diálogo de endereço comum e outras exibições relacionadas.
    
_cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
_lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do armazenamento de mensagens a ser aberto. O  _parâmetro lpEntryID_ não deve ser NULL. 
    
_lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o armazenamento de mensagens. Passar NULL faz com  _que o parâmetro lppMDB_ retorne um ponteiro para a interface padrão para um repositório de mensagens (**IMsgStore**).
    
_ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o objeto é aberto. Os sinalizadores a seguir podem ser usados:
    
  - MAPI_BEST_ACCESS: solicita que o armazenamento de mensagens seja aberto com as permissões máximas de rede permitidas para o usuário e o máximo de permissões de aplicativo cliente. Por exemplo, se o cliente tiver permissão de leitura/gravação, o armazenamento de mensagens deverá ser aberto com permissão de leitura/gravação; se o cliente tiver permissão somente leitura, o armazenamento de mensagens deverá ser aberto com permissão somente leitura. 
      
  - MAPI_DEFERRED_ERRORS: permite que **OpenMsgStore** retorne com êxito, possivelmente antes do repositório de mensagens estar totalmente disponível para o cliente de chamada. Se o armazenamento de mensagens não estiver disponível, fazer uma chamada de objeto subsequente poderá criar um erro. 
      
  - MDB \_ NO_DIALOG: impede a exibição de caixas de diálogo de logon. Se esse sinalizador estiver definido e **OpenMsgStore** tiver informações de configuração insuficientes para abrir o repositório de mensagens sem a ajuda do usuário, ele retornará MAPI_E_LOGON_FAILED. Se esse sinalizador não estiver definido, o provedor do armazenamento de mensagens poderá solicitar que o usuário corrija um nome ou senha ou execute outras ações necessárias para estabelecer uma conexão com o armazenamento de mensagens. 
      
  - MDB \_ NO_MAIL: o armazenamento de mensagens não deve ser usado para envio ou recebimento de emails. Quando esse sinalizador é definido, o MAPI não notifica o spooler MAPI de que esse armazenamento de mensagens está sendo aberto.
      
  - MDB ONLINE: No Modo Cache do Exchange, um cliente ou provedor de serviços pode chamar esse método com o MDB_ONLINE para substituir a conexão com o armazenamento de mensagens local e abrir o armazenamento no servidor \_ remoto. Não é possível abrir um armazenamento do Exchange no modo em cache e no modo não armazenado em cache ao mesmo tempo na mesma sessão MAPI. Se você já tiver aberto o arquivo de cache mensagens, você deve fechar o repositório antes de abri-lo com esse sinalizador ou abrir uma nova sessão MAPI onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.
      
  - MDB_TEMPORARY: instrui o MAPI de que o armazenamento de mensagens não é permanente e não deve ser adicionado à tabela do armazenamento de mensagens. Esse sinalizador é usado para fazer logoff no armazenamento de mensagens para que as informações possam ser recuperadas programaticamente na seção de perfil. 
      
  - MDB_WRITE: solicita permissão de leitura/gravação para o armazenamento de mensagens.
    
_lppMDB_
  
> [out] Ponteiro para um ponteiro do armazenamento de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O armazenamento de mensagens foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um armazenamento de mensagens para o qual o usuário tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> O armazenamento de mensagens indicado  _por lpEntryID_ não existe. 
    
MAPI_E_UNKNOWN_CPID 
  
> O servidor não está configurado para dar suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> O servidor não está configurado para dar suporte às informações de localidade do cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas o provedor do armazenamento de mensagens tem informações de erro disponíveis. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para obter as informações de erro do provedor, chame o [método IMAPISession::GetLastError.](imapisession-getlasterror.md) Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::OpenMsgStore** abre um repositório de mensagens específico. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O nível de permissão padrão para armazenamentos de mensagens é somente leitura. Se você definir o MDB_WRITE de leitura, talvez você ainda não tenha permissão de leitura/gravação. O nível final de acesso que o MAPI atribui ao armazenamento de mensagens depende do nível de permissão, do próprio armazenamento de mensagens e do provedor do armazenamento de mensagens. 
  
Se você chamar **OpenMsgStore** para abrir um repositório de mensagens com permissão somente leitura, ocorrerá o seguinte: 
  
- A propriedade **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do repositório não terá seus bits STORE \_ MODIFY_OK e STORE CREATE_OK \_ definidos. 
    
- As chamadas para abrir uma das mensagens ou pastas do armazenamento de mensagens usando [IMAPISession::OpenEntry](imapisession-openentry.md) com o sinalizador MAPI_MODIFY definido falharão. 
    
- As chamadas para abrir uma das propriedades das mensagens ou pastas do armazenamento de mensagens usando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com o sinalizador MAPI_MODIFY falharão. 
    
- As chamadas para qualquer um dos seguintes métodos falharão: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- As chamadas para os métodos a seguir falharão se o destino da mensagem copiada for somente leitura, se o destino for o mesmo que o armazenamento de mensagens de origem ou se for outro armazenamento somente leitura.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI usa o **método IMAPISession::OpenMsgStore** para abrir um repositório de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
- [Usando macros para tratamento de erros](using-macros-for-error-handling.md)

