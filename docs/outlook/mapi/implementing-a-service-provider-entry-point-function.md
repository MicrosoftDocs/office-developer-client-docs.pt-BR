---
title: Implementando uma função de ponto de entrada do provedor de serviços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332988"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="0fb2d-103">Implementando uma função de ponto de entrada do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="0fb2d-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="0fb2d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fb2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fb2d-105">Cada DLL do provedor de serviços tem uma função de ponto de entrada que o MAPI chama para carregá-la.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="0fb2d-106">Esteja ciente de que essa função de ponto de entrada não é a mesma que [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), a função de ponto de entrada DLL Win32.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="0fb2d-107">Dependendo do tipo de seu provedor, sua função de ponto de entrada do provedor está em conformidade com um protótipo diferente.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="0fb2d-108">MAPI define diferentes protótipos de função de ponto de entrada para provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="0fb2d-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="0fb2d-109">**Provider**</span></span>|<span data-ttu-id="0fb2d-110">**Protótipo de função de ponto de entrada**</span><span class="sxs-lookup"><span data-stu-id="0fb2d-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0fb2d-111">Provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="0fb2d-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="0fb2d-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="0fb2d-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="0fb2d-113">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="0fb2d-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="0fb2d-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="0fb2d-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="0fb2d-115">Provedores de lista de endereços</span><span class="sxs-lookup"><span data-stu-id="0fb2d-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="0fb2d-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="0fb2d-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="0fb2d-117">Grande parte da funcionalidade nesses protótipos é a mesma para todos os tipos de provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="0fb2d-118">O address book, o armazenamento de mensagens e os provedores de transporte executam as duas tarefas principais a seguir em suas funções de ponto de entrada:</span><span class="sxs-lookup"><span data-stu-id="0fb2d-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="0fb2d-119">Verifique a versão da interface do provedor de serviços (SPI) para ter certeza de que o MAPI está usando uma versão compatível com a versão que seu provedor de serviços está usando.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="0fb2d-120">Use o  _parâmetro lpulMAPIVer,_ que contém a versão SPI MAPI, e o parâmetro  _lpulProviderVer,_ que contém sua versão SPI, para executar a verificação.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="0fb2d-121">Esses parâmetros são inteiros não assinados de 32 bits compostos de três partes:</span><span class="sxs-lookup"><span data-stu-id="0fb2d-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="0fb2d-122">Os bits de 24 a 31 representam a versão principal.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="0fb2d-123">Os bits de 16 a 23 representam a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="0fb2d-124">Os bits de 0 a 15 representam o identificador de atualização.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="0fb2d-125">Embora o número da versão principal raramente seja alterado, o número da versão secundária muda sempre que o MAPI é liberado e o SPI é alterado.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="0fb2d-126">O identificador de atualização é a versão de com build interna da Microsoft; ele é usado para controlar alterações durante o processo de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="0fb2d-127">MAPI define a CURRENT_SPI_VERSION constante, documentada no arquivo de header Mapispi.h, para indicar a versão SPI presente.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="0fb2d-128">Falha na verificação com o erro MAPI_E_VERSION se você estiver usando uma versão do SPI mais recente do que a versão que o MAPI está usando.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="0fb2d-129">Crie uma instância de um objeto de provedor.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-129">Create an instance of a provider object.</span></span> <span data-ttu-id="0fb2d-130">Como seu provedor pode ser iniciado e inicializado várias vezes, você deve criar uma nova instância sempre que isso ocorrer.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="0fb2d-131">Os provedores são iniciados várias vezes quando aparecem em vários perfis em uso simultâneo por um ou mais clientes ou quando aparecem várias vezes em um único perfil.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="0fb2d-132">Assim como o protótipo de função de ponto de entrada difere dependendo do tipo de seu provedor, o tipo de objeto do provedor também difere.</span><span class="sxs-lookup"><span data-stu-id="0fb2d-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="0fb2d-133">Se você estiver escrevendo um provedor de agendas, implemente [IABProvider : IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0fb2d-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="0fb2d-134">Se você estiver escrevendo um provedor de armazenamento de mensagens, [implemente IMSProvider : IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0fb2d-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="0fb2d-135">Para obter mais informações, consulte [Carregando provedores de armazenamento de mensagens.](loading-message-store-providers.md)</span><span class="sxs-lookup"><span data-stu-id="0fb2d-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="0fb2d-136">Se você estiver escrevendo um provedor de transporte, implemente [IXPProvider : IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0fb2d-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="0fb2d-137">Para obter mais informações, consulte [Inicializando o Provedor de Transporte.](initializing-the-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="0fb2d-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fb2d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fb2d-138">See also</span></span>



[<span data-ttu-id="0fb2d-139">Iniciando um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="0fb2d-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

