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
  
Indica que ocorreu uma alteração no status do visualizador de formulário. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parâmetros

 _ulDir_
  
> [in] Uma bitmask de sinalizadores que fornece informações sobre a alteração que ocorreu no visualizador e a resposta esperada no formulário. Os sinalizadores a seguir podem ser definidos:
    
VCSTATUS_CATEGORY 
  
> Há uma mensagem seguinte ou anterior em outra categoria. 
    
VCSTATUS_INTERACTIVE 
  
> O formulário deve exibir uma interface do usuário. Se esse sinalizador não estiver definido, o formulário deverá suprimir a exibição de uma interface do usuário, mesmo em resposta a um verbo que normalmente faz com que uma interface do usuário seja exibida. 
    
VCSTATUS_MODAL 
  
> O formulário deve ser modal para o visualizador de formulário. 
    
VCSTATUS_NEXT 
  
> Há uma próxima mensagem no visualizador de formulário. 
    
VCSTATUS_PREV 
  
> Há uma mensagem anterior no visualizador de formulário. 
    
VCSTATUS_READONLY 
  
> As operações excluir, enviar e mover devem ser desabilitadas. 
    
VCSTATUS_UNREAD 
  
> Há uma próxima mensagem não lida ou anterior no visualizador de formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IMAPIFormAdviseSink::OnChange** para notificar o formulário sobre uma alteração no status de um visualizador. Normalmente, a única alteração é definir ou limpar o sinalizador VCSTATUS_NEXT ou VCSTATUS_PREVIOUS com base na presença ou ausência de uma mensagem seguinte ou anterior no visualizador. Da mesma forma, o objeto de formulário habilita ou desabilita qualquer ação seguinte ou anterior a que ele oferece suporte. 
  
As configurações de VCSTATUS_MODAL e VCSTATUS_INTERACTIVE podem mudar em um contexto de exibição após sua criação.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A implementação específica desse método depende completamente das especificidades do formulário. A maioria dos objetos de formulário usa esse método para alterar sua interface do usuário (por exemplo, para habilitar ou desabilitar comandos de menu ou botões para corresponder ao parâmetro de sinalizadores de status do visualizador).
  
## <a name="see-also"></a>Confira também



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

