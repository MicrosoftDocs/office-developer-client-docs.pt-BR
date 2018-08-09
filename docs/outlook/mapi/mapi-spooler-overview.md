---
title: Visão geral de spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5e4bd4f6038db3dbb33ec3511d953448fea7a6c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767960"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="5fa85-103">Visão geral de spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="5fa85-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="5fa85-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5fa85-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5fa85-105">Spooler MAPI é uma função do processo do Microsoft Office Outlook que é responsável por mensagens de recebimento e envio de mensagens para a partir de um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5fa85-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="5fa85-106">Spooler MAPI tem uma função vital no recebimento da mensagem e entrega.</span><span class="sxs-lookup"><span data-stu-id="5fa85-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="5fa85-107">Quando um sistema de mensagens não estiver disponível, MAPI spooler armazena as mensagens e os encaminha automaticamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="5fa85-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="5fa85-108">Essa capacidade de retenção logon em ou enviar dados quando necessário conhecida como armazenar e encaminhar, um recurso fundamental em ambientes onde conexões remotas são comuns e tráfego de rede é alto.</span><span class="sxs-lookup"><span data-stu-id="5fa85-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="5fa85-109">Spooler MAPI é executado como um segmento de plano de fundo dentro do Outlook.</span><span class="sxs-lookup"><span data-stu-id="5fa85-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="5fa85-110">Spooler MAPI tem responsabilidades adicionais relacionadas à distribuição de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5fa85-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="5fa85-111">Essas tarefas adicionais incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5fa85-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="5fa85-112">Manter o controle dos tipos de destinatário são manipulados pelos provedores de transporte específica.</span><span class="sxs-lookup"><span data-stu-id="5fa85-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="5fa85-113">Informando um aplicativo cliente quando uma nova mensagem foi entregue.</span><span class="sxs-lookup"><span data-stu-id="5fa85-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="5fa85-114">Mensagem de invocação pré-processamento e o pós-processamento.</span><span class="sxs-lookup"><span data-stu-id="5fa85-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="5fa85-115">Geração de relatórios que indicam a entrega da mensagem ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5fa85-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="5fa85-116">Mantendo status nos destinatários processados.</span><span class="sxs-lookup"><span data-stu-id="5fa85-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="5fa85-117">A ilustração a seguir mostra nitidamente como uma mensagem flui de um cliente para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5fa85-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="5fa85-118">**Outgoing message flow**</span><span class="sxs-lookup"><span data-stu-id="5fa85-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="5fa85-119">![Fluxo de mensagens de saída] (media/amapi_46.gif "Fluxo de mensagens de saída")</span><span class="sxs-lookup"><span data-stu-id="5fa85-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="5fa85-120">O usuário de um aplicativo cliente envia uma mensagem para um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="5fa85-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="5fa85-121">A mensagem armazenar provedor inicia o processo de envio, formatação da mensagem com informações adicionais necessárias para transmissão.</span><span class="sxs-lookup"><span data-stu-id="5fa85-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="5fa85-122">Spooler MAPI recebe a mensagem para processar se qualquer uma das seguintes condições ocorrerem:</span><span class="sxs-lookup"><span data-stu-id="5fa85-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="5fa85-123">O provedor de armazenamento de mensagem não está firmemente combinado com um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5fa85-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="5fa85-124">A mensagem requer pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="5fa85-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="5fa85-125">O armazenamento de mensagens e o transporte provedor estão intimamente ligado, mas eles não podem lidar com todos os destinatários para quem a mensagem é endereçada.</span><span class="sxs-lookup"><span data-stu-id="5fa85-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="5fa85-126">Se o spooler MAPI recebe a mensagem, ela realiza qualquer pré-processamento necessário e entrega a mensagem para o provedor de transporte adequado.</span><span class="sxs-lookup"><span data-stu-id="5fa85-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="5fa85-127">O provedor de transporte concede a mensagem para seu sistema de mensagens, que envia para o receptor pretendido.</span><span class="sxs-lookup"><span data-stu-id="5fa85-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="5fa85-128">Com as mensagens de entrada, o fluxo é invertido.</span><span class="sxs-lookup"><span data-stu-id="5fa85-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="5fa85-129">O provedor de transporte recebe uma mensagem de seu sistema de mensagens e notifica o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="5fa85-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="5fa85-130">Spooler realiza qualquer pós-processamento necessário e informa o provedor de armazenamento de mensagem que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="5fa85-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="5fa85-131">Essa notificação faz com que o cliente atualizar sua exibição da mensagem, permitindo ao usuário ler a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="5fa85-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5fa85-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fa85-132">See also</span></span>

- [<span data-ttu-id="5fa85-133">Arquitetura e os recursos MAPI</span><span class="sxs-lookup"><span data-stu-id="5fa85-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

