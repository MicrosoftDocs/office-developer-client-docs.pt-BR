---
title: Enviando e recebendo notificações de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431852"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="947c5-103">Enviando e recebendo notificações de formulário</span><span class="sxs-lookup"><span data-stu-id="947c5-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="947c5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="947c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="947c5-105">As notificações de formulário são usadas em MAPI para facilitar a comunicação entre o formulário e o visualizador, bem como do visualizador para o formulário.</span><span class="sxs-lookup"><span data-stu-id="947c5-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="947c5-106">Os formulários enviam notificações ao visualizador quando ocorre um dos seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="947c5-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="947c5-107">O formulário está fechado.</span><span class="sxs-lookup"><span data-stu-id="947c5-107">The form is closed.</span></span>
    
- <span data-ttu-id="947c5-108">Uma nova mensagem é carregada no formulário.</span><span class="sxs-lookup"><span data-stu-id="947c5-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="947c5-109">Uma operação de salvar é concluída.</span><span class="sxs-lookup"><span data-stu-id="947c5-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="947c5-110">Uma mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="947c5-110">A message is sent.</span></span>
    
<span data-ttu-id="947c5-111">Cada um desses tipos de evento corresponde a um método específico em [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), uma das interfaces que o visualizador de formulário deve implementar.</span><span class="sxs-lookup"><span data-stu-id="947c5-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="947c5-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span><span class="sxs-lookup"><span data-stu-id="947c5-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="947c5-113">Por exemplo, quando chega uma nova mensagem que o visualizador deve incluir na exibição, o formulário chama o método [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md)</span><span class="sxs-lookup"><span data-stu-id="947c5-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="947c5-114">Implemente o sink de aconselhador de exibição de uma maneira que faça sentido para o visualizador; não há implementação padrão.</span><span class="sxs-lookup"><span data-stu-id="947c5-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="947c5-115">Por exemplo, em **OnNewMessage,** você pode atualizar a exibição da tabela de conteúdo da pasta atual para incluir a mensagem recém-chegada.</span><span class="sxs-lookup"><span data-stu-id="947c5-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="947c5-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span><span class="sxs-lookup"><span data-stu-id="947c5-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="947c5-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span><span class="sxs-lookup"><span data-stu-id="947c5-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="947c5-118">Para notificar um formulário, chame um dos métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) ou [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span><span class="sxs-lookup"><span data-stu-id="947c5-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="947c5-119">Chame **OnChange** para comunicar o status.</span><span class="sxs-lookup"><span data-stu-id="947c5-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="947c5-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span><span class="sxs-lookup"><span data-stu-id="947c5-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="947c5-121">Chame **OnActivateNext** para alertar o formulário sobre a chegada de uma nova mensagem que ele pode ou não ser capaz de exibir.</span><span class="sxs-lookup"><span data-stu-id="947c5-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="947c5-122">Passe a classe de mensagem da mensagem para **OnActivateNext**.</span><span class="sxs-lookup"><span data-stu-id="947c5-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="947c5-123">As notificações por um objeto de formulário para o aplicativo cliente são manipuladas pela interface **IMAPIViewAdviseSink do** aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="947c5-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="947c5-124">Para obter mais informações, [consulte IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="947c5-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

