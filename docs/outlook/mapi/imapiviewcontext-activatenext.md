---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410613"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ativa a mensagem seguinte ou anterior na ordem de exibição. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parâmetros

_ulDir_
  
> [in] Sinalizadores de status que dão informações sobre a mensagem a ser ativada. As configurações de sinalizador válidas são:
    
  - VCDIR_CATEGORY: o visualizador deve ativar uma mensagem em outra categoria do modo de exibição. A mensagem a ser ativada é: 
        
    - A primeira mensagem na categoria de exibição seguinte se esse sinalizador **for OR** com VCDIR_NEXT. 
        
    - A última mensagem na categoria de exibição anterior se esse sinalizador for **OR** com VCDIR_PREV e a categoria anterior for expandida. 
        
    - A primeira mensagem na categoria de exibição anterior se esse sinalizador for **OR** com VCDIR_PREV e a categoria anterior não for expandida. Nesse caso, a categoria anterior passa por expansão automática. 
        
  - VCDIR_DELETE: o visualizador deve ativar a mensagem seguinte ou anterior porque a mensagem atual foi excluída. 
        
  - VCDIR_MOVE: o visualizador deve ativar a mensagem seguinte ou anterior porque a mensagem atual foi movida. 
        
  - VCDIR_NEXT: o visualizador deve ativar a próxima mensagem na ordem de exibição. 
        
  - VCDIR_PREV: o visualizador deve ativar a mensagem anterior na ordem de exibição. 
        
  - VCDIR_UNREAD: o visualizador deve ativar a próxima mensagem não lida ou anterior na ordem de exibição. 
    
_prcPosRect_
  
> [in] Ponteiro para uma estrutura **de RECT** do Windows que contém o tamanho e a posição da janela a ser usada para exibir a mensagem ativada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem foi ativada com êxito. 
    
S_FALSE 
  
> A mensagem foi ativada com êxito, mas um tipo diferente de formulário foi aberto no processo.
    
## <a name="remarks"></a>Comentários

Os objetos de formulário chamam **o método IMAPIViewContext::ActivateNext** para alterar a mensagem exibida para o usuário. O valor passado no  _parâmetro ulDir_ indica qual mensagem deve ser ativada e, em alguns casos, por quê. Os VCDIR_NEXT e VCDIR_PREVIOUS de comando correspondem aos usuários escolhendo  o comando **Próximo** ou Anterior em um visualização, respectivamente. Essas operações geralmente correspondem a mover para cima ou para baixo uma mensagem na lista de mensagens do visualizador de formulário. 
  
Os sinalizadores VCDIR_DELETE e VCDIR_MOVE são definidos pelos métodos [IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) e [IMAPIMessageSite::MoveMessage,](imapimessagesite-movemessage.md) respectivamente. As implementações desses métodos chamam **ActivateNext** com a direção apropriada e, em seguida, executam a operação solicitada na mensagem se a chamada **ActivateNext** não falhar. Visualizadores de formulário normalmente permitem que os usuários especifiquem a direção para mover na lista de mensagens. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Sua implementação de [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) faz a mensagem seguinte ou anterior na pasta, dependendo do valor de  _ulDir_, a mensagem atual. Depois **que ActivateNext** retornar, chame [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) para obter um ponteiro para a mensagem recém-ativada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se **ActivateNext** retornar S_FALSE, ou se uma mensagem atual não estiver presente, execute o procedimento de desligamento normal, que deve incluir chamar o método [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) do formulário. Se uma mensagem seguinte ou anterior for exibida, use o retângulo de janela passado no parâmetro  _prcPosRect_ para exibi-lo. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI implementa o **método IMAPIViewContext::ActivateNext** nesta função.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

