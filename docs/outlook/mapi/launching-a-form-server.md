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
# <a name="launching-a-form-server"></a><span data-ttu-id="e2304-103">Iniciar um servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="e2304-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="e2304-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2304-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2304-105">A série de interações que ocorre quando um formulário é carregado do armazenamento persistente (ou seja, de uma biblioteca de formulários) para exibir uma mensagem é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e2304-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="e2304-106">O cliente de mensagens Obtém a classe de mensagem, os sinalizadores de mensagem e o status da mensagem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e2304-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="e2304-107">Esta etapa é opcional; Se essas partes de dados não forem fornecidas na etapa 2, o gerente de formulários as recuperará.</span><span class="sxs-lookup"><span data-stu-id="e2304-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="e2304-108">O cliente de mensagens chama [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md) com a mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="e2304-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="e2304-109">O gerente de formulário carrega o servidor de formulário da biblioteca de formulários apropriada.</span><span class="sxs-lookup"><span data-stu-id="e2304-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="e2304-110">Se o servidor de formulário da mensagem de destino não estiver instalado, o Gerenciador de formulários também instalará os arquivos executáveis do formulário.</span><span class="sxs-lookup"><span data-stu-id="e2304-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="e2304-111">O Gerenciador de formulários chama [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) no objeto Form para obter as interfaces [IMAPIForm: IUnknown](imapiformiunknown.md) e [IPersistMessage: IUnknown](ipersistmessageiunknown.md) do objeto Form.</span><span class="sxs-lookup"><span data-stu-id="e2304-111">The form manager calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="e2304-112">O Gerenciador de formulários chama [IPersistMessage:: Load](ipersistmessage-load.md) com o site de mensagens e as interfaces de mensagens do objeto visualizador.</span><span class="sxs-lookup"><span data-stu-id="e2304-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="e2304-113">O objeto Form Retorna a chamada para o método [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) do cliente de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e2304-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="e2304-114">O gerente de formulários chama o método [IMAPIForm:: SetViewContext](imapiform-setviewcontext.md) do objeto Form com a interface de contexto de exibição do cliente de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e2304-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="e2304-115">O objeto Form Retorna a chamada para o método [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) do cliente de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e2304-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="e2304-116">O objeto Form Retorna a chamada para o método [IMAPIViewContext:: GetViewStatus](imapiviewcontext-getviewstatus.md) do cliente de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e2304-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="e2304-117">O cliente de mensagens chama o método [IMAPIForm:: Advise](imapiform-advise.md) do objeto Form com as interfaces de contexto de exibição do objeto visualizador e do objeto site da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e2304-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="e2304-118">O cliente de mensagens chama o método IMAPIForm do objeto Form [::D overb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="e2304-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="e2304-119">O objeto Form cria sua interface de usuário, se necessário, e interage com o usuário.</span><span class="sxs-lookup"><span data-stu-id="e2304-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2304-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2304-120">See also</span></span>



[<span data-ttu-id="e2304-121">InterAções do servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="e2304-121">Form Server Interactions</span></span>](form-server-interactions.md)

