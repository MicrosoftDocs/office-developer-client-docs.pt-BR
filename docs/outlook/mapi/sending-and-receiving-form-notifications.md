---
title: Enviar e receber notificações de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7148383c92b59adb9d3783e079e7c5f28c038eac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588990"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="6e5ad-103">Enviar e receber notificações de formulários</span><span class="sxs-lookup"><span data-stu-id="6e5ad-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="6e5ad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e5ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e5ad-105">Notificações de formulário são usadas em MAPI para facilitar a comunicação tanto contra o formulário para o visualizador, bem como seu visualizador para o formulário.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="6e5ad-106">Formulários enviar notificações para seu visualizador quando um dos seguintes eventos ocorrer:</span><span class="sxs-lookup"><span data-stu-id="6e5ad-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="6e5ad-107">O formulário é fechado.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-107">The form is closed.</span></span>
    
- <span data-ttu-id="6e5ad-108">Uma nova mensagem é carregada no formulário.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="6e5ad-109">Uma operação de salvamento for concluída.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="6e5ad-110">Uma mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-110">A message is sent.</span></span>
    
<span data-ttu-id="6e5ad-111">Cada um desses tipos de eventos corresponde a um método específico no [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), uma das interfaces do visualizador seu formulário deve implementar.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="6e5ad-112">Quando ocorre um evento, as chamadas de formulário, o método **IMAPIViewAdviseSink** correspondente no seu visualizador do coletor de eventos de aviso.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="6e5ad-113">Por exemplo, quando uma nova mensagem é recebida que seu visualizador deve incluir no seu vídeo, o formulário chama seu método [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="6e5ad-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="6e5ad-114">Implementar sua opinião avise o coletor de eventos de forma que faz sentido para sua viewer; Não há nenhuma implementação padrão.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="6e5ad-115">Por exemplo, em **OnNewMessage** , você pode atualizar o modo de exibição de tabela de conteúdo da pasta atual para incluir a mensagem que acabou de chegar.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="6e5ad-116">No [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), o método que é chamado quando você recebe um evento de mensagem enviada, você pode copiar a mensagem enviada para uma pasta de itens enviados.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="6e5ad-117">Formulários recebem a notificação do seu visualizador quando ocorre uma alteração que afeta o formulário e quando você está carregando uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="6e5ad-118">Para notificar um formulário, ligue para um dos métodos de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) ou [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span><span class="sxs-lookup"><span data-stu-id="6e5ad-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="6e5ad-119">Chamada **OnChange** para se comunicar status.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="6e5ad-120">Por exemplo, se o formulário está exibindo o último item em uma pasta, quando uma nova mensagem é recebida, chame **OnChange** com o sinalizador VCSTATUS_NEXT definido para informar o formulário que, agora, há um próximo item.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="6e5ad-121">**OnActivateNext** para o formulário para a chegada de uma nova mensagem de alerta de chamada que ele pode ou não ser capazes de exibir.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="6e5ad-122">Passe a classe de mensagem da mensagem para **OnActivateNext**.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="6e5ad-123">Notificações por um objeto de formulário para o aplicativo cliente são tratadas pela interface de **IMAPIViewAdviseSink** do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="6e5ad-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="6e5ad-124">Para obter mais informações, consulte [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="6e5ad-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

