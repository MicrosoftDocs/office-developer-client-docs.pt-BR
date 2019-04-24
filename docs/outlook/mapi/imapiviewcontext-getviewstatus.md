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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351174"
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
  
> bota Ponteiro para uma bitmask de sinalizadores que fornecem o status do visualizador. Os seguintes sinalizadores podem ser definidos:
    
VCSTATUS_CATEGORY 
  
> Há uma mensagem próxima ou anterior em outra categoria. 
    
VCSTATUS_DELETE 
  
> O formulário permite que as mensagens sejam removidas. 
    
VCSTATUS_INTERACTIVE 
  
> O formulário deve exibir uma interface do usuário. Se esse sinalizador não for definido, o formulário deve suprimir a exibição de uma interface de usuário, mesmo em resposta a um verbo que geralmente faz com que uma interface de usuário seja exibida. 
    
VCSTATUS_MODAL 
  
> O formulário é modal para o visualizador. 
    
VCSTATUS_NEXT 
  
> Há uma próxima mensagem no modo de exibição. 
    
VCSTATUS_PREV 
  
> Há uma mensagem anterior no modo de exibição. 
    
VCSTATUS_READONLY 
  
> A mensagem deve ser aberta no modo somente leitura. As operações excluir, enviar e mover devem ser desabilitadas. 
    
VCSTATUS_UNREAD 
  
> Há uma mensagem não lida seguinte ou anterior no modo de exibição.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O status do visualizador foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

Os objetos Form chamam o método **IMAPIViewContext:: GetViewStatus** para determinar se há mais mensagens a serem ativadas em um modo de exibição de formulário em ambas as direções, na direção na qual um **próximo** comando ativa as mensagens, na direção na qual um comando **anterior** ativa mensagens ou em ambas as direções. O valor apontado pelo parâmetro _lpulStatus_ é usado para determinar se os sinalizadores VCSTATUS_NEXT e VCSTATUS_PREV são válidos para [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md). Se o sinalizador VCSTATUS_DELETE estiver definido, mas não o sinalizador VCSTATUS_READONLY, a mensagem poderá ser excluída usando o método [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) . 
  
Normalmente, os formulários desativam comandos de menu e botões se eles não forem válidos para o contexto do visualizador. Um visualizador pode alertar um formulário para uma alteração no status chamando o método [IMAPIFormAdviseSink::](imapiformadvisesink-onchange.md) OnChange. 
  
O sinalizador VCSTATUS_MODAL é definido se o formulário deve ser modal para a janela cujo identificador é passado no IMAPIForm anterior [::D chamada overb](imapiform-doverb.md) . Se VCSTATUS_MODAL estiver definido, o formulário poderá usar o thread no qual a **** chamada DoVerb foi feita até que o formulário seja fechado. Se VCSTATUS_MODAL não for definido, o formulário não deverá ser modal nesta janela e não deverá usar o thread. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetViewStatus  <br/> |MFCMAPI implementa o método **IMAPIViewContext:: GetViewStatus** nesta função.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

