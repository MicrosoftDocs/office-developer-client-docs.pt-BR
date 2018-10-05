---
title: Iniciar um novo formulário de redação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391770"
---
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="f93d9-103">Iniciar um novo formulário de redação</span><span class="sxs-lookup"><span data-stu-id="f93d9-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="f93d9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f93d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f93d9-105">Implementadores de servidor do formulário devem esperar que a seguinte sequência de chamadas de método em seus servidores de formulário e objetos de formulário quando um aplicativo cliente abre uma nova mensagem para redigir:</span><span class="sxs-lookup"><span data-stu-id="f93d9-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="f93d9-106">O aplicativo cliente chama o método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para obter informações sobre a classe de mensagem do servidor formulário de classe.</span><span class="sxs-lookup"><span data-stu-id="f93d9-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="f93d9-107">O aplicativo cliente chama [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) para obter um novo objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="f93d9-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="f93d9-108">O gerente de formulário MAPI carrega o servidor de formulário, se ele não ainda estiver na memória e obtém uma interface [IMAPIForm](imapiformiunknown.md) do servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="f93d9-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="f93d9-109">O aplicativo cliente leva a interface **IMAPIForm** resultante e chama o método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) para obter a interface do objeto [IPersistMessage](ipersistmessageiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="f93d9-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="f93d9-110">O aplicativo cliente chama o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) para associar o objeto form [IMessage](imessageimapiprop.md), contexto de modo de exibição e objetos de coletor de eventos de aviso.</span><span class="sxs-lookup"><span data-stu-id="f93d9-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="f93d9-111">O aplicativo cliente chama o método de [IMAPIForm::DoVerb](imapiform-doverb.md) para invocar o verbo open.</span><span class="sxs-lookup"><span data-stu-id="f93d9-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f93d9-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="f93d9-112">See also</span></span>



[<span data-ttu-id="f93d9-113">Interações do servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="f93d9-113">Form Server Interactions</span></span>](form-server-interactions.md)

