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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 25c04f8dee012f4985db98df7d1b3ae5536ef6b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767294"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Aplica-se a**: Outlook 
  
Converte o identificador de entrada interna do repositório de uma mensagem para um identificador de entrada no formato padrão MAPI.
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpOrigEntry_ . 
    
 _lpOrigEntry_
  
> [in] Um ponteiro para o identificador de entrada privada para o armazenamento de mensagens.
    
 _lpcbWrappedEntry_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppWrappedEntry_ . 
    
 _lppWrappedEntry_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada com quebra.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O identificador de entrada foi empacotado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::WrapStoreEntryID** é implementado para todos os objetos de suporte de provedor de serviço. Provedores de serviços usam **WrapStoreEntryID** para gerar um identificador de entrada para um armazenamento de mensagens que distribui o identificador de entrada interna da loja MAPI. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando um cliente chama o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de suas mensagens recuperar sua propriedade **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) e seu armazenamento de mensagens usa um identificador de entrada em um formato privado, **WrapStoreEntryID de chamada **e retornar o identificador de entrada apontado pelo parâmetro _lppWrappedEntry_ . 
  
Chamadas para os métodos [IMSProvider::Logon](imsprovider-logon.md) e [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) sempre obtenham o identificador de entrada privada da loja; a versão com quebra é usada apenas entre aplicativos cliente e de MAPI. 
  
Libere a memória para o identificador de entrada apontado pelo parâmetro _lppWrappedEntry_ usando a função [MAPIFreeBuffer](mapifreebuffer.md) quando tiver terminado de usar o identificador de entrada. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

