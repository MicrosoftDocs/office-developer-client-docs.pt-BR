---
title: Iniciar um servidor de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 87299ce4335492a744dd4ee965b4f8b85bcedc84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564889"
---
# <a name="launching-a-form-server"></a>Iniciar um servidor de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A série de interações que ocorre quando um formulário é carregado do armazenamento persistente (ou seja, a partir de uma biblioteca de formulários) exibir uma mensagem é da seguinte maneira:
  
1. O cliente de mensagens obtém o status da mensagem, sinalizadores de mensagem e classe de mensagem da mensagem. Esta etapa é opcional. Se essas partes de dados não forem fornecidos na etapa 2, o gerente de formulário será recuperá-las.
    
2. O cliente de mensagens chama [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) com a mensagem de destino. 
    
3. O gerente do formulário carrega o servidor de formulário da biblioteca de formulários apropriado. Se o servidor de formulário para a mensagem de destino não estiver instalado, o gerente de formulário instala arquivos executáveis do formulário, também.
    
4. O Gerenciador de formulário chama [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) no objeto de formulário para obter o objeto de formulário [IMAPIForm: IUnknown](imapiformiunknown.md) e [IPersistMessage: IUnknown](ipersistmessageiunknown.md) interfaces. 
    
5. O Gerenciador de formulário chama [IPersistMessage::Load](ipersistmessage-load.md) com a mensagem interfaces de site e mensagem do objeto visualizador. 
    
6. O objeto form chama de volta para o método de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) do cliente de mensagens. 
    
7. O gerente do formulário chama o formulário método do objeto [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) com a interface de contexto do modo de exibição a partir do cliente de mensagens. 
    
8. O objeto form chama de volta para o método de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) do cliente de mensagens. 
    
9. O objeto form chama de volta para o método de [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) do cliente de mensagens. 
    
10. O cliente de mensagens chama o formulário método do objeto [IMAPIForm::Advise](imapiform-advise.md) com o modo de exibição interfaces de contexto do objeto visualizador e o objeto de site de mensagem. 
    
11. O cliente de mensagens chama o formulário método do objeto [IMAPIForm::DoVerb](imapiform-doverb.md) . 
    
12. O objeto form cria sua interface de usuário, se necessário e interage com o usuário.
    
## <a name="see-also"></a>Confira também



[Interações do servidor de formulário](form-server-interactions.md)

