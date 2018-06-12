---
title: IMAPIFormContainerGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetLastError
api_type:
- COM
ms.assetid: 04952b51-f005-4933-a1d1-695c6dc736cc
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 399fa54f7120ff72778b89f1122c6852cb15a677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767025"
---
# <a name="imapiformcontainergetlasterror"></a>IMAPIFormContainer::GetLastError

  
  
**Aplica-se a**: Outlook 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior gerado pelo objeto contêiner form. 
  
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
  
> [out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornado que contém informações de versão, componente e contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** para retornar. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e **GetLastError** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **GetLastError** suporta somente Unicode. 
    
## <a name="remarks"></a>Coment�rios

O método **IMAPIFormContainer::GetLastError** fornece informações sobre uma chamada de método anterior que falharam. Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro, incluindo os dados da estrutura de **MAPIERROR** em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode fazer uso do **MAPIERROR** estrutura apontado pelo parâmetro _lppMAPIError_ se MAPI fornece um somente se **GetLastError** Retorna S_OK. Em alguns casos, MAPI não pode determinar o que foi o último erro, ou não tem nada mais a ser relatado sobre o erro. Nessa situação, um ponteiro como NULL é retornado em _lppMAPIError_ , em vez disso. 
  
Para obter mais informações sobre o método **GetLastError** , consulte [Usando erros estendido](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)

