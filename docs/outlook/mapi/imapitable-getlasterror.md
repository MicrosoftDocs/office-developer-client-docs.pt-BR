---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418999"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior na tabela. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
> [in] HRESULT que contém o erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> [in] Máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres retornadas. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na **estrutura MAPIERROR** retornadas no parâmetro  _lppMAPIError_ estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Ponteiro para um ponteiro para a **estrutura MAPIERROR** retornada contendo informações de versão, componente e contexto para o erro. O  _parâmetro lppMAPIError_ pode ser definido como NULL se uma estrutura **MAPIERROR** com informações apropriadas não puder ser fornecida. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação só dá suporte a Unicode.
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::GetLastError** retorna informações detalhadas, se disponíveis, sobre uma chamada de método anterior que falhou. Essas informações podem ser exibidas em uma mensagem ou em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **GetLastError** sempre que precisar exibir informações sobre um erro para o usuário. 
  
Você pode usar a estrutura [MAPIERROR](mapierror.md) apontada pelo parâmetro  _lppMAPIError_ se o objeto table fornece um somente se **GetLastError** retornar S_OK. Às vezes, a implementação da tabela não pode determinar qual foi o último erro ou não tem mais nada a relatar sobre o erro. Nessa situação, o ponteiro em  _lppMAPIError_ é definido como NULL. 
  
Para liberar toda a memória alocada para a **estrutura MAPIERROR,** chame a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
Para obter mais informações sobre **o método GetLastError,** consulte [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

