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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426706"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior no objeto form. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
> [in] Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo de cadeia de caracteres retornada. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na [estrutura MAPIERROR](mapierror.md) retornadas no parâmetro  _lppMAPIError_ estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para uma **estrutura MAPIERROR** que contém informações de versão, componente e contexto para o erro. O _parâmetro lppMAPIError_ pode ser definido como NULL se o formulário não puder fornecer informações apropriadas para uma **estrutura MAPIERROR.** 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE de endereços foi definido e o provedor do address book não oferece suporte a Unicode ou MAPI_UNICODE não foi definido e o provedor de agendas oferece suporte apenas a Unicode.
    
## <a name="remarks"></a>Comentários

Os objetos de formulário implementam o método **IPersistMessage::GetLastError** para fornecer informações sobre uma chamada de método anterior que falhou. Visualizadores de formulário podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da [estrutura MAPIERROR](mapierror.md) em uma caixa de diálogo. 
  
Uma chamada para **GetLastError** não afeta o estado do formulário. Quando **GetLastError** retorna, o formulário permanece no estado em que estava antes da chamada ser feita. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK. Às vezes, o formulário não pode determinar qual foi o último erro ou não tem mais nada a relatar sobre o erro. In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead. 
  
Para obter mais informações sobre **o método GetLastError,** consulte [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

