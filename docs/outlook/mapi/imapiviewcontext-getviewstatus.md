---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429010"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera o status atual do visualizador. 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parâmetros

 _lpulStatus_
  
> [out] Ponteiro para uma máscara de bits de sinalizadores que fornece o status do visualizador. Os sinalizadores a seguir podem ser definidos:
    
VCSTATUS_CATEGORY 
  
> Há uma mensagem seguinte ou anterior em outra categoria. 
    
VCSTATUS_DELETE 
  
> O formulário permite que as mensagens sejam removidas. 
    
VCSTATUS_INTERACTIVE 
  
> O formulário deve exibir uma interface do usuário. Se esse sinalizador não estiver definido, o formulário deverá suprimir a exibição de uma interface do usuário mesmo em resposta a um verbo que normalmente faz com que uma interface do usuário seja exibida. 
    
VCSTATUS_MODAL 
  
> O formulário é modal para o visualizador. 
    
VCSTATUS_NEXT 
  
> Há uma próxima mensagem no ponto de vista. 
    
VCSTATUS_PREV 
  
> Há uma mensagem anterior na exibição. 
    
VCSTATUS_READONLY 
  
> A mensagem deve ser aberta no modo somente leitura. As operações excluir, enviar e mover devem ser desabilitadas. 
    
VCSTATUS_UNREAD 
  
> Há uma próxima mensagem não lida ou anterior no visualização.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O status do visualizador foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chamam o método **IMAPIViewContext::GetViewStatus** para determinar se há mais mensagens a serem ativadas em um modo de formulário em uma  ou ambas as direções, ou seja, na direção na qual um comando **Next** ativa mensagens, na direção em que um comando Previous ativa mensagens ou em ambas as direções. O valor apontado pelo parâmetro  _lpulStatus_ é usado para determinar se os sinalizadores VCSTATUS_NEXT e VCSTATUS_PREV são válidos para [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md). Se o sinalizador VCSTATUS_DELETE estiver definido, mas não o sinalizador VCSTATUS_READONLY, a mensagem poderá ser excluída usando o método [IMAPIMessageSite::D eleteMessage.](imapimessagesite-deletemessage.md) 
  
Normalmente, os formulários desabilitam comandos e botões de menu se não são válidos para o contexto do visualizador. Um visualizador pode alertar um formulário para uma alteração no status chamando seu [método IMAPIFormAdviseSink::OnChange.](imapiformadvisesink-onchange.md) 
  
O VCSTATUS_MODAL é definido se o formulário deve ser modal para a janela cujo alça é passada na chamada [IMAPIForm::D oVerb](imapiform-doverb.md) anterior. Se VCSTATUS_MODAL for definida, o formulário poderá usar o thread no qual a chamada **do DoVerb** foi feita até que o formulário seja fechado. Se VCSTATUS_MODAL não estiver definido, o formulário não deve ser modal para essa janela e não deve usar o thread. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI implementa o **método IMAPIViewContext::GetViewStatus** nesta função.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

