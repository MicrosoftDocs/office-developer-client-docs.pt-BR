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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5bacf3c73ba7f9a7720586c77ee520d289c40e11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766774"
---
# <a name="hresult"></a>HRESULT

  
  
**Aplica-se a**: Outlook 
  
Um valor de 32 bits que é usado para descrever um erro ou aviso.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Coment�rios

O tipo de dados **HRESULT** é o mesmo que o tipo de dados [SCODE](scode.md) . 
  
Um valor **HRESULT** consiste dos seguintes campos: 
  
- Um código de 1 bit indicando a gravidade, onde zero representa sucesso e 1 representa falha.
    
- Um valor de 4 bits reservado.
    
- Um código de 11 bits indicando a responsabilidade para o erro ou aviso, também conhecido como um código de instalações.
    
- Um código de 16 bits, descrevendo o erro ou aviso.
    
A maioria dos métodos de interface MAPI e funções retornam valores **HRESULT** para fornecer a formação da causa detalhadas. Valores **HRESULT** também são amplamente usados nos métodos de interface OLE. OLE fornece várias macros para conversão entre os valores de **HRESULT** e **SCODE** , o tipo de dados comuns outro para tratamento de erros. 
  
> [!NOTE]
> Em MAPI de 64 bits, **HRESULT** ainda é um valor de 32 bits. 
  
Para obter informações sobre o uso OLE dos valores **HRESULT** , consulte a *referência do programador do OLE* . Para obter mais informações sobre o uso desses valores na MAPI, consulte o [Tratamento de erros](error-handling-in-mapi.md) e qualquer um dos seguintes métodos de interface: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>Confira também



[SCODE](scode.md)


[Tipos de dados MAPI](mapi-data-types.md)

