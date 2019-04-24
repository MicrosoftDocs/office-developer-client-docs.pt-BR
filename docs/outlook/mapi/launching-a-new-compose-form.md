---
title: Iniciar um novo formulário de redação
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
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="f8a81-103">Iniciar um novo formulário de redação</span><span class="sxs-lookup"><span data-stu-id="f8a81-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="f8a81-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8a81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8a81-105">Os implementadores do servidor de formulário devem esperar a seguinte sequência de chamadas de método para o servidor de formulários e os objetos de formulário quando um aplicativo cliente abre uma nova mensagem para compor:</span><span class="sxs-lookup"><span data-stu-id="f8a81-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="f8a81-106">O aplicativo cliente chama o método [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para obter informações de classe sobre a classe de mensagens do servidor de formulários.</span><span class="sxs-lookup"><span data-stu-id="f8a81-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="f8a81-107">O aplicativo cliente chama [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) para obter um novo objeto Form.</span><span class="sxs-lookup"><span data-stu-id="f8a81-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="f8a81-108">O Gerenciador de formulários MAPI carrega o servidor de formulário, se ainda não estiver na memória, e obtém uma interface [IMAPIForm](imapiformiunknown.md) do servidor de formulários.</span><span class="sxs-lookup"><span data-stu-id="f8a81-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="f8a81-109">O aplicativo cliente usa a interface **IMAPIForm** resultante e chama o método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) para obter a interface [IPersistMessage](ipersistmessageiunknown.md) do objeto.</span><span class="sxs-lookup"><span data-stu-id="f8a81-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="f8a81-110">O aplicativo cliente chama o método [IPersistMessage:: InitNew](ipersistmessage-initnew.md) para associar o objeto Form a objetos [IMessage](imessageimapiprop.md), de exibição de contexto e de coletor de aviso.</span><span class="sxs-lookup"><span data-stu-id="f8a81-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="f8a81-111">O aplicativo cliente chama o método [IMAPIForm::D overb](imapiform-doverb.md) para invocar o verbo Open.</span><span class="sxs-lookup"><span data-stu-id="f8a81-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f8a81-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8a81-112">See also</span></span>



[<span data-ttu-id="f8a81-113">InterAções do servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="f8a81-113">Form Server Interactions</span></span>](form-server-interactions.md)

