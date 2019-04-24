---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316553"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera os endereços das funções de alocação e desalocação de memória MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Parâmetros

 _lppAllocateBuffer_
  
> bota Um ponteiro para um ponteiro para a função **MAPIAllocateBuffer** . **MAPIAllocateBuffer** aloca memória. 
    
 _lppAllocateMore_
  
> bota Um ponteiro para um ponteiro para a função **MAPIAllocateMore** . **MAPIAllocateMore** aloca memória adicional para a memória que foi originalmente alocada usando o **MAPIAllocateBuffer**.
    
 _lppFreeBuffer_
  
> bota Um ponteiro para um ponteiro para a função **MAPIFreeBuffer** . **MAPIFreeBuffer** libera memória. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os endereços da função foram retornados com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: GetMemAllocRoutines** é implementado para todos os objetos de suporte. Os provedores de serviços chamam o **GetMemAllocRoutines** para obter os endereços das três funções de alocação de memória que são passadas para a função de inicialização ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)ou [XPProviderInit](xpproviderinit.md)). 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

