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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438544"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro de objeto de suporte anterior. 
  
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
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo de cadeia de caracteres retornada. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na **estrutura MAPIERROR** retornadas no parâmetro  _lppMAPIError_ estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a **estrutura MAPIERROR** que contém informações de versão, componente e contexto para o erro. O  _parâmetro lppMAPIError_ pode ser definido como NULL se uma estrutura **MAPIERROR** com informações de erro apropriadas não puder ser fornecida. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE padrão foi definido e o MAPI não dá suporte a Unicode ou MAPI_UNICODE não foi definido e MAPI oferece suporte somente a Unicode.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::GetLastError** é implementado para todos os objetos de suporte. Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da **estrutura MAPIERROR** em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar o ponteiro para a **estrutura MAPIERROR,** se MAPI fornece um, no parâmetro  _lppMAPIError_ somente se **GetLastError** retornar S_OK. Às vezes, o MAPI não pode determinar qual foi o último erro ou não tem mais nada a relatar sobre o erro. Nessa situação,  _lppMAPIError retorna_ um ponteiro para NULL. 
  
Para obter mais informações sobre o **método GetLastError,** consulte [MAPI Extended Errors](mapi-extended-errors.md).
  
Para liberar toda a memória alocada por MAPI, chame a função [MAPIFreeBuffer](mapifreebuffer.md) para a **estrutura MAPIERROR** retornada. 
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Erros estendidos de MAPI](mapi-extended-errors.md)

