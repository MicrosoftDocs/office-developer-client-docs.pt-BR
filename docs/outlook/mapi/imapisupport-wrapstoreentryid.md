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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341283"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte um identificador de entrada interna do repositório de mensagens em um identificador de entrada no formato padrão do MAPI.
  
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
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpOrigEntry_ . 
    
 _lpOrigEntry_
  
> no Um ponteiro para o identificador de entrada particular para o repositório de mensagens.
    
 _lpcbWrappedEntry_
  
> bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppWrappedEntry_ . 
    
 _lppWrappedEntry_
  
> bota Um ponteiro para um ponteiro para o identificador de entrada com quebra.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de entrada foi empacotado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: WrapStoreEntryID** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços usam o **WrapStoreEntryID** para que o MAPI gere um identificador de entrada para um repositório de mensagens que quebra o identificador de entrada interna da loja. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando um cliente chama o método [IMAPIProp::](imapiprop-getprops.md) GetProps do repositório de mensagens para recuperar sua propriedade **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)), e seu repositório de mensagens usa um identificador de entrada em um formato privado, chame **WrapStoreEntryID **e retornar o identificador de entrada apontado pelo parâmetro _lppWrappedEntry_ . 
  
As chamadas para os métodos [IMSProvider:: logon](imsprovider-logon.md) e [IMSLogon:: CompareEntryIDs](imslogon-compareentryids.md) sempre obtêm o identificador de entrada privada da loja; a versão empacotada é usada somente entre aplicativos clientes e MAPI. 
  
Libere a memória para o identificador de entrada apontado pelo parâmetro _lppWrappedEntry_ usando a função [MAPIFreeBuffer](mapifreebuffer.md) quando você terminar de usar o identificador de entrada. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

