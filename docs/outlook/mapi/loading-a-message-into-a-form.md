---
title: Carregar uma mensagem em um formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6e65311187ba96abde31a4779ebba371b3d02084
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576495"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="70a93-103">Carregar uma mensagem em um formulário</span><span class="sxs-lookup"><span data-stu-id="70a93-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="70a93-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70a93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70a93-105">Para carregar uma mensagem existente em um formulário usando um servidor de formulário, use uma das seguintes estratégias.</span><span class="sxs-lookup"><span data-stu-id="70a93-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="70a93-106">[PrepareForm](imapisession-prepareform.md) para criar um token de chamada e, em seguida, [IMAPISession:: ShowForm](imapisession-showform.md) para exibir o formulário.</span><span class="sxs-lookup"><span data-stu-id="70a93-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="70a93-107">Chame [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span><span class="sxs-lookup"><span data-stu-id="70a93-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="70a93-108">Usando a estratégia de **PrepareForm** e **ShowForm** é relativamente fácil, mas ele implica formulários que são modais em relação ao seu cliente.</span><span class="sxs-lookup"><span data-stu-id="70a93-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="70a93-109">Isso ocorre porque a chamada para **ShowForm** não retorna até que o formulário foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="70a93-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="70a93-110">Se você precisar manipular formulários de forma assíncrona, não use essa estratégia.</span><span class="sxs-lookup"><span data-stu-id="70a93-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="70a93-111">Usando a estratégia de **LoadForm** é mais difícil, pois o método requer vários parâmetros.</span><span class="sxs-lookup"><span data-stu-id="70a93-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="70a93-112">Esses parâmetros instruem o Gerenciador de formulário para iniciar o servidor de forma adequada no contexto adequado e exibir a mensagem apropriada.</span><span class="sxs-lookup"><span data-stu-id="70a93-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="70a93-113">Se o servidor de formulário já estiver em execução, o gerente de formulário carrega a mensagem para o servidor de formulário sem lançar uma nova instância do servidor do formulário.</span><span class="sxs-lookup"><span data-stu-id="70a93-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="70a93-114">Para especificar qual servidor formulário início, passe a classe de mensagem manipulada pelo servidor de destino no conteúdo do parâmetro _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="70a93-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="70a93-115">A classe de mensagem apropriada pode ser determinada pela Recuperando a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="70a93-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="70a93-116">Em alguns casos, não há nenhum servidor de formulário para a classe de mensagem especificada, somente um servidor de formulário que trata as mensagens que pertencem a superclasse da mensagem.</span><span class="sxs-lookup"><span data-stu-id="70a93-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="70a93-117">Se você preferir que a mensagem ser carregado somente por um servidor de formulário especificamente desenvolvido para lidar com as mensagens de classe, defina o sinalizador MAPIFORM_EXACTMATCH na chamada **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="70a93-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="70a93-118">Para obter mais informações, consulte [Classes de mensagem MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="70a93-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="70a93-119">**LoadForm** também requer um ponteiro para o site de mensagem do seu visualizador e contexto de modo de exibição e o valor para a mensagem de destino **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) e o **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Propriedades.</span><span class="sxs-lookup"><span data-stu-id="70a93-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

