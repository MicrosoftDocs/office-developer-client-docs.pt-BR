---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428218"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o identificador de entrada do objeto que fornece a identidade principal para a sessão.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de byte no identificador de entrada apontado pelo _parâmetro lppEntryID._ 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada do objeto que fornece a identidade principal.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A identidade principal foi retornada com êxito.
    
MAPI_W_NO_SERVICE 
  
> A chamada foi bem-sucedida, mas não há identidade principal para a sessão. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::QueryIdentity** recupera a identidade principal da sessão atual e retorna o valor por meio do parâmetro _lppEntryID._ A identidade principal é um objeto, normalmente um usuário de mensagens, que representa o usuário de uma sessão.  _LppEntryID_ retorna a identidade principal de um objeto [IMailUser,](imailuserimapiprop.md) que também é armazenado como a [propriedade PidTagEntryID.](pidtagentryid-canonical-property.md) Você pode usar o valor retornado em  _lppEntryID_ para abrir um objeto **IMailUser** usando [IMAPISession::OpenEntry](imapisession-openentry.md).
  
Embora muitos provedores de serviços em vários serviços de mensagem possam fornecer a identidade principal para uma sessão, o MAPI designa um único provedor de serviços. O provedor de serviços que fornece a identidade principal define os seguintes itens:
  
- O STATUS_PRIMARY_IDENTITY sinalizador na **propriedade PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- A **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) .
    
- A **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) .
    
- A **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) .
    
Se o provedor de serviços que fornece a identidade principal pertencer a um serviço de mensagens, os outros provedores de serviços no serviço de mensagens também definirão as PR_IDENTITY propriedades. Essas propriedades são publicadas na tabela de status da sessão. 
  
Se possível, **QueryIdentity** retorna o valor da propriedade **PR_IDENTITY_ENTRYID** da linha de status marcada com STATUS_PRIMARY_IDENTITY. Se a **PR_IDENTITY_ENTRYID** propriedade estiver ausente na linha de identidade primária, **QueryIdentity** retornará um identificador de entrada único criado com outras informações dessa linha. 
  
Se o STATUS_PRIMARY_IDENTITY sinalizador estiver ausente em todas as colunas **PR_RESOURCE_FLAG** na tabela de status, **QueryIdentity** retornará o primeiro identificador de entrada que encontrar. Quando não há identificador de entrada apropriado para retornar, **QueryIdentity** é bem-sucedida com o MAPI_W_NO_SERVICE e aponta  _lppEntryID_ para um identificador de entrada em código. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode chamar o método [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para atribuir a um serviço de mensagem a tarefa de fornecer a identidade principal da sessão. 
  
Outra maneira de recuperar a identidade principal é pesquisando  na tabela de status a linha com PR_RESOURCE_FLAGS colunas definidas como STATUS_PRIMARY_IDENTITY. Para obter mais informações sobre essa maneira alternativa de recuperar informações de identidade, consulte [Status Table and Status Objects](status-table-and-status-objects.md).
  
Quando terminar de usar o identificador de entrada para a identidade principal retornada por **QueryIdentity**, livre sua memória chamando a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
Para obter mais informações sobre identidade em geral, consulte [MAPI Primary Identity](mapi-primary-identity.md). 
  
Para obter mais informações sobre como recuperar a identidade da sessão MAPI, consulte Recuperando a [identidade principal e do provedor.](retrieving-primary-and-provider-identity.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI usa o método **IMAPISession::QueryIdentity** para abrir a entrada do livro de endereços para a identidade principal da sessão.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Identidade Principal MAPI](mapi-primary-identity.md)
  
[Recuperando a identidade principal e do provedor](retrieving-primary-and-provider-identity.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)
  
[Tabela de Status e Objetos de Status](status-table-and-status-objects.md)

