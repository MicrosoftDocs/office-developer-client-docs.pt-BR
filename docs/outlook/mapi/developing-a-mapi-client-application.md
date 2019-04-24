---
title: Desenvolver um aplicativo cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316685"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="44874-103">Desenvolver um aplicativo cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="44874-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="44874-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44874-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44874-105">Os aplicativos clientes MAPI são escritos com a interface de cliente MAPI orientada a objeto.</span><span class="sxs-lookup"><span data-stu-id="44874-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="44874-106">Os clientes MAPI interagem com um ou mais sistemas de mensagens por meio do subsistema MAPI e provedores de serviço compatíveis com MAPI.</span><span class="sxs-lookup"><span data-stu-id="44874-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="44874-107">Essa interação pode ocorrer de várias maneiras diferentes; Há uma enorme variedade de aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="44874-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="44874-108">A maioria dos clientes são clientes de mensagens, integrando o sistema de mensagens ao conjunto de recursos estabelecidos ou realizando mensagens como seu recurso principal.</span><span class="sxs-lookup"><span data-stu-id="44874-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="44874-109">Outros recursos que os clientes MAPI podem fornecer incluem administração de perfil ou catálogo de endereços e gerenciamento de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="44874-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="44874-110">Todos os clientes de mensagens inicializam as bibliotecas MAPI e iniciam uma **sessão** com o subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="44874-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="44874-111">Para obter mais informações, consulte acEssando [objetos usando a sessão](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="44874-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="44874-112">Depois que uma sessão for estabelecida, um cliente poderá:</span><span class="sxs-lookup"><span data-stu-id="44874-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="44874-113">Gerenciar mensagens de saída, incluindo respostas, mensagens encaminhadas e retransmissões.</span><span class="sxs-lookup"><span data-stu-id="44874-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="44874-114">Lidar com mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="44874-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="44874-115">Manipule o repositório de mensagens abrindo pastas e mensagens, criando, modificando, copiando e enviando mensagens, controlando conversas e pesquisando uma ou mais pastas.</span><span class="sxs-lookup"><span data-stu-id="44874-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="44874-116">Manipule o catálogo de endereços criando e modificando destinatários, localizando entradas e atravessando a hierarquia de contêineres.</span><span class="sxs-lookup"><span data-stu-id="44874-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="44874-117">Gerenciar um provedor de transporte executando reconfiguração, definindo opções e ordem de transporte e enviando mensagens sob demanda.</span><span class="sxs-lookup"><span data-stu-id="44874-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="44874-118">Lidar com notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="44874-118">Handle event notification.</span></span>
    
- <span data-ttu-id="44874-119">Manipular formulários.</span><span class="sxs-lookup"><span data-stu-id="44874-119">Handle forms.</span></span>
    
- <span data-ttu-id="44874-120">Gerenciar perfis e serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="44874-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="44874-121">Use os tópicos desta seção para ajudá-lo a implementar essas tarefas básicas e os recursos específicos que farão com que seu cliente MAPI seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="44874-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

