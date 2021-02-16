---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427490"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Marca um objeto como inutilizável.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> Reservado; deve ser zero.
    
 _lpObject_
  
> [in] Um ponteiro para o objeto a ser invalidado. A interface do objeto deve ser derivada de **IUnknown**.
    
 _ulRefCount_
  
> [in] A contagem de referência presente do objeto.
    
 _cMethods_
  
> [in] A contagem de métodos na vtable do objeto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto foi marcado com êxito como inutilizável.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::MakeInvalid** é implementado para todos os objetos de suporte. O objeto a ser invalidado deve ser derivado da interface **IUnknown** ou de uma interface derivada de **IUnknown**.
  
 **MakeInvalid** marca um objeto como inutilizável substituindo a vtable do objeto por um stub vtable de tamanho semelhante no qual os métodos **IUnknown::AddRef** e **IUnknown::Release** executam conforme o esperado. No entanto, qualquer outro método falhará, retornando o valor MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Provedores de serviços e serviços de mensagens normalmente chamam **MakeInvalid** no momento do desligamento. No entanto, **MakeInvalid** pode ser chamado a qualquer momento. Por exemplo, se um cliente liberar um objeto sem liberar alguns de seus subobjetos, você poderá chamar **MakeInvalid** imediatamente para liberar esses subobjetos. 
  
Você deve possuir o objeto que você tenta invalidar. Ele deve ter pelo menos 16 bytes de comprimento e ter pelo menos três métodos em sua vtable. 
  
Você pode chamar **MakeInvalid** e executar qualquer trabalho de desligamento, como descartar estruturas de dados associadas, que geralmente é feito durante a liberação de um objeto. O código para dar suporte ao objeto não precisa ser mantido na memória, pois o MAPI libera a memória chamando [MAPIFreeBuffer](mapifreebuffer.md) e libera o objeto. Você pode liberar recursos, chamar **MakeInvalid** e ignorar o objeto invalidado. 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

