---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416878"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso ao catálogo de endereços.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parâmetros

 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o catálogo de endereços. Os valores válidos são nulos, que indicam a interface do catálogo de endereços padrão [IAddrBook](iaddrbookimapiprop.md)e IID_IAddrBook.
    
 _ulFlags_
  
> Serve deve ser zero.
    
 _lppAdrBook_
  
> bota Um ponteiro para um ponteiro para o catálogo de endereços.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O acesso ao catálogo de endereços foi fornecido.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada teve êxito, mas não foi possível carregar um ou mais provedores de catálogo de endereços. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: OpenAddressBook** é implementado para todos os objetos de suporte do provedor de serviços. Provedores de serviços, normalmente armazenamento de mensagens rigidamente acoplado e provedores de transporte, chamam **OpenAddressBook** para obter acesso ao catálogo de endereços. O ponteiro **IAddrBook** retornado pode ser usado para uma variedade de tarefas do catálogo de endereços, incluindo a abertura de contêineres do catálogo de endereços, a localização de usuários de mensagens e a exibição de caixas de diálogo de endereço. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **OpenAddressBook** pode retornar MAPI_W_ERRORS_RETURNED se não for possível carregar um ou mais dos provedores de catálogo de endereços no perfil atual. Este valor é um aviso e você deve tratar a chamada como bem-sucedida. Mesmo que todos os provedores de catálogos de endereços não sejam carregados, o **OpenAddressBook** ainda terá êxito, retornando MAPI_W_ERRORS_RETURNED e um apontador **IAddrBook** no parâmetro _lppAdrBook_ . Como **OpenAddressBook** sempre retorna um ponteiro **IAddrBook** válido, você deve liberá-lo quando terminar de usá-lo. 
  
Se um ou mais provedores de catálogos de endereços não foram carregados, chame [IMAPISupport:: GetLastError](imapisupport-getlasterror.md) para obter uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre os provedores que não foram carregados. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

