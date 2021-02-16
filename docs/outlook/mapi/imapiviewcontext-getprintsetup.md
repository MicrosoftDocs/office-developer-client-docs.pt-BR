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
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425124"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera informações de impressão atuais.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres retornadas. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lppFormPrintSetup_
  
> [out] Ponteiro para um ponteiro para uma estrutura que contém as informações de impressão.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As informações de impressão foram recuperadas com êxito.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chamam o método **IMAPIViewContext::GetPrintSetup** para recuperar informações sobre a instalação da impressora antes de tentar imprimir a mensagem atual. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Aloque **os membros hDevMode** e **hDevName** da estrutura [FORMPRINTSETUP](formprintsetup.md) usando a função **Win32 GlobalAlloc**.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você espera que os membros **hDevMode** e **hDevName** da estrutura **FORMPRINTSETUP** apontados pelo parâmetro  _lppFormPrintSetup_ sejam cadeias de caracteres Unicode, defina  _ulFlags_ como MAPI_UNICODE. Caso contrário, **GetPrintSetup** retornará essas cadeias de caracteres no formato ANSI. 
  
Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**. Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md). 
  
## <a name="see-also"></a>Confira também



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

