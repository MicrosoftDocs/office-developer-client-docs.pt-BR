---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2be5e40de6894b99d9de86423e99dd95a08bc04c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766935"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**Aplica-se a**: Outlook 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de controle de botão anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Par�metros

 _hResult_
  
> [in] Um identificador para o valor de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** que contém informações de versão, componente e contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se o provedor não pode fornecer uma estrutura **MAPIERROR** com as informações apropriadas. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
## <a name="remarks"></a>Coment�rios

Provedores de serviços de implementam o método **IMAPIControl::GetLastError** para fornecer informações sobre uma chamada de método anterior que falharam. MAPI pode dar obter informações detalhadas sobre o erro usuários exibindo os dados da estrutura de **MAPIERROR** em uma caixa de diálogo ou de mensagem. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você não precisará ter informações a serem incluídas na estrutura de **MAPIERROR** para cada erro. Não é possível determinar qual foi o erro anterior. Se você tiver informações, retorne S_OK e os dados apropriados na estrutura **MAPIERROR** . Se nenhuma informação estiver disponível, retornam S_OK e um ponteiro como NULL para o parâmetro _lppMAPIError_ . 
  
Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl: IUnknown](imapicontroliunknown.md)

