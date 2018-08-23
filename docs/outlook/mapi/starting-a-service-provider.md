---
title: Iniciar um provedor de serviços
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: d14a9961002d63733423af474e147ec5001051fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586330"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="ccf9f-103">Iniciar um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="ccf9f-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="ccf9f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccf9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccf9f-105">Em algum momento depois que um cliente inicia uma sessão com MAPI, seu provedor de serviços será iniciado.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="ccf9f-106">Provedores de transporte são iniciados quando um cliente faz uma solicitação para seus serviços.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="ccf9f-107">Provedores de armazenamento de mensagens e catálogo de endereço são iniciados durante o processo de logon do cliente.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="ccf9f-108">Um cliente chama [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para carregar a cada um dos provedores de catálogo de endereços incluídos no perfil e [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) para carregar um provedor de armazenamento de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="ccf9f-109">Os provedores que fazem parte de um serviço de mensagem foram iniciados antes de qualquer um dos outros provedores no serviço de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="ccf9f-110">MAPI inicia cada provedor de serviços no perfil ativo, fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ccf9f-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="ccf9f-111">Localizando o nome do seu DLL no perfil.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="ccf9f-112">É necessário para registrar o nome do seu provedor de DLL no arquivo de configuração para garantir que ele aparece no perfil Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="ccf9f-113">Quando seu provedor de serviço é adicionado a um perfil, individualmente ou como parte de um serviço de mensagem, todas as seções **[Provedor de serviço]** do Mapisvc que se aplicam ao seu provedor são copiadas para o perfil.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="ccf9f-114">Para obter mais informações sobre a estrutura de Mapisvc, consulte o [Formato de arquivo do Mapisvc](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="ccf9f-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="ccf9f-115">Chamar a função de API do Windows **LoadLibrary** , carregar a DLL.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="ccf9f-116">Porque as chamadas de MAPI **LoadLibrary** alguma toda vez que ele usa um provedor de serviço DLL (independente se já tiver sido carregada) ou somente na primeira vez, seu provedor de serviços não deve fazer suposições sobre o número de vezes que será carregado.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="ccf9f-117">Para cada chamada a **LoadLibrary**, MAPI faz uma chamada para a função de API do Windows **FreeLibrary** quando um provedor de serviços que dll não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="ccf9f-118">Chamar a função de ponto de entrada para o provedor.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="ccf9f-119">MAPI chama a função de ponto de entrada do seu provedor para iniciar o processo de logon.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="ccf9f-120">Funções de ponto de entrada Certifique-se de que você está usando uma versão da interface do provedor de serviço (SPI) que seja compatível com a versão que está sendo usada pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="ccf9f-121">Essas funções retornam também ponteiros para objetos do provedor recém-criado.</span><span class="sxs-lookup"><span data-stu-id="ccf9f-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="ccf9f-122">Para obter mais informações sobre como criar uma entrada ponto função para seu provedor, consulte [Implementando uma função de ponto de entrada do serviço provedor](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="ccf9f-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ccf9f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccf9f-123">See also</span></span>



[<span data-ttu-id="ccf9f-124">Provedores de serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="ccf9f-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

