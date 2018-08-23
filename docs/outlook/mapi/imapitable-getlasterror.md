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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8b7b1db5bcc718858b01f122f53406c885998741
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593813"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) contendo informações sobre o erro anterior na tabela. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
> [in] HRESULT que contém o erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla o tipo das cadeias de caracteres retornadas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Ponteiro para um ponteiro para a estrutura **MAPIERROR** retornado contendo informações de versão, componente e contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não pode ser fornecida uma estrutura **MAPIERROR** com as informações apropriadas. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação só oferece suporte a Unicode.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::GetLastError** retorna informações detalhadas, se estiver disponível, sobre uma chamada de método anterior que falharam. Essas informações podem ser exibidas em uma mensagem ou uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **GetLastError** sempre que for necessário exibir informações sobre um erro ao usuário. 
  
Você pode fazer uso do [MAPIERROR](mapierror.md) estrutura apontado pelo parâmetro _lppMAPIError_ se o objeto table fornece um somente se **GetLastError** Retorna S_OK. Em alguns casos, a implementação de tabela não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro. Nessa situação, o ponteiro do _lppMAPIError_ é definido como NULL. 
  
Para liberar toda a memória alocada para a estrutura **MAPIERROR** , chame a função de [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

