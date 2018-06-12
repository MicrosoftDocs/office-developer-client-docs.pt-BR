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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 16f091f4d9527cd82ebc1d1eadee2fb55b481929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767607"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**Aplica-se a**: Outlook 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior no objeto form. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Par�metros

 _hResult_
  
> [in] Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura [MAPIERROR](mapierror.md) retornado no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** que contém informações de versão, componente e contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se o formulário será possível fornecer informações apropriadas para uma estrutura **MAPIERROR** . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e o provedor de catálogo de endereços não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e o provedor de catálogo de endereços suporta somente Unicode.
    
## <a name="remarks"></a>Coment�rios

Objetos de formulário implementar o método **IPersistMessage::GetLastError** para fornecer informações sobre uma chamada de método anterior que falharam. Visualizadores de formulário podem fornecer seus usuários com informações detalhadas sobre o erro, incluindo os dados da estrutura de [MAPIERROR](mapierror.md) em uma caixa de diálogo. 
  
Uma chamada para **GetLastError** não afeta o estado do formulário. Quando **GetLastError** retorna, o formulário permanece no estado em que estava antes que a chamada foi feita. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a estrutura **MAPIERROR** , se o formulário fornece um, que é apontado pelo parâmetro _lppMAPIError_ somente se **GetLastError** Retorna S_OK. Em alguns casos, o formulário não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro. Nessa situação, o formulário retorna um ponteiro como NULL em _lppMAPIError_ em vez disso. 
  
Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage: IUnknown](ipersistmessageiunknown.md)

