---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430445"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte o identificador de entrada interno de um armazenamento de mensagens em um identificador de entrada no formato padrão MAPI.
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a>Parâmetros

 _cbOrigEntry_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpOrigEntry._ 
    
 _lpOrigEntry_
  
> [in] Um ponteiro para o identificador de entrada privada para o armazenamento de mensagens.
    
 _lpcbWrappedEntry_
  
> [out] Um ponteiro para a contagem de byte no identificador de entrada apontado pelo parâmetro _lppWrappedEntry._ 
    
 _lppWrappedEntry_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada com fim.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de entrada foi empacotado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::WrapStoreEntryID** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços usam **WrapStoreEntryID** para que o MAPI gere um identificador de entrada para um repositório de mensagens que quebra o identificador de entrada interno do repositório. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando um cliente chama o método [IMAPIProp::GetProps](imapiprop-getprops.md) do repositório de mensagens para recuperar sua propriedade **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)), e seu repositório de mensagens usa um identificador de entrada em um formato privado, chame **WrapStoreEntryID** e retorne o identificador de entrada apontado pelo parâmetro _lppWrappedEntry._ 
  
Chamadas para os métodos [IMSProvider::Logon](imsprovider-logon.md) e [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) sempre obtém o identificador de entrada privada do armazenamento; a versão empacotada é usada somente entre aplicativos cliente e MAPI. 
  
Liberar a memória para o identificador de entrada apontado pelo parâmetro  _lppWrappedEntry_ usando a função [MAPIFreeBuffer](mapifreebuffer.md) quando terminar de usar o identificador de entrada. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

