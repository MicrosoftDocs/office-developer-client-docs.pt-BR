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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316657"
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
  
> Serve deve ser zero.
    
 _lpObject_
  
> no Um ponteiro para o objeto a ser invalidado. A interface do objeto deve ser derivada de **IUnknown**.
    
 _ulRefCount_
  
> no A contagem de referência do objeto atual.
    
 _cMethods_
  
> no A contagem de métodos na vtable do objeto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto foi marcado com êxito como inutilizável.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: MakeInvalid** é implementado para todos os objetos de suporte. O objeto a ser invalidado deve ser derivado da interface **IUnknown** ou de uma interface derivada de **IUnknown**.
  
 **MakeInvalid** marca um objeto como inutilizável substituindo a vtable do objeto por um stub vtable de tamanho semelhante em que os métodos **IUnknown:: AddRef** e **IUnknown** : No enTanto, quaisquer outros métodos falham, retornando o valor MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Os provedores de serviços e serviços de mensagens normalmente chamam **MakeInvalid** no momento do desligamento. No enTanto, **MakeInvalid** pode ser chamado a qualquer momento. Por exemplo, se um cliente libera um objeto sem liberar alguns de seus subobjetos, você pode chamar **MakeInvalid** imediatamente para liberar esses subobjetos. 
  
Você deve possuir o objeto que você tentou invalidar. Deve ter pelo menos 16 bytes e ter pelo menos três métodos em sua vtable. 
  
Você pode chamar **MakeInvalid** e, em seguida, executar qualquer trabalho de desligamento, como descartar as estruturas de dados associadas, que geralmente é executada durante o lançamento de um objeto. O código para suportar o objeto não precisa ser mantido na memória porque o MAPI libera a memória chamando [MAPIFreeBuffer](mapifreebuffer.md) e, em seguida, libera o objeto. Você pode liberar recursos, chamar **MakeInvalid**e, em seguida, ignorar o objeto invalidado. 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

