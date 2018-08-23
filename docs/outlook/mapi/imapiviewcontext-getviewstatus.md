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
ms.openlocfilehash: 992d51526c45334f6db3738e36994f4bb9c07c6e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572253"
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
  
> [out] Ponteiro para uma bitmask dos sinalizadores fornecendo o status do visualizador. Sinalizadores a seguir podem ser definidos:
    
VCSTATUS_CATEGORY 
  
> Há uma mensagem anterior ou seguinte em outra categoria. 
    
VCSTATUS_DELETE 
  
> O formulário permite mensagens a ser removido. 
    
VCSTATUS_INTERACTIVE 
  
> O formulário deve exibir uma interface do usuário. Se esse sinalizador não estiver definida, o formulário deve suprimir exibindo uma interface do usuário, mesmo em resposta a um verbo que geralmente faz com que uma interface de usuário a ser exibido. 
    
VCSTATUS_MODAL 
  
> O formulário é modal do observador. 
    
VCSTATUS_NEXT 
  
> Há uma mensagem próxima no modo de exibição. 
    
VCSTATUS_PREV 
  
> Há uma mensagem anterior no modo de exibição. 
    
VCSTATUS_READONLY 
  
> A mensagem deve ser aberta no modo somente leitura. Excluir, enviar e mover as operações devem ser desabilitadas. 
    
VCSTATUS_UNREAD 
  
> Há uma mensagem não lida seguinte ou anterior no modo de exibição.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Status do visualizador foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chamar o método **IMAPIViewContext::GetViewStatus** para determinar se há mais mensagens a ser ativada em um modo de formulário em um ou ambas as direções ou seja, na direção na qual um comando **seguida** ativa somente mensagens, além de direção na qual um comando **anterior** ativa mensagens, ou em ambas as direções. O valor apontado pelo parâmetro _lpulStatus_ é usado para determinar se os sinalizadores VCSTATUS_NEXT e VCSTATUS_PREV são válidos para [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md). Se o sinalizador VCSTATUS_DELETE for definido, mas não o sinalizador VCSTATUS_READONLY, e em seguida, a mensagem pode ser excluída, usando o método [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) . 
  
Normalmente, formulários desabilitar comandos de menu e botões se eles não são válidos para o contexto do visualizador. Um visualizador alertando um formulário para uma alteração no status chamando o método [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) . 
  
O sinalizador VCSTATUS_MODAL é definido se o formulário deve ser modal para a janela cujo identificador é passado na chamada [IMAPIForm::DoVerb](imapiform-doverb.md) anterior. Se VCSTATUS_MODAL for definido, o formulário pode usar o thread no qual a chamada **DoVerb** foi feita até que o formulário é fechado. Se VCSTATUS_MODAL não estiver definida, o formulário não deve ser modal a esta janela e não deve usar o segmento. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI implementa o método **IMAPIViewContext::GetViewStatus** nessa função.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

