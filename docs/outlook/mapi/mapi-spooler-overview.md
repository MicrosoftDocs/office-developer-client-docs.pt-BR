---
title: Visão geral do spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432713"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="be428-103">Visão geral do spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="be428-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="be428-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be428-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be428-105">MAPI spooler é uma função do processo do Microsoft Office Outlook responsável por enviar mensagens e receber mensagens de um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="be428-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="be428-106">O spooler MAPI exerce uma função vital no recebimento e na entrega de mensagens.</span><span class="sxs-lookup"><span data-stu-id="be428-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="be428-107">Quando um sistema de mensagens está indisponível, o spooler MAPI armazena as mensagens e as encaminha automaticamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="be428-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="be428-108">Essa capacidade de manter ou enviar dados quando necessário é conhecido como armazenar e encaminhar, um recurso crítico em ambientes onde as conexões remotas são comuns e o tráfego de rede é alto.</span><span class="sxs-lookup"><span data-stu-id="be428-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="be428-109">O spooler MAPI é executado como um thread de segundo plano no Outlook.</span><span class="sxs-lookup"><span data-stu-id="be428-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="be428-110">O spooler MAPI tem responsabilidades adicionais relacionadas à distribuição de mensagens.</span><span class="sxs-lookup"><span data-stu-id="be428-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="be428-111">Essas tarefas adicionais incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="be428-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="be428-112">Manter o controle dos tipos de destinatários que são tratados por provedores de transporte específicos.</span><span class="sxs-lookup"><span data-stu-id="be428-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="be428-113">Informando um aplicativo cliente quando uma nova mensagem é entregue.</span><span class="sxs-lookup"><span data-stu-id="be428-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="be428-114">Invocar o pré-processamento e o processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="be428-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="be428-115">Geração de relatórios que indicam que a entrega de mensagens ocorreu.</span><span class="sxs-lookup"><span data-stu-id="be428-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="be428-116">Manutenção do status em destinatários processados.</span><span class="sxs-lookup"><span data-stu-id="be428-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="be428-117">A ilustração a seguir mostra em nível alto como uma mensagem flui de um cliente para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="be428-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="be428-118">**Outgoing message flow**</span><span class="sxs-lookup"><span data-stu-id="be428-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="be428-119">![Fluxo de mensagens de saída] (media/amapi_46.gif "Fluxo de mensagens de saída")</span><span class="sxs-lookup"><span data-stu-id="be428-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="be428-120">O usuário de um aplicativo cliente envia uma mensagem para um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="be428-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="be428-121">O provedor de repositório de mensagens inicia o processo de envio, Formatando a mensagem com informações adicionais necessárias para a transmissão.</span><span class="sxs-lookup"><span data-stu-id="be428-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="be428-122">MAPI spooler recebe a mensagem a ser processada se ocorrer qualquer uma das seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="be428-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="be428-123">O provedor de repositório de mensagens não está rigidamente acoplado a um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="be428-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="be428-124">A mensagem requer pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="be428-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="be428-125">O repositório de mensagens e o provedor de transporte estão rigidamente acoplados, mas não podem lidar com todos os destinatários para os quais a mensagem é endereçada.</span><span class="sxs-lookup"><span data-stu-id="be428-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="be428-126">Se o spooler MAPI receber a mensagem, ele realiza qualquer pré-processamento necessário e entrega a mensagem para o provedor de transporte apropriado.</span><span class="sxs-lookup"><span data-stu-id="be428-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="be428-127">O provedor de transporte fornece a mensagem ao seu sistema de mensagens, que a envia para o destinatário pretendido.</span><span class="sxs-lookup"><span data-stu-id="be428-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="be428-128">Com mensagens de entrada, o fluxo é revertido.</span><span class="sxs-lookup"><span data-stu-id="be428-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="be428-129">O provedor de transporte recebe uma mensagem de seu sistema de mensagens e notifica o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="be428-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="be428-130">O spooler realiza todos os processamentos e informa o provedor do repositório de mensagens de que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="be428-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="be428-131">Essa notificação faz com que o cliente atualize sua exibição de mensagem, permitindo que o usuário leia a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="be428-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be428-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="be428-132">See also</span></span>

- [<span data-ttu-id="be428-133">Recursos e arquitetura MAPI</span><span class="sxs-lookup"><span data-stu-id="be428-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

