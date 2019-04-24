---
title: Implementar um visualizador de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332890"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="bce72-103">Implementar um visualizador de formulários</span><span class="sxs-lookup"><span data-stu-id="bce72-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="bce72-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bce72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bce72-105">Um visualizador de formulários inclui três objetos: um site de mensagens, um coletor de aviso de exibição e um contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="bce72-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="bce72-106">Cada um desses objetos permite interagir com um servidor de formulários e seus formulários.</span><span class="sxs-lookup"><span data-stu-id="bce72-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="bce72-107">Um site de mensagens é um objeto que implementa a interface [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) e ajuda os servidores de formulário com tarefas como mover, salvar ou excluir mensagens, criar novas mensagens ou iniciar novos servidores de formulários.</span><span class="sxs-lookup"><span data-stu-id="bce72-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="bce72-108">Os sites de mensagens são usados por formulários para obter informações sobre o status do seu cliente em relação a vários provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="bce72-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="bce72-109">Por exemplo, um formulário pode usar seu site de mensagens para obter um ponteiro para o repositório de mensagens atual, uma mensagem ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="bce72-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="bce72-110">Há dois tipos de métodos na interface **IMAPIMessageSite** :</span><span class="sxs-lookup"><span data-stu-id="bce72-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="bce72-111">Métodos que fornecem informações para objetos de formulário.</span><span class="sxs-lookup"><span data-stu-id="bce72-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="bce72-112">Métodos que manipulam mensagens.</span><span class="sxs-lookup"><span data-stu-id="bce72-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="bce72-113">Os métodos que fornecem informações a objetos de formulário são simples de implementar.</span><span class="sxs-lookup"><span data-stu-id="bce72-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="bce72-114">Em todos os casos, exceto [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md), você já deve ter disponível as informações exigidas por cada método.</span><span class="sxs-lookup"><span data-stu-id="bce72-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="bce72-115">Os métodos que manipulam mensagens devem atuar como se tivessem sido acionados por meio da interface do usuário normal.</span><span class="sxs-lookup"><span data-stu-id="bce72-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="bce72-116">Por exemplo, se um objeto Form chamar o método [IMAPIMessageSite:: NewMessage](imapimessagesite-newmessage.md) , se comportará como se o usuário tivesse optado por compor uma nova mensagem personalizada com sua interface do usuário normal.</span><span class="sxs-lookup"><span data-stu-id="bce72-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="bce72-117">Comandos que normalmente geram esse comportamento \*\*\*\* são compor, **abrir**, **responder**, **responder a todos os destinatários**e encaminhar. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bce72-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="bce72-118">Um contexto de exibição é um objeto que implementa a interface [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) e fornece servidores de formulário com um contexto para a mensagem atual, permitindo que os servidores alternem facilmente para a mensagem seguinte ou anterior na pasta.</span><span class="sxs-lookup"><span data-stu-id="bce72-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="bce72-119">Um formulário usa um contexto de exibição para compartilhar informações.</span><span class="sxs-lookup"><span data-stu-id="bce72-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="bce72-120">Com um objeto de contexto de exibição, um formulário pode:</span><span class="sxs-lookup"><span data-stu-id="bce72-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="bce72-121">Registre-se em seu cliente para notificações.</span><span class="sxs-lookup"><span data-stu-id="bce72-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="bce72-122">Ativar a mensagem seguinte ou anterior na pasta.</span><span class="sxs-lookup"><span data-stu-id="bce72-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="bce72-123">Obter informações de impressão.</span><span class="sxs-lookup"><span data-stu-id="bce72-123">Get printing information.</span></span>
    
- <span data-ttu-id="bce72-124">Obter o status do cliente.</span><span class="sxs-lookup"><span data-stu-id="bce72-124">Get your client's status.</span></span>
    
- <span data-ttu-id="bce72-125">Obtenha um Stream que pode ser usado para salvar a versão de texto de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bce72-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="bce72-126">Semelhante aos métodos da interface [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) , os métodos no **IMAPIViewContext** se correlacionam com ações do usuário e recursos do cliente relacionados ao contexto do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="bce72-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="bce72-127">Por exemplo, um contexto de exibição está envolvido na ativação da mensagem seguinte ou anterior, classificando o conteúdo da pasta e filtrando o conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="bce72-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="bce72-128">Não é importante qual mecanismo você fornece para que os usuários ativem esses recursos, é importante que a semântica desses recursos seja mapeada bem para os métodos na interface **IMAPIViewContext** .</span><span class="sxs-lookup"><span data-stu-id="bce72-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="bce72-129">Um coletor de aviso de exibição é um objeto que implementa a interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) e manipula notificações de servidores de formulário que afetam o visualizador e formulários de ajuda e visualizadores de formulários para trabalhar juntos.</span><span class="sxs-lookup"><span data-stu-id="bce72-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="bce72-130">Para obter mais informações, consulte [envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="bce72-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

