---
title: IMAPIMessageSiteGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetLastError
api_type:
- COM
ms.assetid: 7ea282d7-388a-4f05-9780-f8dbc5c5d395
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cc4de8aa21d4b3b27bf757389b663ebeff69a9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420735"
---
# <a name="imapimessagesitegetlasterror"></a>IMAPIMessageSite::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre com o objeto site da mensagem. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _And_
  
> no Um HRESULT que contém o valor de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
 _lppMAPIError_
  
> bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada que contém a versão, o componente e informações de contexto para o erro. Esse parâmetro pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** a ser retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH
  
> O sinalizador MAPI_UNICODE foi definido e getLastError não tem suporte para Unicode, ou MAPI_UNICODE não foi definido e **GetLastError** oferece suporte somente para Unicode. **** 
    
## <a name="remarks"></a>Comentários

O método **IMAPIMessageSite:: GetLastError** fornece informações sobre uma chamada de método anterior que falhou. Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da estrutura **MAPIERROR** em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a estrutura **MAPIERROR** indicada pelo parâmetro _LPPMAPIERROR_ se a MAPI fornecer somente um se GetLastError retornar **** S_OK. Às vezes, o MAPI não pode determinar qual é o último erro ou não tem mais a relatar sobre o erro. Nessa situação, um ponteiro para nulo é retornado em _lppMAPIError_ em vez disso. 
  
Para obter mais informações sobre **** o método GetLastError, consulte [usando erros estendidos](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)

