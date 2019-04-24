---
title: Verificar a configuração do provedor de serviços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329601"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="e7249-103">Verificar a configuração do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="e7249-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="e7249-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7249-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7249-105">Seu método de logon ([IABProvider:: logon](iabprovider-logon.md), [IMSProvider:: logon](imsprovider-logon.md)ou [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md)) deve verificar a configuração do provedor.</span><span class="sxs-lookup"><span data-stu-id="e7249-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="e7249-106">Isso envolve verificar se todas as propriedades necessárias para a operação completa estão definidas corretamente.</span><span class="sxs-lookup"><span data-stu-id="e7249-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="e7249-107">Cada provedor requer um número diferente de propriedades; a configuração depende do provedor e do grau de interação do usuário que você permite.</span><span class="sxs-lookup"><span data-stu-id="e7249-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="e7249-108">Alguns provedores de serviços mantêm todas as propriedades necessárias no perfil.</span><span class="sxs-lookup"><span data-stu-id="e7249-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="e7249-109">Outros provedores de serviços mantêm um conjunto parcial de propriedades no perfil e solicitam que o usuário especifique valores ausentes.</span><span class="sxs-lookup"><span data-stu-id="e7249-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="e7249-110">Outros provedores ainda não armazenam propriedades no perfil, contando com o usuário para fornecer todas as informações necessárias para a configuração.</span><span class="sxs-lookup"><span data-stu-id="e7249-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="e7249-111">Para recuperar as propriedades armazenadas no perfil</span><span class="sxs-lookup"><span data-stu-id="e7249-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="e7249-112">Chame [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md), passando o [MAPIUID](mapiuid.md) de seu provedor como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="e7249-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="e7249-113">Chame os métodos [IMAPIProp::](imapiprop-getprops.md) GetProps ou [IMAPIProp::](imapiprop-getproplist.md) getproplist da seção de perfil para recuperar propriedades individuais ou uma lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e7249-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="e7249-114">Para definir propriedades a partir de informações do usuário</span><span class="sxs-lookup"><span data-stu-id="e7249-114">To set properties from user information</span></span>
  
<span data-ttu-id="e7249-115">Exibe uma folha de propriedades, se MAPI não tiver definido um sinalizador proibindo a exibição.</span><span class="sxs-lookup"><span data-stu-id="e7249-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="e7249-116">Os sinalizadores a seguir indicam que uma interface do usuário não pode ser apresentada.</span><span class="sxs-lookup"><span data-stu-id="e7249-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="e7249-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="e7249-117">**Flag**</span></span>|<span data-ttu-id="e7249-118">**Provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="e7249-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e7249-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e7249-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e7249-120">Provedor de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="e7249-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="e7249-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e7249-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e7249-122">Provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="e7249-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="e7249-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e7249-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="e7249-124">Provedor de repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="e7249-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="e7249-125">Se seu provedor não armazenar todas as suas propriedades de configuração no perfil, exigindo interação do usuário, e o MAPI passar um dos sinalizadores de supressão da caixa de diálogo para seu método de logon, retorne MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="e7249-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="e7249-126">Também retorna esse erro quando o sinalizador de supressão de caixa de diálogo não está definido, mas o usuário não fornece todas as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="e7249-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="e7249-127">Quando o seu provedor de serviços falha em seu método de logon com MAPI_E_UNCONFIGURED, MAPI chama sua função de ponto de entrada novamente.</span><span class="sxs-lookup"><span data-stu-id="e7249-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="e7249-128">Se as informações não puderem ser localizadas com a segunda chamada, a sessão poderá ser encerrada, dependendo da importância de seu provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e7249-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="e7249-129">A ilustração a seguir mostra a lógica necessária para configuração no seu método de logon do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e7249-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="e7249-130">**Configuration verification flowchart**</span><span class="sxs-lookup"><span data-stu-id="e7249-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="e7249-131">![Fluxograma de verificação de configuração] (media/amapi_62.gif "Fluxograma de verificação de configuração")</span><span class="sxs-lookup"><span data-stu-id="e7249-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7249-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7249-132">See also</span></span>

- [<span data-ttu-id="e7249-133">Implementar o logon do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="e7249-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

