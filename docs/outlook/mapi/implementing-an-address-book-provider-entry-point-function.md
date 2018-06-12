---
title: Implementando uma função de ponto de entrada do endereço livro provedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: b60a80bc0ede0c2800f6cfd98a98f498b93a1d8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767416"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="34ac5-103">Implementando uma função de ponto de entrada do endereço livro provedor</span><span class="sxs-lookup"><span data-stu-id="34ac5-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="34ac5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34ac5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34ac5-105">Quando a chamadas do aplicativo de cliente [MAPILogonEx](mapilogonex.md) para iniciar uma sessão usando um perfil que contém seu provedor de catálogo de endereços, MAPI carrega seu provedor e todas as outras pessoas que fazem parte do perfil.</span><span class="sxs-lookup"><span data-stu-id="34ac5-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="34ac5-106">MAPI aprende do nome da função do ponto de entrada do seu provedor observando o perfil.</span><span class="sxs-lookup"><span data-stu-id="34ac5-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="34ac5-107">Lembre-se de que essa função não é o mesmo que uma função de ponto de entrada DLL; Consulte a documentação para **DllMain** na documentação do Win32.</span><span class="sxs-lookup"><span data-stu-id="34ac5-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="34ac5-108">Existem várias entradas, alguns dos quais devem ser exibida no arquivo de configuração Mapisvc, que estão incluídas na seção de perfil de cada provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="34ac5-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="34ac5-109">A tabela a seguir lista essas entradas da seção de perfil e o arquivo Mapisvc ou não deve inclui-los.</span><span class="sxs-lookup"><span data-stu-id="34ac5-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="34ac5-110">**Entrada de seção de perfil**</span><span class="sxs-lookup"><span data-stu-id="34ac5-110">**Profile section entry**</span></span>|<span data-ttu-id="34ac5-111">**requisito de Mapisvc**</span><span class="sxs-lookup"><span data-stu-id="34ac5-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34ac5-112">PR_DISPLAY_NAME = _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="34ac5-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="34ac5-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="34ac5-113">Optional</span></span>  <br/> |
|<span data-ttu-id="34ac5-114">PR_PROVIDER_DISPLAY = _string_</span><span class="sxs-lookup"><span data-stu-id="34ac5-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="34ac5-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="34ac5-115">Required</span></span>  <br/> |
|<span data-ttu-id="34ac5-116">PR_PROVIDER_DLL_NAME = o _nome do arquivo DLL_</span><span class="sxs-lookup"><span data-stu-id="34ac5-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="34ac5-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="34ac5-117">Required</span></span>  <br/> |
|<span data-ttu-id="34ac5-118">PR_RESOURCE_TYPE = _longo_</span><span class="sxs-lookup"><span data-stu-id="34ac5-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="34ac5-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="34ac5-119">Required</span></span>  <br/> |
|<span data-ttu-id="34ac5-120">PR_RESOURCE_FLAGS = _bitmask_</span><span class="sxs-lookup"><span data-stu-id="34ac5-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="34ac5-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="34ac5-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="34ac5-122">Seu provedor de catálogo de endereços pode fazer essas informações em um perfil diretamente chamando o método de [IMAPIProp::SetProps](imapiprop-setprops.md) da seção do seu perfil ou indiretamente modificando Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="34ac5-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="34ac5-123">Perfis são criados usando as informações relevantes na MAPISVC. INF para os provedores de serviço selecionado ou os serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="34ac5-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="34ac5-124">Para obter mais informações sobre a organização e o conteúdo de MAPISVC. INF, consulte o [Formato de arquivo do Mapisvc](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="34ac5-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="34ac5-125">O nome da função de ponto de entrada DLL do seu provedor catálogo de endereços deve ser [ABProviderInit](abproviderinit.md) e ele deve se adequar ao protótipo **ABProviderInit** .</span><span class="sxs-lookup"><span data-stu-id="34ac5-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="34ac5-126">Execute as seguintes tarefas na função de ponto de entrada DLL do seu provedor:</span><span class="sxs-lookup"><span data-stu-id="34ac5-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="34ac5-127">Verifica a versão da interface do provedor de serviço (SPI) para certificar-se de que MAPI está usando uma versão compatível com a versão que está usando o seu provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="34ac5-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="34ac5-128">Criar uma instância de um objeto de provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="34ac5-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="34ac5-129">Não chame **MAPIInitialize** ou **MAPIUninitialize** nessa função.</span><span class="sxs-lookup"><span data-stu-id="34ac5-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="34ac5-130">A função do ponto de entrada DLL instancia um objeto de provedor e retorna ao MAPI um ponteiro para aquele objeto.</span><span class="sxs-lookup"><span data-stu-id="34ac5-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

