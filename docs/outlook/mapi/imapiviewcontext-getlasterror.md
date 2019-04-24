---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bcd8e977d924bae170dcad27c672b963189cfa94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351392"
---
# <a name="imapiviewcontextgetlasterror"></a>IMAPIViewContext::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre com o objeto Context do modo de exibição. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _And_
  
> no Tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> no Bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornado. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
 _lppMAPIError_
  
> bota Ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada que contém a versão, o componente e informações de contexto para o erro. Esse parâmetro pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** a ser retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e **GetLastError** não tem suporte para Unicode, ou MAPI_UNICODE não foi definido, e GetLastError só oferece suporte a Unicode. **** 
    
## <a name="remarks"></a>Comentários

O método **IMAPIViewContext:: GetLastError** fornece informações sobre uma chamada de método anterior que falhou. Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da estrutura **MAPIERROR** em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a estrutura **MAPIERROR** indicada pelo parâmetro _LPPMAPIERROR_ se a MAPI fornecer somente um se GetLastError retornar **** S_OK. Às vezes, o MAPI não pode determinar o que foi o último erro ou não faz mais para relatar o erro. Nessa situação, um ponteiro para nulo é retornado em _lppMAPIError_ em vez disso. 
  
Para obter mais informações sobre **** o método GetLastError, consulte [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

