---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 63e3eca4e91e560a28d57f05250264d7e0592142
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587254"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera as informações de impressão atuais.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla o tipo das cadeias de caracteres retornadas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lppFormPrintSetup_
  
> [out] Ponteiro para um ponteiro para uma estrutura que mantém as informações de impressão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As informações de impressão foi recuperadas com êxito.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chame o método **IMAPIViewContext::GetPrintSetup** para recuperar informações sobre a configuração da impressora antes de tentar imprimir a mensagem atual. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Aloca os membros **hDevMode** e **hDevName** da estrutura [FORMPRINTSETUP](formprintsetup.md) usando a função Win32 **GlobalAlloc**.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você espera que os **campos hDevMode** e **hDevName** membros da estrutura **FORMPRINTSETUP** apontado pelo parâmetro _lppFormPrintSetup_ para ser cadeias de caracteres Unicode, defina _ulFlags_ como MAPI_UNICODE. Caso contrário, o **GetPrintSetup** retornará essas cadeias de caracteres em formato ANSI. 
  
Libere os membros **hDevMode** e **hDevName** da estrutura **FORMPRINTSETUP** chamando-se a função Win32 **GlobalFree**. Libere toda a estrutura **FORMPRINTSETUP** chamando [MAPIFreeBuffer](mapifreebuffer.md). 
  
## <a name="see-also"></a>Confira também



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

