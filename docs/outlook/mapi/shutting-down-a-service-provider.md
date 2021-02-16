---
title: Desligar um provedor de serviços
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339204"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="20e88-103">Desligar um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="20e88-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="20e88-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20e88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20e88-105">Quando um cliente chama o método [IMAPISession::Logoff](imapisession-logoff.md) para encerrar a sessão e desligar todos os provedores de serviços ativos, o MAPI, por sua vez, chama os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="20e88-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="20e88-106">[IABLogon::Logoff para](iablogon-logoff.md) provedores de agendamento de endereços.</span><span class="sxs-lookup"><span data-stu-id="20e88-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="20e88-107">[IMSLogon::Logoff para](imslogon-logoff.md) provedores de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="20e88-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="20e88-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) para provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="20e88-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="20e88-109">Esses métodos têm implementações semelhantes.</span><span class="sxs-lookup"><span data-stu-id="20e88-109">These methods have similar implementations.</span></span> <span data-ttu-id="20e88-110">As principais tarefas que um método logoff executa são as seguinte:</span><span class="sxs-lookup"><span data-stu-id="20e88-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="20e88-111">Liberação de todos os objetos abertos, incluindo subobjetos e objetos de status.</span><span class="sxs-lookup"><span data-stu-id="20e88-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="20e88-112">Chamar o método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do objeto de suporte para rebaixar sua contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="20e88-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="20e88-113">Removendo todas as estruturas [MAPIUID](mapiuid.md) registradas do provedor.</span><span class="sxs-lookup"><span data-stu-id="20e88-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="20e88-114">Removendo a linha do provedor na tabela de status.</span><span class="sxs-lookup"><span data-stu-id="20e88-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="20e88-115">Executar tarefas relacionadas à limpeza de recursos, como as seguintes:</span><span class="sxs-lookup"><span data-stu-id="20e88-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="20e88-116">Terminando uma conexão com um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="20e88-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="20e88-117">Diminuindo a contagem de referência no objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="20e88-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="20e88-118">Removendo o objeto de logon da lista de objetos de logon que seu provedor armazena.</span><span class="sxs-lookup"><span data-stu-id="20e88-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="20e88-119">No modo de depuração, emita rastreamentos para localizar objetos que tenham vazado memória.</span><span class="sxs-lookup"><span data-stu-id="20e88-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="20e88-120">Quando o método logoff retorna, o MAPI chama o seguinte:</span><span class="sxs-lookup"><span data-stu-id="20e88-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="20e88-121">Método **IUnknown::Release** do objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="20e88-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="20e88-122">O método Shutdown do objeto **do** provedor para executar qualquer tarefa de limpeza final.</span><span class="sxs-lookup"><span data-stu-id="20e88-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="20e88-123">Dependendo do tipo de provedor, um dos seguintes métodos é chamado:</span><span class="sxs-lookup"><span data-stu-id="20e88-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="20e88-124">[IABProvider::Shutdown](iabprovider-shutdown.md) para provedores de agendas</span><span class="sxs-lookup"><span data-stu-id="20e88-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="20e88-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) para provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="20e88-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="20e88-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="20e88-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="20e88-127">Método **IUnknown::Release do seu** objeto provedor.</span><span class="sxs-lookup"><span data-stu-id="20e88-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="20e88-128">Se o provedor for um repositório de mensagens, uma chamada de cliente para [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) também iniciará o processo de desligamento.</span><span class="sxs-lookup"><span data-stu-id="20e88-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="20e88-129">**StoreLogoff** desliga um provedor de armazenamento de mensagens específico e não tem efeito na sessão.</span><span class="sxs-lookup"><span data-stu-id="20e88-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="20e88-130">Somente um provedor de armazenamento de mensagens pode ser desligado com esse método; não há uma maneira explícita de desligar um determinado address book ou provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="20e88-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="20e88-131">Para obter informações sobre como responder a uma **chamada StoreLogoff,** consulte [Desligar um Provedor de Armazenamento de Mensagens.](shutting-down-a-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="20e88-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="20e88-132">A DLL do seu provedor será descarregada quando MAPI chamar a função de API **Win32 FreeLibrary**, uma chamada que é feita após o último cliente ativo ter chamado [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="20e88-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="20e88-133">Neste momento, seu provedor de serviços terá terminado de desligar.</span><span class="sxs-lookup"><span data-stu-id="20e88-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20e88-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="20e88-134">See also</span></span>



[<span data-ttu-id="20e88-135">Provedores de Serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="20e88-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

