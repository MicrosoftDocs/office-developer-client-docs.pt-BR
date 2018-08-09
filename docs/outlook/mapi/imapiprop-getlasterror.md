---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 67aa5b3d85de3df659b5aa1a351ec0d1dcf90248
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767142"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Aplica-se a**: Outlook 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
> [in] Um identificador para o código de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que indica o formato para o texto retornado na estrutura **MAPIERROR** apontada pela _lppMAPIError_. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres devem estar no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem estar no formato ANSI.
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** que contém informações de versão, componente e contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma informação de erro para retornar. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> As informações de erro foi retornadas.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp::GetLastError** fornece informações sobre uma chamada de método anterior que falharam. Clientes podem fornecer aos usuários informações detalhadas sobre o erro, incluindo os dados da estrutura de **MAPIERROR** em uma caixa de diálogo. 
  
Todas as implementações de **GetLastError** fornecido pelo MAPI são implementações ANSI, exceto para a implementação de [IAddrBook](iaddrbookimapiprop.md) . O método **GetLastError** incluído **IAddrBook** oferece suporte a Unicode. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Os detalhes de um controle remoto de transporte do provedor de implementação deste método e Cite mensagens que esse método retorna o provedor de transporte, porque as condições de erro específicas que levam a vários valores de HRESULT será diferentes para transporte diferentes provedores.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a estrutura **MAPIERROR** apontada pelo parâmetro _lppMAPIError_ , se **GetLastError** fornece um, apenas se o valor de retorno é S_OK. Às vezes **GetLastError** não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro. Nessa situação, um ponteiro como NULL é retornado em _lppMAPIError_ , em vez disso. 
  
Para liberar a memória para a estrutura **MAPIERROR** , chame a função de [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI estendido erros](mapi-extended-errors.md)

