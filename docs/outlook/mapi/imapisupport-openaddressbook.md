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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e9cd1c7ce0983a47311b2626cc3b40b47748b951
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767266"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**Aplica-se a**: Outlook 
  
Fornece acesso ao catálogo de endereços.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Par�metros

 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o catálogo de endereços. Valores válidos são NULL, indicando que a interface de catálogo de endereços padrão [IAddrBook](iaddrbookimapiprop.md)e IID_IAddrBook.
    
 _ulFlags_
  
> Reservado; deve ser zero.
    
 _lppAdrBook_
  
> [out] Um ponteiro para um ponteiro para o catálogo de endereços.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Acesso ao catálogo de endereços foi fornecido.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas um ou mais provedores de catálogo de endereços não pôde ser carregados. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::OpenAddressBook** é implementado para todos os objetos de suporte de provedor de serviço. Provedores de serviços de mensagem de ligação geralmente estreita armazenam e provedores de transporte, chame **OpenAddressBook** para obter acesso ao catálogo de endereços. O ponteiro **IAddrBook** retornado pode ser usado para uma variedade de tarefas do catálogo de endereços, incluindo a abertura de contêineres de catálogo de endereço, Localizando usuários mensagens e exibindo caixas de diálogo de endereço. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **OpenAddressBook** pode retornar MAPI_W_ERRORS_RETURNED se ele não é possível carregar um ou mais dos provedores de catálogo de endereços no perfil atual. Esse valor é um aviso e a chamada devem ser tratados como bem sucedida. Mesmo que todos os provedores de catálogo de endereços Falha ao carregar, **OpenAddressBook** ainda tiver êxito, retornando MAPI_W_ERRORS_RETURNED e um ponteiro **IAddrBook** no parâmetro _lppAdrBook_ . Como **OpenAddressBook** sempre retorna um ponteiro **IAddrBook** válido, você deve liberá-lo quando terminar de utilizá-lo. 
  
Se um ou mais provedores de catálogo de endereços Falha ao carregar, chame [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para obter uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre os provedores que não é carregado. 
  
## <a name="see-also"></a>Confira também



[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

