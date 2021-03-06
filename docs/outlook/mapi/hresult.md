---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435016"
---
# <a name="hresult"></a>HRESULT

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um valor de 32 bits que é usado para descrever um erro ou aviso.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Comentários

O **tipo de dados HRESULT** é o mesmo que o tipo de dados [SCODE.](scode.md) 
  
Um **valor HRESULT** consiste nos seguintes campos: 
  
- Um código de 1 bit indicando gravidade, onde zero representa sucesso e 1 representa falha.
    
- Um valor reservado de 4 bits.
    
- Um código de 11 bits indicando a responsabilidade pelo erro ou aviso, também conhecido como código de recurso.
    
- Um código de 16 bits que descreve o erro ou aviso.
    
A maioria dos métodos e funções de interface MAPI retorna **valores HRESULT** para fornecer uma causa detalhada. **Os valores HRESULT** também são amplamente usados em métodos de interface OLE. O OLE fornece várias macros para conversão entre valores **HRESULT** e **valores SCODE,** outro tipo de dados comum para tratamento de erros. 
  
> [!NOTE]
> Em MAPI de 64 bits, **HRESULT** ainda é um valor de 32 bits. 
  
Para obter informações sobre o uso OLE de **valores HRESULT,** consulte a *Referência do programador OLE.* Para obter mais informações sobre o uso [](error-handling-in-mapi.md) desses valores em MAPI, consulte Tratamento de Erros e qualquer um dos seguintes métodos de interface: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>Confira também



[SCODE](scode.md)


[Tipos de dados MAPI](mapi-data-types.md)

