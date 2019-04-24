---
title: Enviar e receber notificações de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339708"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="0053b-103">Enviar e receber notificações de formulário</span><span class="sxs-lookup"><span data-stu-id="0053b-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="0053b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0053b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0053b-105">As notificações de formulário são usadas em MAPI para facilitar a comunicação do formulário para o seu visualizador, bem como do seu visualizador para o formulário.</span><span class="sxs-lookup"><span data-stu-id="0053b-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="0053b-106">Os formulários enviam notificações para o seu visualizador quando ocorre um dos seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="0053b-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="0053b-107">O formulário é fechado.</span><span class="sxs-lookup"><span data-stu-id="0053b-107">The form is closed.</span></span>
    
- <span data-ttu-id="0053b-108">Uma nova mensagem é carregada no formulário.</span><span class="sxs-lookup"><span data-stu-id="0053b-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="0053b-109">Uma operação de salvamento foi concluída.</span><span class="sxs-lookup"><span data-stu-id="0053b-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="0053b-110">Uma mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="0053b-110">A message is sent.</span></span>
    
<span data-ttu-id="0053b-111">Cada um desses tipos de eventos corresponde a um método específico no [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), uma das interfaces que seu visualizador de formulários deve implementar.</span><span class="sxs-lookup"><span data-stu-id="0053b-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="0053b-112">Quando ocorre um evento, o formulário chama o método **IMAPIViewAdviseSink** correspondente no coletor de aviso do visualizador.</span><span class="sxs-lookup"><span data-stu-id="0053b-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="0053b-113">Por exemplo, quando uma nova mensagem chega que o seu visualizador deve incluir em sua exibição, o formulário chama o método [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="0053b-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="0053b-114">Implemente seu coletor de aviso de exibição de uma maneira que faz sentido para o seu visualizador; Não há implementação padrão.</span><span class="sxs-lookup"><span data-stu-id="0053b-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="0053b-115">Por exemplo, no **OnNewMessage** , você pode atualizar o modo de exibição da tabela de conteúdo da pasta atual para incluir a mensagem recém-criada.</span><span class="sxs-lookup"><span data-stu-id="0053b-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="0053b-116">Em [IMAPIViewAdviseSink::](imapiviewadvisesink-onsubmitted.md)onsent, o método que é chamado quando você recebe um evento de mensagem enviado, você pode copiar a mensagem enviada para uma pasta Itens enviados.</span><span class="sxs-lookup"><span data-stu-id="0053b-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="0053b-117">Os formulários recebem uma notificação do seu visualizador quando ocorre uma alteração que afeta o formulário e quando você está carregando uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="0053b-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="0053b-118">Para notificar um formulário, chame um dos métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::](imapiformadvisesink-onchange.md) OnChange ou [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md).</span><span class="sxs-lookup"><span data-stu-id="0053b-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="0053b-119">Chamar \*\*\*\* OnChange para comunicar o status.</span><span class="sxs-lookup"><span data-stu-id="0053b-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="0053b-120">Por exemplo, se o formulário estiver exibindo o último item em uma pasta quando uma nova mensagem chegar, \*\*\*\* chame OnChange com o sinalizador VCSTATUS_NEXT definido para informar ao formulário que agora há um próximo item.</span><span class="sxs-lookup"><span data-stu-id="0053b-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="0053b-121">Chamar **OnActivateNext** para alertar o formulário para a chegada de uma nova mensagem que pode ou não ser exibida.</span><span class="sxs-lookup"><span data-stu-id="0053b-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="0053b-122">Passe a classe de mensagem da mensagem para **OnActivateNext**.</span><span class="sxs-lookup"><span data-stu-id="0053b-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="0053b-123">As notificações de um objeto de formulário para o aplicativo cliente são manipuladas pela interface do **IMAPIViewAdviseSink** do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="0053b-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="0053b-124">Para obter mais informações, consulte [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0053b-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

