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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 595d5fdba28634b038838921102d3125135452a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767243"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**Aplica-se a**: Outlook 
  
Marca um objeto como não utilizável.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> Reservado; deve ser zero.
    
 _lpObject_
  
> [in] Um ponteiro para o objeto a ser invalidado. A interface do objeto deve ser derivada de **IUnknown**.
    
 _ulRefCount_
  
> [in] Contagem de referência presente do objeto.
    
 _cMethods_
  
> [in] A contagem de métodos em vtable do objeto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O objeto foi marcado como não utilizável com êxito.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::MakeInvalid** é implementado para todos os objetos de suporte. O objeto a ser invalidado deve ser derivado da interface **IUnknown** ou de uma interface derivada de **IUnknown**.
  
 **MakeInvalid** marca um objeto como não utilizável, substituindo vtable do objeto com uma vtable stub do tamanho semelhante, no qual os métodos **AddRef** e **IUnknown:: Release** executam conforme o esperado. No entanto, quaisquer outros métodos falharem, retornando o valor MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Provedores de serviço e serviços de mensagem normalmente chama **MakeInvalid** no horário de desligamento. No entanto, **MakeInvalid** pode ser chamado a qualquer momento. Por exemplo, se um cliente libera um objeto sem liberar alguns dos seus subobjetos, você pode chamar **MakeInvalid** imediatamente para liberar esses subobjetos. 
  
Você deve possuir o objeto que você tente invalidar. Ela deve ter pelo menos de 16 bytes e ter pelo menos três métodos em seu vtable. 
  
Você pode chamar **MakeInvalid** e, em seguida, executar qualquer desligamento trabalho, como descartar estruturas de dados associados, que geralmente é feito durante a versão de um objeto. Código de suporte para o objeto não precisa ser mantido na memória, porque o MAPI libera a memória chamando [MAPIFreeBuffer](mapifreebuffer.md) e depois libera o objeto. Você pode liberar recursos, chamar **MakeInvalid**e, em seguida, ignorar o objeto invalidado. 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

