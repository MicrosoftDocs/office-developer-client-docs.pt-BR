---
title: Iniciando um novo formulário de composição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270053"
---
# <a name="launching-a-new-compose-form"></a>Iniciando um novo formulário de composição

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os implementadores de servidor de formulário devem esperar a seguinte sequência de chamadas de método para seus objetos de formulário e servidor de formulário quando um aplicativo cliente abrir uma nova mensagem para composição:
  
1. O aplicativo cliente chama o método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para obter informações de classe sobre a classe de mensagens do servidor de formulário. 
    
2. O aplicativo cliente chama [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) para obter um novo objeto de formulário. 
    
3. O gerenciador de formulário MAPI carrega o servidor de formulário, se ainda não estiver na memória, e obtém uma interface [IMAPIForm](imapiformiunknown.md) do servidor de formulário. 
    
4. O aplicativo cliente assume a interface **IMAPIForm** resultante e chama o método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) para obter a interface [IPersistMessage](ipersistmessageiunknown.md) do objeto. 
    
5. O aplicativo cliente chama o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) para associar o objeto de formulário a [IMessage](imessageimapiprop.md), exibir contexto e avisar objetos sink.
    
6. O aplicativo cliente chama o [método IMAPIForm::D oVerb](imapiform-doverb.md) para invocar o verbo open. 
    
## <a name="see-also"></a>Confira também



[Interações do Servidor de Formulário](form-server-interactions.md)

