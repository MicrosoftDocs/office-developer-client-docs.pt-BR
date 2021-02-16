---
title: Iniciando um servidor de formulário
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
# <a name="launching-a-form-server"></a>Iniciando um servidor de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A série de interações que ocorre quando um formulário é carregado do armazenamento persistente (ou seja, de uma biblioteca de formulário) para exibir uma mensagem é a seguinte:
  
1. O cliente de mensagens obtém a classe de mensagem, sinalizadores de mensagem e status da mensagem da mensagem. Esta etapa é opcional; se essas partes de dados não são fornecidas na etapa 2, o gerenciador de formulário irá recuperá-los.
    
2. O cliente de mensagens chama [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) com a mensagem de destino. 
    
3. O gerenciador de formulário carrega o servidor de formulário a partir da biblioteca de formulário apropriada. Se o servidor de formulário para a mensagem de destino não estiver instalado, o gerenciador de formulário também instalará os arquivos executáveis do formulário.
    
4. O gerenciador de formulário chama [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) no objeto de formulário para obter [o IMAPIForm do](imapiformiunknown.md) objeto de formulário : IUnknown e [IPersistMessage : interfaces IUnknown.](ipersistmessageiunknown.md) 
    
5. O gerenciador de formulário [chama IPersistMessage::Load](ipersistmessage-load.md) com o site de mensagens e as interfaces de mensagem do objeto do visualizador. 
    
6. O objeto de formulário chama de volta para o método [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) do cliente de mensagens. 
    
7. O gerenciador de formulário chama o método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) do objeto de formulário com a interface de contexto de exibição do cliente de mensagens. 
    
8. O objeto form chama de volta para o método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) do cliente de mensagens. 
    
9. O objeto form chama de volta para o método [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) do cliente de mensagens. 
    
10. O cliente de mensagens chama o método [IMAPIForm::Advise](imapiform-advise.md) do objeto de formulário com as interfaces de contexto de exibição do objeto visualizador e o objeto de site de mensagem. 
    
11. O cliente de mensagens chama o método [IMAPIForm::D oVerb do](imapiform-doverb.md) objeto de formulário. 
    
12. O objeto de formulário cria sua interface do usuário, se necessário, e interage com o usuário.
    
## <a name="see-also"></a>Confira também



[Interações do Servidor de Formulário](form-server-interactions.md)

