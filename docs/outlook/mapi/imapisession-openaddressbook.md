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
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329418"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre o livro de endereços integrado MAPI, retornando um ponteiro [IAddrBook](iaddrbookimapiprop.md) para mais acesso. 
  
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
  
> [in] Um alça para a janela pai da caixa de diálogo de endereço comum e outras exibições relacionadas.
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o livro de endereços. Passar **nulo** retorna um ponteiro para a interface padrão do livro de endereços, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a abertura do livro de endereços. O sinalizador a seguir pode ser definido:
    
AB_NO_DIALOG 
  
> Suprime a exibição de caixas de diálogo. Se o AB_NO_DIALOG de endereço não estiver definido, os provedores de agendas que contribuem para o livro de endereços integrado poderão solicitar ao usuário as informações necessárias. 
    
 _lppAdrBook_
  
> [out] Um ponteiro para um ponteiro para o livro de endereços.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O livro de endereços foi aberto com êxito.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas os contêineres de um ou mais provedores de agendamento de endereço não puderam ser abertos. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::OpenAddressBook** abre o livro de endereços integrado MAPI, uma coleção dos contêineres de nível superior de todos os provedores de livro de endereços no perfil. O ponteiro retornado no parâmetro  _lppAdrBook_ fornece mais acesso ao conteúdo do livro de endereços. Isso permite que o chamador execute tarefas como abrir contêineres individuais, localizar usuários de mensagens e exibir caixas de diálogo de endereço comuns. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **OpenAddressBook** retornará MAPI_W_ERRORS_RETURNED se não puder carregar um ou mais provedores de lista de endereços no perfil. Este valor é um aviso, não um valor de erro; lidar com ele como você S_OK. **OpenAddressBook** sempre retorna um ponteiro válido no parâmetro  _lppAdrBook,_ independentemente de quantos provedores de agendas falharam ao carregar. Portanto, você deve sempre chamar o método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do livro de endereços em algum momento antes de fazer logon. 
  
Quando **OpenAddressBook** retornar MAPI_W_ERRORS_RETURNED, chame [IMAPISession::GetLastError](imapisession-getlasterror.md) para obter uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre os provedores com falha. Uma única **estrutura MAPIERROR** é retornada que contém informações fornecidas por todos os provedores. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI usa o **método IMAPISession::OpenAddressBook** para obter o livro de endereços integrado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

