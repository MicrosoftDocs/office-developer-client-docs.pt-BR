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
ms.openlocfilehash: c8f05707d63f922c9ce22e6e520c6c57e686f884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767197"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**Aplica-se a**: Outlook 
  
Retorna o identificador de entrada do objeto que fornece a identidade principal para a sessão.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada do objeto que fornece a identidade principal.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A identidade principal foi retornada com êxito.
    
MAPI_W_NO_SERVICE 
  
> A chamada foi bem-sucedida, mas não há nenhuma identidade primária para a sessão. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::QueryIdentity** recupera a identidade principal para a sessão atual e retorna o valor através do parâmetro _lppEntryID_ . A identidade principal é um objeto, normalmente um usuário de mensagens, que represente o usuário de uma sessão.  _lppEntryID_ retorna a identidade principal para um objeto [IMailUser](imailuserimapiprop.md) , que também é armazenado à propriedade [PidTagEntryID](pidtagentryid-canonical-property.md) . Você pode usar o valor retornado nos _lppEntryID_ para abrir um objeto **IMailUser** usando [IMAPISession::OpenEntry](imapisession-openentry.md).
  
Embora muitos provedores de serviço em vários serviços de mensagem podem fornecer a identidade principal para uma sessão, MAPI designa um provedor de serviços único. O provedor de serviço que fornece a identidade principal define os seguintes itens:
  
- O sinalizador STATUS_PRIMARY_IDENTITY na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- A propriedade **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- A propriedade **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- A propriedade **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Se o provedor de serviço que fornece a identidade principal pertencer a um serviço de mensagem, os outros provedores de serviço no serviço de mensagem também definir as propriedades PR_IDENTITY. Essas propriedades são publicadas na tabela de status da sessão. 
  
Se possível, **QueryIdentity** retornará o valor da propriedade **PR_IDENTITY_ENTRYID** da linha status marcada com STATUS_PRIMARY_IDENTITY. Se a propriedade **PR_IDENTITY_ENTRYID** estiver falta da linha principal de identidade, **QueryIdentity** retorna um identificador de entrada únicos criado com outras informações a partir dessa linha. 
  
Se o sinalizador STATUS_PRIMARY_IDENTITY estiver faltando em todas as colunas **PR_RESOURCE_FLAG** na tabela de status, **QueryIdentity** retorna o primeiro identificador de entrada que encontrar. Quando não houver nenhum identificador de entrada apropriada para retornar, **QueryIdentity** tiver êxito com o aviso MAPI_W_NO_SERVICE e aponta _lppEntryID_ para um identificador de entrada codificadas. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode chamar o método [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para atribuir a tarefa de fornecer a identidade de principal da sessão de um serviço de mensagem. 
  
Outra maneira de recuperar a identidade principal é pesquisando a tabela de status da linha com as colunas **PR_RESOURCE_FLAGS** definidas como STATUS_PRIMARY_IDENTITY. Para obter mais informações sobre essa maneira alternativa de recuperar informações de identidade, consulte a [tabela de Status e objetos de Status](status-table-and-status-objects.md).
  
Quando tiver terminado de usar o identificador de entrada para a identidade principal retornada pela **QueryIdentity**, libere seu memória chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para obter mais informações sobre identidade em geral, consulte [Identidade primária de MAPI](mapi-primary-identity.md). 
  
Para obter mais informações sobre como recuperar a identidade de sessão MAPI, consulte [Recuperando primário e o provedor de identidade](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI usa o método **IMAPISession::QueryIdentity** para abrir a entrada do catálogo de endereços para a identidade principal da sessão.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Identidade primária de MAPI](mapi-primary-identity.md)
  
[Recuperar identidade principal e do provedor](retrieving-primary-and-provider-identity.md)
  
[Usar macros para lidar com erros](using-macros-for-error-handling.md)
  
[Tabela de status e objetos de status](status-table-and-status-objects.md)

