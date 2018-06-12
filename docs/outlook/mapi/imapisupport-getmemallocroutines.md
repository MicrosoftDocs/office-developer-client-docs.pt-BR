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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 782c04d05ea5cea811784b031e8a118a9c08cbb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767249"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Aplica-se a**: Outlook 
  
Recupera os endereços das MAPI memória alocação e desalocação funções ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Par�metros

 _lppAllocateBuffer_
  
> [out] Um ponteiro para um ponteiro para a função **MAPIAllocateBuffer** . **MAPIAllocateBuffer** aloca memória. 
    
 _lppAllocateMore_
  
> [out] Um ponteiro para um ponteiro para a função **MAPIAllocateMore** . **MAPIAllocateMore** aloca memória adicional para memória que foi originalmente alocada usando **MAPIAllocateBuffer**.
    
 _lppFreeBuffer_
  
> [out] Um ponteiro para um ponteiro para a função **MAPIFreeBuffer** . **MAPIFreeBuffer** libera a memória. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os endereços de função foram retornados com êxito.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::GetMemAllocRoutines** é implementado para todos os objetos de suporte. Provedores de serviços de chamarem **GetMemAllocRoutines** para obter os endereços das funções de alocação de três memória que são passados para as suas funções de inicialização ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)ou [XPProviderInit](xpproviderinit.md)). 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

