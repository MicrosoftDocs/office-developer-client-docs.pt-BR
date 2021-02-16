---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435828"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
> [in] Um alça para o código de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que indica o formato do texto retornado na estrutura **MAPIERROR** apontado por  _lppMAPIError_. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres devem estar no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, as cadeias de caracteres deverão estar no formato ANSI.
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a **estrutura MAPIERROR** que contém informações de versão, componente e contexto para o erro. O  _parâmetro lppMAPIError_ pode ser definido como NULL se não houver informações de erro a serem retornadas. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As informações de erro foram retornadas.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
## <a name="remarks"></a>Comentários

O **método IMAPIProp::GetLastError** fornece informações sobre uma chamada de método anterior que falhou. Os clientes podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da **estrutura MAPIERROR** em uma caixa de diálogo. 
  
Todas as implementações de **GetLastError** fornecidas pela MAPI são implementações ANSI, exceto para a implementação [de IAddrBook.](iaddrbookimapiprop.md) O **método GetLastError** incluído com **IAddrBook** dá suporte a Unicode. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os detalhes da implementação desse método por um provedor de transporte remoto e as mensagens que esse método retorna são do provedor de transporte, pois as condições de erro específicas que levam a vários valores HRESULT serão diferentes para provedores de transporte diferentes.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a **estrutura MAPIERROR** apontada pelo parâmetro  _lppMAPIError,_ se **GetLastError** fornece um, somente se o valor de retorno for S_OK. Às **vezes, GetLastError** não pode determinar qual foi o último erro ou não tem mais nada a relatar sobre o erro. Nessa situação, um ponteiro para NULL é retornado em _lppMAPIError._ 
  
Para liberar a memória para a **estrutura MAPIERROR,** chame a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
Para obter mais informações sobre o **método GetLastError,** consulte [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Erros estendidos de MAPI](mapi-extended-errors.md)

