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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328995"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior na tabela. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _And_
  
> no HRESULT contendo o erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> no Bitmask dos sinalizadores que controlam o tipo das cadeias de caracteres retornadas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
 _lppMAPIError_
  
> bota Ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada contendo a versão, o componente e informações de contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não for possível fornecer uma estrutura **MAPIERROR** com as informações apropriadas. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação só oferece suporte a Unicode.
    
## <a name="remarks"></a>Comentários

O método imApitable **:: GetLastError** retorna informações detalhadas, se disponíveis, sobre uma chamada de método anterior que falhou. Essas informações podem ser exibidas em uma mensagem ou em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **GetLastError** sempre que precisar exibir informações sobre um erro para o usuário. 
  
Você pode usar a estrutura [MAPIERROR](mapierror.md) apontada pelo parâmetro _lppMAPIError_ se o objeto Table fornecer um somente se GetLastError retornar **** S_OK. Às vezes, a implementação de tabela não pode determinar qual é o último erro ou não é mais relatado sobre o erro. Nessa situação, o ponteiro em _lppMAPIError_ é definido como nulo. 
  
Para liberar toda a memória alocada para a estrutura **MAPIERROR** , chame a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para obter mais informações sobre **** o método GetLastError, consulte [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

