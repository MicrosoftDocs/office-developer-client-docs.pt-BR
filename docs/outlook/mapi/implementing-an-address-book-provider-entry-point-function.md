---
title: Implementando uma função de ponto de entrada do provedor de agendamento de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409710"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="962d0-103">Implementando uma função de ponto de entrada do provedor de agendamento de endereços</span><span class="sxs-lookup"><span data-stu-id="962d0-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="962d0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="962d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="962d0-105">Quando um aplicativo cliente chama [MAPILogonEx](mapilogonex.md) para iniciar uma sessão usando um perfil que contém seu provedor de agendamento de endereços, o MAPI carrega seu provedor e todos os outros que fazem parte do perfil.</span><span class="sxs-lookup"><span data-stu-id="962d0-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="962d0-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span><span class="sxs-lookup"><span data-stu-id="962d0-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="962d0-107">Lembre-se de que essa função não é a mesma que uma função de ponto de entrada de DLL; consulte a documentação **de DllMain** na documentação do Win32.</span><span class="sxs-lookup"><span data-stu-id="962d0-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="962d0-108">Há várias entradas, algumas das quais devem aparecer no arquivo de configuração mapisvc.inf, incluídas na seção de perfil de cada provedor de agendas de endereços.</span><span class="sxs-lookup"><span data-stu-id="962d0-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="962d0-109">A tabela a seguir lista essas entradas de seção de perfil e se o arquivo mapisvc.inf deve ou não incluí-las.</span><span class="sxs-lookup"><span data-stu-id="962d0-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="962d0-110">**Entrada de seção de perfil**</span><span class="sxs-lookup"><span data-stu-id="962d0-110">**Profile section entry**</span></span>|<span data-ttu-id="962d0-111">**requisito mapisvc.inf**</span><span class="sxs-lookup"><span data-stu-id="962d0-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="962d0-112">PR_DISPLAY_NAME= cadeia de _caracteres_</span><span class="sxs-lookup"><span data-stu-id="962d0-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="962d0-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="962d0-113">Optional</span></span>  <br/> |
|<span data-ttu-id="962d0-114">PR_PROVIDER_DISPLAY= cadeia de _caracteres_</span><span class="sxs-lookup"><span data-stu-id="962d0-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="962d0-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="962d0-115">Required</span></span>  <br/> |
|<span data-ttu-id="962d0-116">PR_PROVIDER_DLL_NAME= _nome de arquivo DLL_</span><span class="sxs-lookup"><span data-stu-id="962d0-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="962d0-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="962d0-117">Required</span></span>  <br/> |
|<span data-ttu-id="962d0-118">PR_RESOURCE_TYPE= _long_</span><span class="sxs-lookup"><span data-stu-id="962d0-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="962d0-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="962d0-119">Required</span></span>  <br/> |
|<span data-ttu-id="962d0-120">PR_RESOURCE_FLAGS= _bitmask_</span><span class="sxs-lookup"><span data-stu-id="962d0-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="962d0-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="962d0-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="962d0-122">Seu provedor de agendamento de endereços pode colocar essas informações em um perfil diretamente chamando o método [IMAPIProp::SetProps](imapiprop-setprops.md) da seção de perfil ou indiretamente modificando MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="962d0-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="962d0-123">Os perfis são criados usando as informações relevantes no MAPISVC. INF para os provedores de serviços ou serviços de mensagem selecionados.</span><span class="sxs-lookup"><span data-stu-id="962d0-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="962d0-124">Para obter mais informações sobre a organização e o conteúdo do MAPISVC. INF, consulte [Formato de arquivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="962d0-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="962d0-125">O nome da função de ponto de entrada DLL do seu provedor de endereços deve ser [ABProviderInit](abproviderinit.md) e deve estar em conformidade com o protótipo **ABProviderInit.**</span><span class="sxs-lookup"><span data-stu-id="962d0-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="962d0-126">Execute as seguintes tarefas na função de ponto de entrada DLL do provedor:</span><span class="sxs-lookup"><span data-stu-id="962d0-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="962d0-127">Verifique a versão da interface do provedor de serviços (SPI) para verificar se o MAPI está usando uma versão compatível com a versão que seu provedor de agendas está usando.</span><span class="sxs-lookup"><span data-stu-id="962d0-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="962d0-128">In instantiate an address book provider object.</span><span class="sxs-lookup"><span data-stu-id="962d0-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="962d0-129">Não chame **MAPIInitialize** ou **MAPIUninitialize** nesta função.</span><span class="sxs-lookup"><span data-stu-id="962d0-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="962d0-130">A função de ponto de entrada de DLL insta em um objeto de provedor e retorna a MAPI um ponteiro para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="962d0-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

