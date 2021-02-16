---
title: Implementando um Visualizador de Formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435814"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="ae7cc-103">Implementando um Visualizador de Formulário</span><span class="sxs-lookup"><span data-stu-id="ae7cc-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="ae7cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae7cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae7cc-105">Um visualizador de formulário inclui três objetos: um site de mensagens, um pia de conselhos de exibição e um contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="ae7cc-106">Cada um desses objetos permite que você interaja com um servidor de formulários e seus formulários.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="ae7cc-107">Um site de mensagens é um objeto que implementa a interface [IMAPIMessageSite : interface IUnknown](imapimessagesiteiunknown.md) e auxilia os servidores de formulário com tarefas como mover, salvar ou excluir mensagens, criar novas mensagens ou iniciar novos servidores de formulário.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="ae7cc-108">Os sites de mensagens são usados por formulários para obter informações sobre o status do cliente em relação a vários provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="ae7cc-109">Por exemplo, um formulário pode usar seu site de mensagens para obter um ponteiro para seu armazenamento de mensagens atual, uma mensagem ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="ae7cc-110">Há dois tipos de métodos na interface **IMAPIMessageSite:**</span><span class="sxs-lookup"><span data-stu-id="ae7cc-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="ae7cc-111">Métodos que fornecem informações para objetos de formulário.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="ae7cc-112">Métodos que manipulam mensagens.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="ae7cc-113">Os métodos que fornecem informações para objetos de formulário são simples de implementar.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="ae7cc-114">Em todos os casos, exceto [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), você já deve ter disponível as informações necessárias para cada método.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="ae7cc-115">Os métodos que manipulam mensagens devem agir como se tivessem sido disparados por meio da interface do usuário normal.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="ae7cc-116">Por exemplo, se um objeto de formulário chamar seu método [IMAPIMessageSite::NewMessage,](imapimessagesite-newmessage.md) comporte-se como se o usuário tivesse optado por redigir uma nova mensagem personalizada com sua interface de usuário normal.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="ae7cc-117">Os comandos que normalmente geram esse comportamento são **Compose**, **Open**, **Reply**, Reply to **All Recipients** e **Forward**.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="ae7cc-118">Um contexto de exibição é um objeto que implementa a interface [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) e fornece servidores de formulário com um contexto para a mensagem atual, permitindo que os servidores alternem facilmente para a mensagem seguinte ou anterior na pasta.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="ae7cc-119">Um formulário usa um contexto de exibição para compartilhar informações.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="ae7cc-120">Com um objeto de contexto de exibição, um formulário pode:</span><span class="sxs-lookup"><span data-stu-id="ae7cc-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="ae7cc-121">Registre-se com seu cliente para receber notificações.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="ae7cc-122">Ative a próxima mensagem ou a mensagem anterior na pasta.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="ae7cc-123">Obter informações de impressão.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-123">Get printing information.</span></span>
    
- <span data-ttu-id="ae7cc-124">Obter o status do seu cliente.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-124">Get your client's status.</span></span>
    
- <span data-ttu-id="ae7cc-125">Obter um fluxo que pode ser usado para salvar a versão de texto de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="ae7cc-126">Semelhante aos métodos na interface [IMAPIMessageSite : IUnknown,](imapimessagesiteiunknown.md) os métodos em **IMAPIViewContext** correlacionam-se com as ações do usuário e os recursos do cliente relacionados ao contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="ae7cc-127">Por exemplo, um contexto de exibição está envolvido na ativação da mensagem seguinte ou anterior, na classificação do conteúdo da pasta e na filtragem do conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="ae7cc-128">Não é importante qual mecanismo você fornece para que os usuários ativem esses recursos, é importante apenas que a semântica desses recursos mapeie bem para os métodos na interface **IMAPIViewContext.**</span><span class="sxs-lookup"><span data-stu-id="ae7cc-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="ae7cc-129">Um sink de aviso de exibição é um objeto que implementa o [IMAPIViewAdviseSink : interface IUnknown](imapiviewadvisesinkiunknown.md) e lida com notificações de servidores de formulário que afetam seu visualizador e ajudam os formulários e visualizadores de formulário a trabalharem juntos.</span><span class="sxs-lookup"><span data-stu-id="ae7cc-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="ae7cc-130">Para obter mais informações, consulte [Enviando e recebendo notificações de formulário.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="ae7cc-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

