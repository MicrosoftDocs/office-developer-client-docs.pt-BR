---
title: Desenvolvendo um aplicativo cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410032"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="58529-103">Desenvolvendo um aplicativo cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="58529-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="58529-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58529-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58529-105">Os aplicativos cliente MAPI são escritos com a interface de cliente MAPI orientada ao objeto.</span><span class="sxs-lookup"><span data-stu-id="58529-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="58529-106">Os clientes MAPI interagem com um ou mais sistemas de mensagens por meio do subsistema MAPI e provedores de serviços compatíveis com MAPI.</span><span class="sxs-lookup"><span data-stu-id="58529-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="58529-107">Essa interação pode ocorrer de várias maneiras diferentes; há uma enorme variedade em aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="58529-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="58529-108">A maioria dos clientes são clientes de mensagens, integrando mensagens ao conjunto de recursos estabelecido ou executando mensagens como seu recurso principal.</span><span class="sxs-lookup"><span data-stu-id="58529-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="58529-109">Outros recursos que os clientes MAPI podem fornecer incluem a administração de perfil ou o livro de endereços e o gerenciamento de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="58529-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="58529-110">Todos os clientes de mensagens inicializam as bibliotecas MAPI e iniciam **uma sessão com** o subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="58529-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="58529-111">Para obter mais informações, [consulte Acessando objetos usando a sessão.](accessing-objects-by-using-the-session.md)</span><span class="sxs-lookup"><span data-stu-id="58529-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="58529-112">Depois que uma sessão é estabelecida, um cliente pode:</span><span class="sxs-lookup"><span data-stu-id="58529-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="58529-113">Lidar com mensagens de saída, incluindo respostas, mensagens encaminhadas e retransmissões.</span><span class="sxs-lookup"><span data-stu-id="58529-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="58529-114">Manipular mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="58529-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="58529-115">Manipular o armazenamento de mensagens abrindo pastas e mensagens, criando, modificando, copiando e enviando mensagens, acompanhando conversas e pesquisando uma ou mais pastas.</span><span class="sxs-lookup"><span data-stu-id="58529-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="58529-116">Manipular o livro de endereços criando e modificando destinatários, localizando entradas e percorrendo a hierarquia do contêiner.</span><span class="sxs-lookup"><span data-stu-id="58529-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="58529-117">Manipular um provedor de transporte executando reconfiguração, definindo opções e ordem de transporte e enviando mensagens sob demanda.</span><span class="sxs-lookup"><span data-stu-id="58529-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="58529-118">Manipular notificação de evento.</span><span class="sxs-lookup"><span data-stu-id="58529-118">Handle event notification.</span></span>
    
- <span data-ttu-id="58529-119">Manipular formulários.</span><span class="sxs-lookup"><span data-stu-id="58529-119">Handle forms.</span></span>
    
- <span data-ttu-id="58529-120">Manipular perfis e serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="58529-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="58529-121">Use os tópicos desta seção para ajudá-lo a implementar essas tarefas básicas e os recursos específicos que tornarão seu cliente MAPI exclusivo.</span><span class="sxs-lookup"><span data-stu-id="58529-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

