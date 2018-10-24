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
ms.openlocfilehash: e32157f41632b782fbacf87e0411c18d167b4279
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576677"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica que ocorreu uma alteração no status do Visualizador do formulário. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parâmetros

 _ulDir_
  
> [in] Uma bitmask dos sinalizadores que fornece informações sobre a alteração que ocorreu no visualizador e a resposta esperada no formulário. Sinalizadores a seguir podem ser definidos:
    
VCSTATUS_CATEGORY 
  
> Há uma mensagem anterior ou seguinte em outra categoria. 
    
VCSTATUS_INTERACTIVE 
  
> O formulário deve exibir uma interface do usuário. Se esse sinalizador não estiver definida, o formulário deve suprimir exibindo uma interface do usuário, mesmo em resposta a um verbo que geralmente faz com que uma interface de usuário a ser exibido. 
    
VCSTATUS_MODAL 
  
> O formulário deve ser modal para o Visualizador do formulário. 
    
VCSTATUS_NEXT 
  
> Há uma mensagem próxima no Visualizador do formulário. 
    
VCSTATUS_PREV 
  
> Há uma mensagem anterior no Visualizador do formulário. 
    
VCSTATUS_READONLY 
  
> Excluir, enviar e mover as operações devem ser desabilitadas. 
    
VCSTATUS_UNREAD 
  
> Há uma mensagem não lida seguinte ou anterior no Visualizador do formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método **IMAPIFormAdviseSink::OnChange** para notificar o formulário sobre uma alteração no status do visualizador. Geralmente, a única alteração é a definição ou desmarcar o sinalizador VCSTATUS_NEXT ou VCSTATUS_PREVIOUS com base na presença ou ausência de uma mensagem seguinte ou anterior no visualizador. Da mesma forma, a objeto form, em seguida, habilita ou desabilita quaisquer ações seguinte ou anteriores, que ele oferece suporte. 
  
As configurações de VCSTATUS_MODAL e VCSTATUS_INTERACTIVE não é possível alterar em um contexto de modo de exibição após ele ter sido criado.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A implementação específica desse método depende completamente as especificações do formulário. A maioria dos objetos de formulário usar esse método para alterar sua interface do usuário (por exemplo, para habilitar ou desabilitar comandos de menu ou botões para coincidir com o parâmetro de sinalizadores de status do visualizador).
  
## <a name="see-also"></a>Confira também



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

