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
ms.openlocfilehash: ad0da261b3059ca83f2d547c25a508ec9337aa72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584741"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="6e6d2-103">Implementar um visualizador de formulários</span><span class="sxs-lookup"><span data-stu-id="6e6d2-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="6e6d2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e6d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e6d2-105">Um visualizador de formulário inclui três objetos: um site de mensagem, coletor de eventos e um contexto de modo de exibição de aviso de um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="6e6d2-106">Cada um desses objetos permite que você interaja com um servidor de formulário e seus formulários.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="6e6d2-107">Um site de mensagem é um objeto que implementa o [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interface e os servidores de formulário com tarefas como mover, salvar, ou excluindo mensagens, criando novas mensagens ou lançar novos servidores de formulário de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="6e6d2-108">Para obter mais informações sobre o status do seu cliente com relação a vários provedores de serviços, sites de mensagem são usados por formulários.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="6e6d2-109">Por exemplo, um formulário pode usar o seu site de mensagem para obter um ponteiro para o armazenamento de mensagens atual, uma mensagem ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="6e6d2-110">Existem dois tipos de métodos na interface do **IMAPIMessageSite** :</span><span class="sxs-lookup"><span data-stu-id="6e6d2-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="6e6d2-111">Métodos que fornecem informações aos objetos de formulário.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="6e6d2-112">Métodos que manipulam mensagens.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="6e6d2-113">Os métodos que fornecem informações aos objetos de formulário são simples de implementar.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="6e6d2-114">Em todos os casos, exceto [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), você já deve ter disponíveis as informações necessárias para cada método.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="6e6d2-115">Os métodos de manipulam mensagens devem agir como se eles tivessem sido disparados por meio da interface de usuário normal.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="6e6d2-116">Por exemplo, se um objeto form chama seu método [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) , se comportam como se o usuário teve escolhida redigir uma nova mensagem personalizada com uma interface do usuário regular.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="6e6d2-117">Os comandos que geralmente geram esse comportamento são **redação**, **Abrir**, **responder**, **responder a todos os destinatários**e **Encaminhar**.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="6e6d2-118">Um contexto de modo de exibição é um objeto que implementa o [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) interface e fornece os servidores de formulário com um contexto da mensagem atual, permitindo que os servidores alternar facilmente para a mensagem anterior ou seguinte na pasta.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="6e6d2-119">Um formulário usa um contexto de modo de exibição para compartilhamento de informações.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="6e6d2-120">Com um objeto de contexto do modo de exibição, um formulário pode:</span><span class="sxs-lookup"><span data-stu-id="6e6d2-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="6e6d2-121">Registre seu cliente para notificações.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="6e6d2-122">Ative a mensagem anterior ou seguinte na pasta.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="6e6d2-123">Obtenha informações sobre a impressão.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-123">Get printing information.</span></span>
    
- <span data-ttu-id="6e6d2-124">Obter o status do seu cliente.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-124">Get your client's status.</span></span>
    
- <span data-ttu-id="6e6d2-125">Obtenha um fluxo que pode ser usado para salvar a versão de texto de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="6e6d2-126">Semelhante aos métodos no [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interface, os métodos do **IMAPIViewContext** correlacionam com ações do usuário e recursos do cliente que se relacionam com o contexto de modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="6e6d2-127">Por exemplo, um contexto de modo de exibição está envolvido com ativando a mensagem anterior ou seguinte, o conteúdo da pasta de classificação e filtragem de conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="6e6d2-128">Não é importante que você fornecer para usuários de mecanismo para ativar esses recursos, só é importante que a semântica desses recursos mapa bem para os métodos na interface do **IMAPIViewContext** .</span><span class="sxs-lookup"><span data-stu-id="6e6d2-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="6e6d2-129">Um modo de exibição de aviso coletor de eventos é um objeto que implementa o [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) notificações de interface e os identificadores dos servidores de formulário que afetam seus formulários visualizador e ajuda e visualizadores de formulário para que trabalhem juntos.</span><span class="sxs-lookup"><span data-stu-id="6e6d2-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="6e6d2-130">Para obter mais informações, consulte [enviando e recebendo notificações de formulário](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="6e6d2-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

