---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431894"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica que uma alteração ocorreu no status do Visualizador de formulários. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parâmetros

 _ulDir_
  
> no Uma bitmask de sinalizadores que fornece informações sobre a alteração que ocorreu no visualizador e a resposta esperada no formulário. Os seguintes sinalizadores podem ser definidos:
    
VCSTATUS_CATEGORY 
  
> Há uma mensagem próxima ou anterior em outra categoria. 
    
VCSTATUS_INTERACTIVE 
  
> O formulário deve exibir uma interface do usuário. Se esse sinalizador não for definido, o formulário deve suprimir a exibição de uma interface de usuário, mesmo em resposta a um verbo que geralmente faz com que uma interface de usuário seja exibida. 
    
VCSTATUS_MODAL 
  
> O formulário deve ser modal no Visualizador de formulários. 
    
VCSTATUS_NEXT 
  
> Há uma próxima mensagem no Visualizador de formulários. 
    
VCSTATUS_PREV 
  
> Há uma mensagem anterior no Visualizador de formulários. 
    
VCSTATUS_READONLY 
  
> As operações excluir, enviar e mover devem ser desabilitadas. 
    
VCSTATUS_UNREAD 
  
> Há uma mensagem não lida seguinte ou anterior no Visualizador de formulários.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormAdviseSink::** OnChange para notificar o formulário sobre uma alteração no status de um visualizador. Normalmente, a única alteração é definir ou limpar o sinalizador VCSTATUS_NEXT ou VCSTATUS_PREVIOUS com base na presença ou ausência de uma mensagem seguinte ou anterior no visualizador. Portanto, o objeto Form, em seguida, habilita ou desabilita qualquer ação seguinte ou anterior aceita. 
  
As configurações do VCSTATUS_MODAL e do VCSTATUS_INTERACTIVE não podem ser alteradas em um contexto de exibição após sua criação.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A implementação específica desse método depende completamente das especificações do formulário. A maioria dos objetos de formulário usa esse método para alterar sua interface de usuário (por exemplo, para habilitar ou desabilitar comandos de menu ou botões para corresponder ao parâmetro de status de visualizador).
  
## <a name="see-also"></a>Confira também



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

