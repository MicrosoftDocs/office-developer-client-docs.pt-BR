---
title: Implementar uma função de ponto de entrada do provedor de serviços
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
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="2f699-103">Implementar uma função de ponto de entrada do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="2f699-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="2f699-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f699-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f699-105">Cada DLL do provedor de serviços tem uma função de ponto de entrada que o MAPI chama para carregá-lo.</span><span class="sxs-lookup"><span data-stu-id="2f699-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="2f699-106">Lembre-se de que essa função de ponto de entrada não é igual a [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), a função de ponto de entrada da dll Win32.</span><span class="sxs-lookup"><span data-stu-id="2f699-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="2f699-107">Dependendo do tipo de seu provedor, sua função de ponto de entrada do provedor está de acordo com um protótipo diferente.</span><span class="sxs-lookup"><span data-stu-id="2f699-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="2f699-108">MAPI define diferentes protótipos de função de ponto de entrada para provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="2f699-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="2f699-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="2f699-109">**Provider**</span></span>|<span data-ttu-id="2f699-110">**Protótipo de função de ponto de entrada**</span><span class="sxs-lookup"><span data-stu-id="2f699-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f699-111">Provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="2f699-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="2f699-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="2f699-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="2f699-113">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="2f699-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="2f699-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="2f699-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="2f699-115">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="2f699-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="2f699-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="2f699-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="2f699-117">Grande parte da funcionalidade nesses protótipos é o mesmo para todos os tipos de provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="2f699-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="2f699-118">Catálogo de endereços, repositório de mensagens e provedores de transporte execute as duas tarefas principais em suas funções de ponto de entrada:</span><span class="sxs-lookup"><span data-stu-id="2f699-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="2f699-119">Verifique a versão da interface do provedor de serviços (SPI) para certificar-se de que o MAPI está usando uma versão compatível com a versão que seu provedor de serviços está usando.</span><span class="sxs-lookup"><span data-stu-id="2f699-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="2f699-120">Use o parâmetro _lpulMAPIVer_ , que contém a versão da SPI MAPI, e o parâmetro _lpulProviderVer_ , que contém sua versão SPI, para executar a verificação.</span><span class="sxs-lookup"><span data-stu-id="2f699-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="2f699-121">Esses parâmetros são inteiros não assinados de 32 bits compostos de três partes:</span><span class="sxs-lookup"><span data-stu-id="2f699-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="2f699-122">Os bits de 24 a 31 representam a versão principal.</span><span class="sxs-lookup"><span data-stu-id="2f699-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="2f699-123">Os bits 16 a 23 representam a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="2f699-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="2f699-124">Os bits 0 a 15 representam o identificador de atualização.</span><span class="sxs-lookup"><span data-stu-id="2f699-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="2f699-125">Embora o número de versão principal raramente seja alterado, o número da versão secundária é alterado sempre que MAPI é liberado e o SPI foi alterado.</span><span class="sxs-lookup"><span data-stu-id="2f699-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="2f699-126">O identificador de atualização é a versão de compilação interna da Microsoft; é usado para controlar as alterações durante o processo de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="2f699-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="2f699-127">MAPI define a constante CURRENT_SPI_VERSION, documentada no arquivo de cabeçalho Mapispi. h, para indicar a versão da SPI atual.</span><span class="sxs-lookup"><span data-stu-id="2f699-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="2f699-128">Falha ao verificar com o erro MAPI_E_VERSION se você estiver usando uma versão do SPI mais recente do que a versão que o MAPI está usando.</span><span class="sxs-lookup"><span data-stu-id="2f699-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="2f699-129">Criar uma instância de um objeto Provider.</span><span class="sxs-lookup"><span data-stu-id="2f699-129">Create an instance of a provider object.</span></span> <span data-ttu-id="2f699-130">Como o provedor pode ser iniciado e inicializado várias vezes, você deve criar uma nova instância sempre que isso ocorrer.</span><span class="sxs-lookup"><span data-stu-id="2f699-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="2f699-131">Os provedores são iniciados várias vezes quando aparecem em vários perfis que estão sendo usados simultaneamente por um ou mais clientes ou quando aparecem várias vezes em um único perfil.</span><span class="sxs-lookup"><span data-stu-id="2f699-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="2f699-132">Assim como o protótipo de função de ponto de entrada difere dependendo do tipo de seu provedor, o tipo de objeto Provider.</span><span class="sxs-lookup"><span data-stu-id="2f699-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="2f699-133">Se você estiver escrevendo um provedor de catálogo de endereços, implemente [IABProvider: IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="2f699-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="2f699-134">Se você estiver criando um provedor de armazenamento de mensagens, implemente [IMSProvider: IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="2f699-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="2f699-135">Para obter mais informações, consulte [carregando provedores de repositório de mensagens](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="2f699-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="2f699-136">Se você estiver escrevendo um provedor de transporte, implemente [IXPProvider: IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="2f699-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="2f699-137">Para obter mais informações, consulte [inicializar o provedor de transporte](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2f699-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f699-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f699-138">See also</span></span>



[<span data-ttu-id="2f699-139">Iniciar um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="2f699-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

