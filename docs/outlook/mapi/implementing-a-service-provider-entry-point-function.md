---
title: Implementando uma função de ponto de entrada de provedor de serviço
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 632aff9c0f6fc60ee9730b5e43667b5b610ae8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767412"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="62394-103">Implementando uma função de ponto de entrada de provedor de serviço</span><span class="sxs-lookup"><span data-stu-id="62394-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="62394-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62394-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62394-105">Cada DLL do provedor de serviço tem uma entrada aponte a função que chamadas MAPI carregá-la.</span><span class="sxs-lookup"><span data-stu-id="62394-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="62394-106">Lembre-se de que essa função de ponto de entrada não é igual ao [DllMain](http://msdn.microsoft.com/pt-br/library/ms682583.aspx), a função do ponto de entrada DLL Win32.</span><span class="sxs-lookup"><span data-stu-id="62394-106">Be aware that this entry point function is not the same as [DllMain](http://msdn.microsoft.com/pt-br/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="62394-107">Dependendo do tipo do seu provedor, sua função de ponto de entrada do provedor está em conformidade com um protótipo diferente.</span><span class="sxs-lookup"><span data-stu-id="62394-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="62394-108">MAPI define protótipos de função de ponto de entrada diferentes para provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="62394-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="62394-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="62394-109">**Provider**</span></span>|<span data-ttu-id="62394-110">**Protótipo de função de ponto de entrada**</span><span class="sxs-lookup"><span data-stu-id="62394-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62394-111">Provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="62394-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="62394-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="62394-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="62394-113">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="62394-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="62394-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="62394-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="62394-115">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="62394-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="62394-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="62394-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="62394-117">Muitas das funcionalidades nesses protótipos é o mesmo para todos os tipos de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="62394-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="62394-118">Catálogo de endereços, armazenamento de mensagens e provedores de transporte executam duas tarefas principais a seguir em suas funções de ponto de entrada:</span><span class="sxs-lookup"><span data-stu-id="62394-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="62394-119">Verifica a versão da interface do provedor de serviço (SPI) para certificar-se de que o MAPI está usando uma versão compatível com a versão que está usando o seu provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="62394-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="62394-120">Use o parâmetro _lpulMAPIVer_ , que contém a versão de MAPI SPI e o parâmetro _lpulProviderVer_ , que contém sua versão EDA, executar a verificação.</span><span class="sxs-lookup"><span data-stu-id="62394-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="62394-121">Estes parâmetros são números inteiros não assinados de 32 bits compostos de três partes:</span><span class="sxs-lookup"><span data-stu-id="62394-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="62394-122">Bits 24 a 31 representam a versão principal.</span><span class="sxs-lookup"><span data-stu-id="62394-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="62394-123">Bits 16 a 23 representam a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="62394-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="62394-124">Bits 0 a 15 representam o identificador de atualização.</span><span class="sxs-lookup"><span data-stu-id="62394-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="62394-125">Embora raramente altera o número da versão principal, a número da versão secundária alterações sempre que o MAPI é liberada e o SPI foi alterada.</span><span class="sxs-lookup"><span data-stu-id="62394-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="62394-126">O identificador de atualização é a versão; de compilação do Microsoft interno ele é usado para rastrear alterações durante o processo de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="62394-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="62394-127">MAPI define a constante CURRENT_SPI_VERSION, documentados no arquivo de cabeçalho Mapispi.h, para indicar a versão de EDA presente.</span><span class="sxs-lookup"><span data-stu-id="62394-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="62394-128">Falha de sua verificação com o erro MAPI_E_VERSION se você estiver usando uma versão da SPI mais recente que a versão que está usando o MAPI.</span><span class="sxs-lookup"><span data-stu-id="62394-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="62394-129">Crie uma instância de um objeto do provedor.</span><span class="sxs-lookup"><span data-stu-id="62394-129">Create an instance of a provider object.</span></span> <span data-ttu-id="62394-130">Porque seu provedor pode ser iniciado e inicializado várias vezes, você deve criar uma nova instância sempre que isso ocorre.</span><span class="sxs-lookup"><span data-stu-id="62394-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="62394-131">Provedores são iniciados várias vezes quando eles aparecem em vários perfis que estiverem em uso simultaneamente por um ou mais clientes ou quando eles aparecem várias vezes em um único perfil.</span><span class="sxs-lookup"><span data-stu-id="62394-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="62394-132">Assim como o protótipo de função de ponto de entrada será diferente, dependendo do tipo de seu provedor, portanto não o tipo de objeto do provedor.</span><span class="sxs-lookup"><span data-stu-id="62394-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="62394-133">Se você estiver escrevendo um provedor de catálogo de endereços, implemente [IABProvider: IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="62394-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="62394-134">Se você estiver escrevendo um provedor de armazenamento de mensagem, implemente [IMSProvider: IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="62394-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="62394-135">Para obter mais informações, consulte [Carregando provedores de armazenamento de mensagem](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="62394-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="62394-136">Se você estiver escrevendo um provedor de transporte, implemente [IXPProvider: IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="62394-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="62394-137">Para obter mais informações, consulte [inicializar o provedor de transporte](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="62394-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62394-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="62394-138">See also</span></span>



[<span data-ttu-id="62394-139">Iniciando um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="62394-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

