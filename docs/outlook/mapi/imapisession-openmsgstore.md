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
ms.openlocfilehash: fdf75787153f9a85e6a7bcddff44cf2c468a7975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595031"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um armazenamento de mensagens e retorna um ponteiro de [IMsgStore](imsgstoreimapiprop.md) para obter mais acesso. 
  
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
  
> [in] Um identificador para a janela do pai da caixa de diálogo endereço comuns e outros relacionados a exibe.
    
_cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
_lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do repositório de mensagem a ser aberto. O parâmetro _lpEntryID_ não deve ser NULL. 
    
_lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface a ser usado para acessar o repositório de mensagem. Passar NULL faz com que o parâmetro _lppMDB_ retornar um ponteiro para a interface padrão para um armazenamento de mensagens (**IMsgStore**).
    
_ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto é aberto. Sinalizadores a seguir podem ser usados:
    
  - MAPI_BEST_ACCESS: Solicitações que o armazenamento de mensagens seja aberto com as permissões de rede máximo permitido para o usuário e o cliente máximo permissões do aplicativo. Por exemplo, se o cliente tem a permissão de leitura/gravação, o armazenamento de mensagens deve ser aberto com permissão de leitura/gravação; Se o cliente tem a permissão somente leitura, o armazenamento de mensagens deve ser aberto com permissão somente leitura. 
      
  - MAPI_DEFERRED_ERRORS: Permite **OpenMsgStore** retornar com êxito, possivelmente antes da mensagem repositório é totalmente disponível para o cliente da chamada. Se o armazenamento de mensagens não estiver disponível, fazendo uma chamada do objeto subsequente pode gerar um erro. 
      
  - MDB\_NO_DIALOG: impede a exibição das caixas de diálogo de logon. Se esse sinalizador estiver definido e **OpenMsgStore** tem informações de configuração insuficiente para abrir o armazenamento de mensagens sem a Ajuda do usuário, ele retornará MAPI_E_LOGON_FAILED. Se esse sinalizador não estiver definido, o provedor de armazenamento de mensagens pode solicitar o usuário para corrigir um nome ou a senha ou para executar outras ações necessárias para estabelecer uma conexão para o armazenamento de mensagens. 
      
  - MDB\_NO_MAIL: O armazenamento de mensagens não deve ser usado para envio ou recebimento de email. Quando esse sinalizador estiver definido, MAPI não notificar o spooler MAPI que este armazenamento de mensagens está sendo aberto.
      
  - MDB\_ONLINE: no modo cache do Exchange, um provedor de cliente ou serviço pode chamar esse método com MDB_ONLINE para substituir a conexão ao repositório de mensagem local e abrir o repositório de servidor remoto. Você não pode abrir um repositório do Exchange no modo de cache e no modo em cache não ao mesmo tempo na mesma sessão MAPI. Se você já abriu o armazenamento de mensagens em cache, você deve fechar ou o repositório antes de abri-lo com esse sinalizador ou abra uma nova sessão MAPI, onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.
      
  - MDB_TEMPORARY: Instrui MAPI que o armazenamento de mensagens não é permanente e não deve ser adicionado à tabela de repositório de mensagem. Esse sinalizador é usado para fazer o logon no repositório de mensagem para que informações podem ser recuperadas por meio de programação da seção perfil. 
      
  - MDB_WRITE: Solicitações de leitura/gravação permissão para o armazenamento de mensagens.
    
_lppMDB_
  
> [out] Ponteiro para um ponteiro para o armazenamento de mensagens.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O armazenamento de mensagens foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um armazenamento de mensagens para o qual o usuário tem permissões insuficientes.
    
E_NOT_FOUND 
  
> O armazenamento de mensagens indicado pelo _lpEntryID_ não existe. 
    
MAPI_E_UNKNOWN_CPID 
  
> O servidor não está configurado para oferecer suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> O servidor não está configurado para oferecer suporte a informações de localidade do cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas o provedor de armazenamento de mensagem tem informações de erro disponíveis. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para obter as informações de erro do provedor, chame o método [IMAPISession::GetLastError](imapisession-getlasterror.md) . Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::OpenMsgStore** abre um armazenamento de mensagens específico. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O nível de permissão padrão para repositórios de mensagem é somente leitura. Se você definir o sinalizador MDB_WRITE, você ainda pode não ser concedida permissão de leitura/gravação. Nível de acesso que atribui MAPI para o armazenamento de mensagens depende de seu nível de permissão do final, a mensagem armazenar propriamente dito e o provedor de armazenamento de mensagem. 
  
Se você chamar **OpenMsgStore** para abrir um armazenamento de mensagens com permissão somente leitura, ocorrerá o seguinte: 
  
- O repositório **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) propriedade não terá seu armazenamento\_MODIFY_OK e repositório\_CREATE_OK o conjunto de bits. 
    
- Chamadas para abrir uma das mensagens ou pastas do armazenamento de mensagens usando [IMAPISession::OpenEntry](imapisession-openentry.md) com o sinalizador definido MAPI_MODIFY falhará. 
    
- Chamadas para abrir uma das propriedades de mensagens ou pastas do armazenamento de mensagens usando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com o sinalizador MAPI_MODIFY falhará. 
    
- Falharão chamadas para qualquer um dos seguintes métodos: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Chamadas para os métodos a seguintes irá falhar se o destino da mensagem copiada é somente leitura, se o destino for o mesmo que o armazenamento de mensagens do código-fonte ou outro repositório de somente leitura.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI usa o método **IMAPISession::OpenMsgStore** para abrir um armazenamento de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
- [Usar macros para lidar com erros](using-macros-for-error-handling.md)

