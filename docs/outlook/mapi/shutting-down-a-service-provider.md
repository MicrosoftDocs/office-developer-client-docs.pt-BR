---
title: Desligar a um provedor de serviços
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 71706fc970170f74aa5555da29d904c08c0422f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770411"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="1fc7b-103">Desligar a um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="1fc7b-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="1fc7b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1fc7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1fc7b-105">Quando um cliente chama o método [IMAPISession::Logoff](imapisession-logoff.md) terminar a sessão e desligue todos os provedores de serviço ativo, MAPI por sua vez chama os métodos a seguir:</span><span class="sxs-lookup"><span data-stu-id="1fc7b-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="1fc7b-106">[IABLogon::Logoff](iablogon-logoff.md) para provedores de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="1fc7b-107">[IMSLogon::Logoff](imslogon-logoff.md) para provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="1fc7b-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) para provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="1fc7b-109">Esses métodos têm implementações semelhantes.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-109">These methods have similar implementations.</span></span> <span data-ttu-id="1fc7b-110">As principais tarefas que está executando um método logoff são:</span><span class="sxs-lookup"><span data-stu-id="1fc7b-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="1fc7b-111">Liberar todos os objetos abertos, incluindo subobjetos e objetos de status.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="1fc7b-112">Chamando o suporte ao método do objeto [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para diminuir sua contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-112">Calling the support object's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="1fc7b-113">Removendo todas as estruturas [MAPIUID](mapiuid.md) registradas do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="1fc7b-114">Removendo a linha do seu provedor na tabela de status.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="1fc7b-115">Execução de tarefas relacionadas ao limpando recursos, como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1fc7b-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="1fc7b-116">Encerrando uma conexão com um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="1fc7b-117">A referência de diminuição contar com o objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="1fc7b-118">Removendo o objeto de logon da lista de objetos de logon que armazena seu provedor.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="1fc7b-119">No modo de depuração, emitindo rastreamentos para localizar os objetos que têm vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="1fc7b-120">Quando seu método logoff retorna, MAPI chama o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1fc7b-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="1fc7b-121">Método de **IUnknown:: Release** do objeto seu logon.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="1fc7b-122">Método de **desligamento** do objeto do provedor para executar quaisquer tarefas de limpeza final.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="1fc7b-123">Dependendo do tipo do seu provedor, é chamado um dos métodos a seguir:</span><span class="sxs-lookup"><span data-stu-id="1fc7b-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="1fc7b-124">[IABProvider::Shutdown](iabprovider-shutdown.md) para provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="1fc7b-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="1fc7b-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) para provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="1fc7b-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="1fc7b-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="1fc7b-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="1fc7b-127">Método de **IUnknown:: Release** do objeto do provedor.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="1fc7b-128">Se seu provedor for um armazenamento de mensagens, uma chamada de cliente para [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) também iniciará o processo de desligamento.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="1fc7b-129">**StoreLogoff** desliga o provedor de armazenamento de uma determinada mensagem e não tem efeito sobre a sessão.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="1fc7b-130">Apenas um provedor de armazenamento de mensagens pode ser desligado com este método; Não há explícito para serem desligados um provedor de transporte ou catálogo determinado endereço.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="1fc7b-131">Para obter informações sobre como responder a um **StoreLogoff** chamada, consulte [Sendo para baixo uma mensagem de provedor de armazenamento](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1fc7b-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="1fc7b-132">DLL do seu provedor será descarregado quando a função de API do Win32 **FreeLibrary**, uma chamada feita após o último cliente ativo tiver chamado [MAPIUninitialize](mapiuninitialize.md)chamadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="1fc7b-133">Neste momento, seu provedor de serviços serão terminar desligado.</span><span class="sxs-lookup"><span data-stu-id="1fc7b-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1fc7b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fc7b-134">See also</span></span>



[<span data-ttu-id="1fc7b-135">Provedores de serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="1fc7b-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

