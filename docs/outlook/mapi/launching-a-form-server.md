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
# <a name="launching-a-form-server"></a><span data-ttu-id="6f676-103">Iniciar um servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="6f676-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="6f676-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f676-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f676-105">A série de interações que ocorre quando um formulário é carregado do armazenamento persistente (ou seja, a partir de uma biblioteca de formulários) exibir uma mensagem é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6f676-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="6f676-106">O cliente de mensagens obtém o status da mensagem, sinalizadores de mensagem e classe de mensagem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f676-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="6f676-107">Esta etapa é opcional. Se essas partes de dados não forem fornecidos na etapa 2, o gerente de formulário será recuperá-las.</span><span class="sxs-lookup"><span data-stu-id="6f676-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="6f676-108">O cliente de mensagens chama [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) com a mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="6f676-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="6f676-109">O gerente do formulário carrega o servidor de formulário da biblioteca de formulários apropriado.</span><span class="sxs-lookup"><span data-stu-id="6f676-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="6f676-110">Se o servidor de formulário para a mensagem de destino não estiver instalado, o gerente de formulário instala arquivos executáveis do formulário, também.</span><span class="sxs-lookup"><span data-stu-id="6f676-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="6f676-111">O Gerenciador de formulário chama [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) no objeto de formulário para obter o objeto de formulário [IMAPIForm: IUnknown](imapiformiunknown.md) e [IPersistMessage: IUnknown](ipersistmessageiunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="6f676-111">The form manager calls [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="6f676-112">O Gerenciador de formulário chama [IPersistMessage::Load](ipersistmessage-load.md) com a mensagem interfaces de site e mensagem do objeto visualizador.</span><span class="sxs-lookup"><span data-stu-id="6f676-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="6f676-113">O objeto form chama de volta para o método de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) do cliente de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6f676-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="6f676-114">O gerente do formulário chama o formulário método do objeto [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) com a interface de contexto do modo de exibição a partir do cliente de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6f676-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="6f676-115">O objeto form chama de volta para o método de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) do cliente de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6f676-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="6f676-116">O objeto form chama de volta para o método de [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) do cliente de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6f676-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="6f676-117">O cliente de mensagens chama o formulário método do objeto [IMAPIForm::Advise](imapiform-advise.md) com o modo de exibição interfaces de contexto do objeto visualizador e o objeto de site de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f676-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="6f676-118">O cliente de mensagens chama o formulário método do objeto [IMAPIForm::DoVerb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="6f676-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="6f676-119">O objeto form cria sua interface de usuário, se necessário e interage com o usuário.</span><span class="sxs-lookup"><span data-stu-id="6f676-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f676-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f676-120">See also</span></span>



[<span data-ttu-id="6f676-121">Interações do servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="6f676-121">Form Server Interactions</span></span>](form-server-interactions.md)

