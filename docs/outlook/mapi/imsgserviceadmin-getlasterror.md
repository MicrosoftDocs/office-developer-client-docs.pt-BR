---
title: IMsgServiceAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetLastError
api_type:
- COM
ms.assetid: 9e3c8d6e-74be-46a7-94ed-74a969caf165
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 302aebd0be78c833acf4f82d2bb815ba46ae6f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412139"
---
# <a name="imsgserviceadmingetlasterror"></a>IMsgServiceAdmin::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para um objeto de administração de serviço de mensagens. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _And_
  
> no Um tipo de dados HRESULT que contém o valor de erro gerado pela chamada de método anterior.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
 _lppMAPIError_
  
> bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada que contém a versão, o componente e informações de contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** a ser retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e o objeto de administração do serviço de mensagens não tem suporte para Unicode.
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin:: GetLastError** recupera informações sobre o último erro retornado por uma chamada de método [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Os clientes podem fornecer a seus usuários informações detalhadas sobre o erro, incluindo essa informação em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a estrutura **MAPIERROR** , se o MAPI fornecer um, indicado pelo parâmetro _lppMAPIError_ somente se GetLastError retornar **** S_OK. Às vezes, o MAPI não pode determinar o que foi o último erro ou não faz mais para relatar o erro. Nessa situação, **GetLastError** retorna um ponteiro para nulo em _lppMAPIError_ em vez disso. 
  
Para obter mais informações sobre **** o método GetLastError, consulte [usando erros estendidos](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

