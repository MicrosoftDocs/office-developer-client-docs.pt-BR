---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0902aeb71ed66381772a808d21d77edb7e0e2da8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589872"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre o catálogo de endereços integrada de MAPI, retornando um ponteiro [IAddrBook](iaddrbookimapiprop.md) para obter mais acesso. 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um identificador para a janela do pai da caixa de diálogo endereço comuns e outros relacionados a exibe.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o catálogo de endereços. Passar **Nulo** retorna um ponteiro para a interface de padrão do catálogo de endereços, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a abertura do catálogo de endereços. O seguinte sinalizador pode ser definido:
    
AB_NO_DIALOG 
  
> Suprime a exibição das caixas de diálogo. Se o sinalizador AB_NO_DIALOG não estiver definido, os provedores de catálogo de endereços que contribuem para o catálogo de endereços integrada podem solicitar ao usuário de qualquer informação necessária. 
    
 _lppAdrBook_
  
> [out] Um ponteiro para um ponteiro para o catálogo de endereços.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O catálogo de endereços foi aberto com êxito.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas os contêineres de um ou mais provedores de catálogo de endereços não pôde ser abertos. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::OpenAddressBook** abre o catálogo de endereços integrada de MAPI, uma coleção dos contêineres de todos os provedores de catálogo de endereços no perfil de nível superior. O ponteiro retornado no parâmetro _lppAdrBook_ fornece mais acesso ao conteúdo do catálogo de endereços. Isso permite que o chamador realizar tarefas como contêineres individuais de abertura, os usuários de mensagens de localização e exibindo caixas de diálogo comuns do endereço. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **OpenAddressBook** retorna MAPI_W_ERRORS_RETURNED se ele não é possível carregar um ou mais dos provedores de catálogo de endereços no perfil. Esse valor é um aviso, não é um valor de erro; lidar com ele como faria S_OK. **OpenAddressBook** sempre retorna um ponteiro válido no parâmetro _lppAdrBook_ , independentemente de quantos dos provedores de catálogo de endereços a falha ao carregar. Portanto, você sempre deve chamar método de [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) do catálogo de endereços em algum momento antes de fazer logoff. 
  
Quando **OpenAddressBook** retorna MAPI_W_ERRORS_RETURNED, chame [IMAPISession::GetLastError](imapisession-getlasterror.md) para obter uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre os provedores de falha. Uma estrutura **MAPIERROR** única é retornada que contém as informações fornecidas pelo todos os provedores. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI usa o método **IMAPISession::OpenAddressBook** para obter o catálogo de endereços integrada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

