---
title: Verificando a configuração de provedor de serviço
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f6190b2860e227b24b34e31a4ee9741468383460
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589634"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="cb3cc-103">Verificando a configuração de provedor de serviço</span><span class="sxs-lookup"><span data-stu-id="cb3cc-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="cb3cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb3cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb3cc-105">Seu método de logon ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) Verifique a configuração do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="cb3cc-106">Isso envolve a verificação de que todas as propriedades necessárias para a operação completa estão definidas corretamente.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="cb3cc-107">Cada provedor requer um número diferente de propriedades; configuração depende do seu provedor e o grau de você permitir a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="cb3cc-108">Alguns provedores de serviços mantenha todas as propriedades necessárias no perfil.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="cb3cc-109">Outros provedores de serviços mantenha um conjunto parcial das propriedades no perfil e solicitar ao usuário de valores ausentes.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="cb3cc-110">Ainda outros provedores não armazene propriedades no perfil nisso, depender fornecer todas as informações necessárias para configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="cb3cc-111">Para recuperar as propriedades armazenadas no perfil</span><span class="sxs-lookup"><span data-stu-id="cb3cc-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="cb3cc-112">Chame [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passando o [MAPIUID](mapiuid.md) do provedor de como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="cb3cc-113">Chame métodos de [IMAPIProp::GetProps](imapiprop-getprops.md) ou [IMAPIProp::GetPropList](imapiprop-getproplist.md) da seção perfil para recuperar as propriedades individuais ou uma lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="cb3cc-114">Para definir as propriedades das informações do usuário</span><span class="sxs-lookup"><span data-stu-id="cb3cc-114">To set properties from user information</span></span>
  
<span data-ttu-id="cb3cc-115">Exiba uma folha de propriedades, se MAPI não tiver definido um sinalizador proibindo a exibição.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="cb3cc-116">Sinalizadores a seguir indicam que uma interface de usuário não pode ser apresentada.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="cb3cc-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="cb3cc-117">**Flag**</span></span>|<span data-ttu-id="cb3cc-118">**Provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="cb3cc-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb3cc-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="cb3cc-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="cb3cc-120">Provedor de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="cb3cc-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="cb3cc-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="cb3cc-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="cb3cc-122">Provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="cb3cc-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="cb3cc-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="cb3cc-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="cb3cc-124">Provedor de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="cb3cc-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="cb3cc-125">Se seu provedor não armazena todas as suas propriedades de configuração do perfil, exigir interação do usuário e MAPI passa uma dos sinalizadores de supressão de caixa de diálogo para seu método de logon, retorne MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="cb3cc-126">Também retorne esse erro quando o sinalizador de supressão de diálogo não estiver definido, mas o usuário não fornecer todas as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="cb3cc-127">Quando seu provedor de serviço falha seu método de logon com MAPI_E_UNCONFIGURED, MAPI chama a função do ponto de entrada novamente.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="cb3cc-128">Se as informações não podem ser localizadas com a segunda chamada, talvez encerrar a sessão, dependendo de qual seu provedor de serviços é a importância.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="cb3cc-129">A ilustração a seguir mostra a lógica obrigatório para a configuração no seu método de logon do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="cb3cc-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="cb3cc-130">**Configuration verification flowchart**</span><span class="sxs-lookup"><span data-stu-id="cb3cc-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="cb3cc-131">![Fluxograma de verificação de configuração] (media/amapi_62.gif "Fluxograma de verificação de configuração")</span><span class="sxs-lookup"><span data-stu-id="cb3cc-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb3cc-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb3cc-132">See also</span></span>

- [<span data-ttu-id="cb3cc-133">Implementar o logon do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="cb3cc-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

