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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 150a0c6eb7efa83f5ff1d12d915351bf5ca9d45a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767380"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**Aplica-se a**: Outlook 
  
Ativa a mensagem anterior ou seguinte na ordem de exibição. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Par�metros

_ulDir_
  
> [in] Sinalizadores de status oferecendo informações sobre a mensagem a ser ativada. Configurações de sinalizador válidos são:
    
  - VCDIR_CATEGORY: O Visualizador deve ativar uma mensagem em outra categoria do modo de exibição. A mensagem a ser ativada é: 
        
    - A primeira mensagem na categoria próxima modo de exibição se esse sinalizador for ed **ou**com VCDIR_NEXT. 
        
    - A última mensagem da categoria do modo de exibição anterior se esse sinalizador for **OR**ed com VCDIR_PREV e a categoria anterior é expandida. 
        
    - A primeira mensagem na categoria exibir anterior se esse sinalizador for **OR**ed com VCDIR_PREV e a categoria anterior não será expandida. Nesse caso, a categoria anterior passa por expansão automática. 
        
  - VCDIR_DELETE: O Visualizador deve ativar a mensagem anterior ou seguinte porque a mensagem atual foi excluída. 
        
  - VCDIR_MOVE: O Visualizador deve ativar a mensagem anterior ou seguinte porque a mensagem atual foi movida. 
        
  - VCDIR_NEXT: O Visualizador deve ativar a próxima mensagem na ordem de exibição. 
        
  - VCDIR_PREV: O Visualizador deve ativar a mensagem anterior na ordem de exibição. 
        
  - VCDIR_UNREAD: O Visualizador deve ativar a mensagem não lida seguinte ou anterior na ordem de exibição. 
    
_prcPosRect_
  
> [in] Ponteiro para um Windows **Retangular** estruturar contendo o tamanho e a posição da janela a ser usado para exibir a mensagem ativada. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A mensagem foi ativada com êxito. 
    
S_FALSE 
  
> A mensagem foi ativada com êxito, mas um tipo diferente de formulário foi aberto no processo.
    
## <a name="remarks"></a>Coment�rios

Objetos de formulário chame o método de **IMAPIViewContext::ActivateNext** para alterar o que mensagem é exibida ao usuário. O valor passado no parâmetro _ulDir_ indica qual mensagem deve ser ativado e, em alguns casos, o motivo. Os sinalizadores VCDIR_NEXT e VCDIR_PREVIOUS correspondem aos usuários, escolha o comando **próximo** ou **anterior** em um modo de exibição, respectivamente. Essas operações geralmente correspondem ao mover para cima ou para baixo uma mensagem na lista do Visualizador de formulário de mensagens. 
  
Os sinalizadores VCDIR_DELETE e VCDIR_MOVE são definidos por [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) e [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) métodos, respectivamente. Implementações desses métodos chamar **ActivateNext** com direção apropriada e, em seguida, executam a operação solicitada na mensagem se a chamada **ActivateNext** não falhou. Visualizadores de formulário normalmente habilitar usuários especificar a direção para mover-se na lista de mensagens. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

A implementação dos [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) torna a mensagem anterior ou seguinte na pasta, dependendo do valor da _ulDir_, a mensagem atual. Após **ActivateNext** retorna, chame [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) para obter um ponteiro para a mensagem recentemente ativada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se **ActivateNext** retorna S_FALSE, ou se uma mensagem atual não estiver presente, execute o procedimento de desligamento normal que deve incluir a chamar o método de [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) do seu formulário. Se for exibida uma mensagem seguinte ou anterior, use o retângulo de janela passado no parâmetro _prcPosRect_ para exibi-la. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI implementa o método **IMAPIViewContext::ActivateNext** nessa função.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

