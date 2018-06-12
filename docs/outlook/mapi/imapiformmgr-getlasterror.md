---
title: IMAPIFormMgrGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.GetLastError
api_type:
- COM
ms.assetid: 5d908771-ec16-444d-a9b6-44cc75a4d715
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9dcf0154f0f89a7d5446b832799a78752435ff01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767049"
---
# <a name="imapiformmgrgetlasterror"></a>IMAPIFormMgr::GetLastError

  
  
**Aplica-se a**: Outlook 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior gerado pelo objeto Gerenciador de formulário. 
  
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
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornado que contém informações de versão, componente e contexto para o erro. Este parâmetro pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** para retornar. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e **GetLastError** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **GetLastError** suporta somente Unicode. 
    
## <a name="remarks"></a>Coment�rios

O método **IMAPIFormMgr::GetLastError** fornece informações sobre uma chamada de método anterior que falharam. Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro, incluindo os dados da estrutura de **MAPIERROR** em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a estrutura **MAPIERROR** apontada pelo parâmetro _lppMAPIError_ se MAPI fornece um somente se **GetLastError** Retorna S_OK. Em alguns casos, MAPI não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro. Nessa situação, NULL é retornado em _lppMAPIError_ , em vez disso. 
  
Para obter mais informações sobre o método **GetLastError** , consulte [Usando erros estendido](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

