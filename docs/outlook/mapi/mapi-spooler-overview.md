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
# <a name="mapi-spooler-overview"></a><span data-ttu-id="04480-103">Visão geral do spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="04480-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="04480-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04480-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04480-105">O spooler MAPI é uma função do processo do Microsoft Office Outlook responsável por enviar e receber mensagens de um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="04480-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="04480-106">O spooler MAPI desempenha um papel vital no recebimento e na entrega de mensagens.</span><span class="sxs-lookup"><span data-stu-id="04480-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="04480-107">Quando um sistema de mensagens não está disponível, o spooler MAPI armazena as mensagens e as encaminha automaticamente posteriormente.</span><span class="sxs-lookup"><span data-stu-id="04480-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="04480-108">Essa capacidade de manter ou enviar dados quando necessário é conhecida como armazenamento e encaminhamento, um recurso crítico em ambientes onde as conexões remotas são comuns e o tráfego de rede é alto.</span><span class="sxs-lookup"><span data-stu-id="04480-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="04480-109">O spooler MAPI é executado como um thread em segundo plano no Outlook.</span><span class="sxs-lookup"><span data-stu-id="04480-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="04480-110">O spooler MAPI tem responsabilidades adicionais relacionadas à distribuição de mensagens.</span><span class="sxs-lookup"><span data-stu-id="04480-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="04480-111">Essas tarefas extras incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="04480-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="04480-112">Acompanhar os tipos de destinatários manipulados por provedores de transporte específicos.</span><span class="sxs-lookup"><span data-stu-id="04480-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="04480-113">Informar um aplicativo cliente quando uma nova mensagem for entregue.</span><span class="sxs-lookup"><span data-stu-id="04480-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="04480-114">Invocando o pré-processamento e o pós-processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="04480-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="04480-115">Gerar relatórios que indicam que a entrega da mensagem ocorreu.</span><span class="sxs-lookup"><span data-stu-id="04480-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="04480-116">Mantendo o status de destinatários processados.</span><span class="sxs-lookup"><span data-stu-id="04480-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="04480-117">A ilustração a seguir mostra em um alto nível como uma mensagem flui de um cliente para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="04480-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="04480-118">**Outgoing message flow**</span><span class="sxs-lookup"><span data-stu-id="04480-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="04480-119">![Fluxo de mensagens de saída Fluxo]de mensagens de(media/amapi_46.gif "saída")</span><span class="sxs-lookup"><span data-stu-id="04480-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="04480-120">O usuário de um aplicativo cliente envia uma mensagem para um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="04480-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="04480-121">O provedor de armazenamento de mensagens inicia o processo de envio, formatando a mensagem com informações adicionais necessárias para transmissão.</span><span class="sxs-lookup"><span data-stu-id="04480-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="04480-122">O spooler MAPI recebe a mensagem a ser processada se qualquer uma das seguintes condições ocorrer:</span><span class="sxs-lookup"><span data-stu-id="04480-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="04480-123">O provedor de armazenamento de mensagens não está fortemente unido a um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="04480-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="04480-124">A mensagem requer pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="04480-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="04480-125">O armazenamento de mensagens e o provedor de transporte estão fortemente próximos, mas não podem lidar com todos os destinatários aos quais a mensagem é endereçada.</span><span class="sxs-lookup"><span data-stu-id="04480-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="04480-126">Se o spooler MAPI receber a mensagem, ele executará qualquer pré-processamento necessário e entregará a mensagem ao provedor de transporte apropriado.</span><span class="sxs-lookup"><span data-stu-id="04480-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="04480-127">O provedor de transporte fornece a mensagem ao seu sistema de mensagens, que a envia ao destinatário pretendido.</span><span class="sxs-lookup"><span data-stu-id="04480-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="04480-128">Com as mensagens de entrada, o fluxo é revertido.</span><span class="sxs-lookup"><span data-stu-id="04480-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="04480-129">O provedor de transporte recebe uma mensagem de seu sistema de mensagens e notifica o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="04480-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="04480-130">O Spooler executa qualquer pós-processamento necessário e informa ao provedor do armazenamento de mensagens que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="04480-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="04480-131">Essa notificação faz com que o cliente atualize a exibição da mensagem, permitindo que o usuário leia a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="04480-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04480-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="04480-132">See also</span></span>

- [<span data-ttu-id="04480-133">Recursos e arquitetura MAPI</span><span class="sxs-lookup"><span data-stu-id="04480-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

