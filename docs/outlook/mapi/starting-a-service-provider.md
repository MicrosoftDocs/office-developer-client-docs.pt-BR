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
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341710"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="5a82c-103">Iniciar um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="5a82c-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="5a82c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a82c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a82c-105">Em algum momento após um cliente iniciar uma sessão com MAPI, seu provedor de serviços será iniciado.</span><span class="sxs-lookup"><span data-stu-id="5a82c-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="5a82c-106">Os provedores de transporte são iniciados quando um cliente faz uma solicitação para seus serviços.</span><span class="sxs-lookup"><span data-stu-id="5a82c-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="5a82c-107">Os provedores de catálogo de endereços e de repositório de mensagens são iniciados durante o processo de logon do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a82c-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="5a82c-108">Um cliente chama [IMAPISession:: OpenAddressBook](imapisession-openaddressbook.md) para carregar cada um dos provedores de catálogo de endereços incluídos no perfil e [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) para carregar um provedor de repositório de mensagens específico.</span><span class="sxs-lookup"><span data-stu-id="5a82c-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="5a82c-109">Os provedores de catálogo de endereços que fazem parte de um serviço de mensagens são iniciados antes de qualquer um dos outros provedores no serviço.</span><span class="sxs-lookup"><span data-stu-id="5a82c-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="5a82c-110">MAPI inicia cada provedor de serviços no perfil ativo fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5a82c-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="5a82c-111">Localizar o nome de sua DLL no perfil.</span><span class="sxs-lookup"><span data-stu-id="5a82c-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="5a82c-112">Você precisa registrar o nome da sua DLL de provedor no arquivo de configuração MAPISVC. inf para garantir que ele apareça no perfil.</span><span class="sxs-lookup"><span data-stu-id="5a82c-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="5a82c-113">Quando o provedor de serviços é adicionado a um perfil, individualmente ou como parte de um serviço de mensagens, todas as seções do **[provedor de serviços]** de MAPISVC. inf que se aplicam ao seu provedor são copiadas para o perfil.</span><span class="sxs-lookup"><span data-stu-id="5a82c-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="5a82c-114">Para obter mais informações sobre a estrutura de MAPISVC. inf, consulte [formato de arquivo de MAPISVC. inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="5a82c-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="5a82c-115">Chamar a função da API do Windows **LoadLibrary** para carregar a dll.</span><span class="sxs-lookup"><span data-stu-id="5a82c-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="5a82c-116">Como o MAPI chama a **LoadLibrary** sempre que usa uma DLL de provedor de serviços (independentemente de ter sido carregado) ou somente na primeira vez, seu provedor de serviços não deve fazer suposições sobre o número de vezes que ele será carregado.</span><span class="sxs-lookup"><span data-stu-id="5a82c-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="5a82c-117">Para cada chamada para **LoadLibrary**, o MAPI faz uma chamada para a função da API do Windows **FREELIBRARY** quando uma DLL do provedor de serviços não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="5a82c-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="5a82c-118">Chamar a função de ponto de entrada para o provedor.</span><span class="sxs-lookup"><span data-stu-id="5a82c-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="5a82c-119">MAPI chama a função de ponto de entrada do provedor para iniciar o processo de logon.</span><span class="sxs-lookup"><span data-stu-id="5a82c-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="5a82c-120">As funções de ponto de entrada garantem que você esteja usando uma versão da SPI (interface de provedor de serviços) compatível com a versão que está sendo usada pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="5a82c-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="5a82c-121">Essas funções também retornam ponteiros para objetos de provedor recém-criados.</span><span class="sxs-lookup"><span data-stu-id="5a82c-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="5a82c-122">Para obter mais informações sobre a criação de uma função de ponto de entrada para o seu provedor, consulte [implementando uma função de ponto de entrada do provedor de serviços](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="5a82c-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a82c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a82c-123">See also</span></span>



[<span data-ttu-id="5a82c-124">Provedores de serviço MAPI</span><span class="sxs-lookup"><span data-stu-id="5a82c-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

