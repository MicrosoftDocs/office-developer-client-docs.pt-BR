---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435576"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro de sessão anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
> [in] Um alça para o valor de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo de cadeia de caracteres retornada. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na **estrutura MAPIERROR** retornadas no parâmetro  _lppMAPIError_ estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para uma **estrutura MAPIERROR** que contém informações de versão, componente e contexto para o erro. O _parâmetro lppMAPIError_ pode ser definido como NULL se MAPI não puder fornecer informações apropriadas para uma **estrutura MAPIERROR.** 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O MAPI_UNICODE sinalizador foi definido e a sessão não dá suporte a Unicode.
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::GetLastError** recupera informações sobre o último erro retornado por uma chamada de método **IMAPISession.** Os clientes podem fornecer aos usuários informações detalhadas sobre o erro incluindo essas informações em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a **estrutura MAPIERROR,** se MAPI fornece uma, apontado pelo parâmetro  _lppMAPIError_ somente se **GetLastError** retornar S_OK. Às vezes, o MAPI não pode determinar qual foi o último erro ou não tem mais nada a relatar sobre o erro. Nesta situação, **GetLastError** retorna um ponteiro para NULL em _lppMAPIError._ 
  
Para obter mais informações sobre o **método GetLastError,** consulte [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[Erros estendidos de MAPI](mapi-extended-errors.md)

