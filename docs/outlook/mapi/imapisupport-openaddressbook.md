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
  
Fornece acesso ao livro de endereços.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parâmetros

 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o livro de endereços. Os valores válidos são NULL, que indica a interface padrão do livro de endereços [IAddrBook](iaddrbookimapiprop.md)e IID_IAddrBook.
    
 _ulFlags_
  
> Reservado; deve ser zero.
    
 _lppAdrBook_
  
> [out] Um ponteiro para um ponteiro para o livro de endereços.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O acesso ao livro de endereços foi fornecido.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas não foi possível carregar um ou mais provedores de agendamento de endereços. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::OpenAddressBook** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços, normalmente bem próximos de provedores de transporte e de armazenamento de mensagens, chamam **OpenAddressBook** para obter acesso ao livro de endereços. O ponteiro **IAddrBook** retornado pode ser usado para uma variedade de tarefas do livro de endereços, incluindo a abertura de contêineres do livro de endereços, a busca de usuários de mensagens e a exibição de caixas de diálogo de endereço. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **OpenAddressBook** poderá retornar MAPI_W_ERRORS_RETURNED se não puder carregar um ou mais provedores de agendas no perfil atual. Esse valor é um aviso e você deve tratar a chamada como bem-sucedida. Mesmo se todos os provedores de agendamento de endereços falharem ao carregar, **OpenAddressBook** ainda terá êxito, retornando MAPI_W_ERRORS_RETURNED e um ponteiro **IAddrBook** no parâmetro _lppAdrBook._ Como **OpenAddressBook** sempre retorna um ponteiro **IAddrBook** válido, você deve liberá-lo quando terminar de usá-lo. 
  
Se um ou mais provedores de agendamento de endereços falharem ao carregar, chame [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para obter uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre os provedores que não foram carregados. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

