---
title: Carregando uma mensagem em um formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412412"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="b7905-103">Carregando uma mensagem em um formulário</span><span class="sxs-lookup"><span data-stu-id="b7905-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="b7905-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7905-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7905-105">Para carregar uma mensagem existente em um formulário usando um servidor de formulário, use uma das estratégias a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7905-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="b7905-106">Chame [IMAPISession::P repareForm](imapisession-prepareform.md) para criar um token e, em [seguida, IMAPISession::ShowForm](imapisession-showform.md) para exibir o formulário.</span><span class="sxs-lookup"><span data-stu-id="b7905-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="b7905-107">Chame [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span><span class="sxs-lookup"><span data-stu-id="b7905-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="b7905-108">Usar a **estratégia PrepareForm** e **ShowForm** é relativamente fácil, mas resulta em formulários que são modais em relação ao seu cliente.</span><span class="sxs-lookup"><span data-stu-id="b7905-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="b7905-109">Isso acontece porque a chamada para **ShowForm** não retorna até que o formulário saia.</span><span class="sxs-lookup"><span data-stu-id="b7905-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="b7905-110">Se você precisar lidar com formulários de forma assíncrona, não use essa estratégia.</span><span class="sxs-lookup"><span data-stu-id="b7905-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="b7905-111">Usar a **estratégia LoadForm** é mais difícil porque o método requer vários parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b7905-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="b7905-112">Esses parâmetros instruem o gerenciador de formulário a iniciar o servidor de formulário adequado no contexto apropriado e exibir a mensagem adequada.</span><span class="sxs-lookup"><span data-stu-id="b7905-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="b7905-113">Se o servidor de formulário já estiver em execução, o gerenciador de formulário carregará a mensagem no servidor de formulário sem iniciar uma nova instância do servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="b7905-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="b7905-114">Para especificar qual servidor de formulário iniciar, passe a classe de mensagem manipulada pelo servidor de destino no conteúdo do _parâmetro lpszMessageClass._</span><span class="sxs-lookup"><span data-stu-id="b7905-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="b7905-115">A classe de mensagem apropriada pode ser determinada recuperando a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="b7905-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="b7905-116">Às vezes, não há nenhum servidor de formulário para a classe de mensagem especificada, somente um servidor de formulário que lida com mensagens pertencentes à superclasse da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b7905-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="b7905-117">Se você preferir que a mensagem seja carregada somente por um servidor de formulário especificamente destinado a manipular mensagens dessa classe, de definida a MAPIFORM_EXACTMATCH sinalizador na chamada **LoadForm.**</span><span class="sxs-lookup"><span data-stu-id="b7905-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="b7905-118">Para obter mais informações, consulte [CLASSES de mensagens MAPI.](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="b7905-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="b7905-119">**LoadForm** também requer um ponteiro para o site de mensagens do visualizador e o contexto de exibição e o valor das propriedades **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) e **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="b7905-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

