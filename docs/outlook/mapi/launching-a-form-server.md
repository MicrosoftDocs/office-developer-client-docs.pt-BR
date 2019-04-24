---
title: Iniciar um servidor de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270046"
---
# <a name="launching-a-form-server"></a>Iniciar um servidor de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A série de interações que ocorre quando um formulário é carregado do armazenamento persistente (ou seja, de uma biblioteca de formulários) para exibir uma mensagem é da seguinte maneira:
  
1. O cliente de mensagens Obtém a classe de mensagem, os sinalizadores de mensagem e o status da mensagem da mensagem. Esta etapa é opcional; Se essas partes de dados não forem fornecidas na etapa 2, o gerente de formulários as recuperará.
    
2. O cliente de mensagens chama [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md) com a mensagem de destino. 
    
3. O gerente de formulário carrega o servidor de formulário da biblioteca de formulários apropriada. Se o servidor de formulário da mensagem de destino não estiver instalado, o Gerenciador de formulários também instalará os arquivos executáveis do formulário.
    
4. O Gerenciador de formulários chama [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) no objeto Form para obter as interfaces [IMAPIForm: IUnknown](imapiformiunknown.md) e [IPersistMessage: IUnknown](ipersistmessageiunknown.md) do objeto Form. 
    
5. O Gerenciador de formulários chama [IPersistMessage:: Load](ipersistmessage-load.md) com o site de mensagens e as interfaces de mensagens do objeto visualizador. 
    
6. O objeto Form Retorna a chamada para o método [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) do cliente de mensagens. 
    
7. O gerente de formulários chama o método [IMAPIForm:: SetViewContext](imapiform-setviewcontext.md) do objeto Form com a interface de contexto de exibição do cliente de mensagens. 
    
8. O objeto Form Retorna a chamada para o método [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) do cliente de mensagens. 
    
9. O objeto Form Retorna a chamada para o método [IMAPIViewContext:: GetViewStatus](imapiviewcontext-getviewstatus.md) do cliente de mensagens. 
    
10. O cliente de mensagens chama o método [IMAPIForm:: Advise](imapiform-advise.md) do objeto Form com as interfaces de contexto de exibição do objeto visualizador e do objeto site da mensagem. 
    
11. O cliente de mensagens chama o método IMAPIForm do objeto Form [::D overb](imapiform-doverb.md) . 
    
12. O objeto Form cria sua interface de usuário, se necessário, e interage com o usuário.
    
## <a name="see-also"></a>Confira também



[InterAções do servidor de formulário](form-server-interactions.md)

