---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3e641842dd8264c0cd3556c498bd74c77bda32f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577503"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de objeto de suporte anteriores. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
> [in] Um identificador para o valor de erro gerado na chamada do método anterior para o objeto de suporte.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** que contém informações de versão, componente e contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não pode ser fornecida uma estrutura **MAPIERROR** com informações de erro apropriado. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e MAPI não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e Unicode só oferece suporte a MAPI.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::GetLastError** é implementado para todos os objetos de suporte. Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro, incluindo os dados da estrutura de **MAPIERROR** em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar o ponteiro para a estrutura **MAPIERROR** , se o MAPI fornece um, no parâmetro _lppMAPIError_ somente se **GetLastError** Retorna S_OK. Em alguns casos, MAPI não pode determinar qual foi o último erro ou não tem nada mais ao relatório sobre o erro. Nessa situação, _lppMAPIError_ retorna um ponteiro como NULL, em vez disso. 
  
Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).
  
Para liberar toda a memória alocada por MAPI, chame a função de [MAPIFreeBuffer](mapifreebuffer.md) para a estrutura de **MAPIERROR** retornada. 
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[MAPI estendido erros](mapi-extended-errors.md)

