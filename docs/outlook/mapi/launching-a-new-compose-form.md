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
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="fa08f-103">Iniciando um novo formulário de composição</span><span class="sxs-lookup"><span data-stu-id="fa08f-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="fa08f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa08f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa08f-105">Os implementadores de servidor de formulário devem esperar a seguinte sequência de chamadas de método para seus objetos de formulário e servidor de formulário quando um aplicativo cliente abrir uma nova mensagem para composição:</span><span class="sxs-lookup"><span data-stu-id="fa08f-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="fa08f-106">O aplicativo cliente chama o método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para obter informações de classe sobre a classe de mensagens do servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="fa08f-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="fa08f-107">O aplicativo cliente chama [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) para obter um novo objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="fa08f-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="fa08f-108">O gerenciador de formulário MAPI carrega o servidor de formulário, se ainda não estiver na memória, e obtém uma interface [IMAPIForm](imapiformiunknown.md) do servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="fa08f-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="fa08f-109">O aplicativo cliente assume a interface **IMAPIForm** resultante e chama o método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) para obter a interface [IPersistMessage](ipersistmessageiunknown.md) do objeto.</span><span class="sxs-lookup"><span data-stu-id="fa08f-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="fa08f-110">O aplicativo cliente chama o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) para associar o objeto de formulário a [IMessage](imessageimapiprop.md), exibir contexto e avisar objetos sink.</span><span class="sxs-lookup"><span data-stu-id="fa08f-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="fa08f-111">O aplicativo cliente chama o [método IMAPIForm::D oVerb](imapiform-doverb.md) para invocar o verbo open.</span><span class="sxs-lookup"><span data-stu-id="fa08f-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fa08f-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa08f-112">See also</span></span>



[<span data-ttu-id="fa08f-113">Interações do Servidor de Formulário</span><span class="sxs-lookup"><span data-stu-id="fa08f-113">Form Server Interactions</span></span>](form-server-interactions.md)

