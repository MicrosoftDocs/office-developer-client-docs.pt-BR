---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317161"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior no objeto Form. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _And_
  
> no Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura [MAPIERROR](mapierror.md) retornada no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
 _lppMAPIError_
  
> bota Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** que contém a versão, o componente e informações de contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se o formulário não puder fornecer as informações apropriadas para uma estrutura **MAPIERROR** . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e o provedor de catálogo de endereços não é compatível com Unicode, ou o MAPI_UNICODE não foi definido e o provedor de catálogo de endereços oferece suporte somente a Unicode.
    
## <a name="remarks"></a>Comentários

Os objetos Form implementam o método **IPersistMessage:: GetLastError** para fornecer informações sobre uma chamada de método anterior que falhou. Os visualizadores de formulários podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da estrutura [MAPIERROR](mapierror.md) em uma caixa de diálogo. 
  
Uma chamada para **GetLastError** não afeta o estado do formulário. Quando **GetLastError** retorna, o formulário permanece no estado em que estava antes da chamada ser feita. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a estrutura **MAPIERROR** , se o formulário fornecer um, que será apontado pelo parâmetro _lppMAPIError_ somente se GetLastError retornar S_OK. **** Às vezes, o formulário não pode determinar o que foi o último erro ou não faz mais para relatar o erro. Nessa situação, o formulário retorna um ponteiro para nulo em _lppMAPIError_ em vez disso. 
  
Para obter mais informações sobre **** o método GetLastError, consulte [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

