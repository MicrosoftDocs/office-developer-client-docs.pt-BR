---
title: Desenvolver aplicativos cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bffcfdd6d688c483655b97d61075b147430e3fcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564973"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="71868-103">Desenvolver aplicativos cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="71868-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="71868-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71868-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71868-105">Aplicativos de cliente MAPI são gravados com a interface de cliente MAPI orientada a objeto.</span><span class="sxs-lookup"><span data-stu-id="71868-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="71868-106">Clientes MAPI interagem com um ou mais sistemas de mensagens por meio do subsistema MAPI e os provedores de serviço compatível com MAPI.</span><span class="sxs-lookup"><span data-stu-id="71868-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="71868-107">Essa interação pode ocorrer de várias maneiras diferentes; Não há uma enorme variedade em aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="71868-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="71868-108">A maioria dos clientes são mensagens de clientes, a integração de mensagens em seu conjunto de recursos estabelecidas ou realização de mensagens como seu recurso principal.</span><span class="sxs-lookup"><span data-stu-id="71868-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="71868-109">Outros recursos que podem fornecer a clientes MAPI incluem a administração de perfil ou gerenciamento de repositório de mensagem e catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="71868-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="71868-110">Todos os clientes de mensagens inicializar as bibliotecas MAPI e iniciar uma **sessão** com o subsistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="71868-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="71868-111">Para obter mais informações, consulte [Acessando objetos usando a sessão](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="71868-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="71868-112">Depois que uma sessão tiver sido estabelecida, um cliente pode:</span><span class="sxs-lookup"><span data-stu-id="71868-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="71868-113">Trata as mensagens de saída, incluindo respostas, encaminhadas mensagens e retransmissões.</span><span class="sxs-lookup"><span data-stu-id="71868-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="71868-114">Trata as mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="71868-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="71868-115">Lidar com o armazenamento de mensagens por abrindo pastas e mensagens, criando, modificando, copiar e envio de mensagens, conversas de acompanhamento e uma ou mais pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="71868-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="71868-116">Manipule o catálogo de endereços, criação e modificação de destinatários, localizar entradas e atravessando a hierarquia de contêiner.</span><span class="sxs-lookup"><span data-stu-id="71868-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="71868-117">Lidar com um provedor de transporte executando reconfiguração, definindo opções e transporte de ordem, e enviando mensagens sob demanda.</span><span class="sxs-lookup"><span data-stu-id="71868-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="71868-118">Manipule notificações de evento.</span><span class="sxs-lookup"><span data-stu-id="71868-118">Handle event notification.</span></span>
    
- <span data-ttu-id="71868-119">Lidar com formulários.</span><span class="sxs-lookup"><span data-stu-id="71868-119">Handle forms.</span></span>
    
- <span data-ttu-id="71868-120">Lidar com perfis e serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="71868-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="71868-121">Use os tópicos desta seção para ajudá-lo a implementar essas tarefas básicas e os recursos específicos que tornarão seu cliente MAPI exclusivo.</span><span class="sxs-lookup"><span data-stu-id="71868-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

