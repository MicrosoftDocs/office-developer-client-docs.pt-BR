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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418845"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="05148-103">Verificar a configuração do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="05148-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="05148-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05148-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05148-105">O método de logon ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)ou [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) deve verificar a configuração do provedor.</span><span class="sxs-lookup"><span data-stu-id="05148-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="05148-106">Isso envolve a verificação de que todas as propriedades necessárias para a operação completa estão definidas corretamente.</span><span class="sxs-lookup"><span data-stu-id="05148-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="05148-107">Cada provedor requer um número diferente de propriedades; depende do provedor e do grau de interação do usuário que você permite.</span><span class="sxs-lookup"><span data-stu-id="05148-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="05148-108">Alguns provedores de serviços mantêm todas as propriedades necessárias no perfil.</span><span class="sxs-lookup"><span data-stu-id="05148-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="05148-109">Outros provedores de serviços mantêm um conjunto parcial de propriedades no perfil e solicitam valores ausentes ao usuário.</span><span class="sxs-lookup"><span data-stu-id="05148-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="05148-110">Ainda assim, outros provedores não armazenam propriedades no perfil, confiando no usuário para fornecer todas as informações necessárias para a configuração.</span><span class="sxs-lookup"><span data-stu-id="05148-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="05148-111">Para recuperar propriedades armazenadas no perfil</span><span class="sxs-lookup"><span data-stu-id="05148-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="05148-112">Chame [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passando [o MAPIUID](mapiuid.md) do seu provedor como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="05148-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="05148-113">Chame os métodos [IMAPIProp::GetProps](imapiprop-getprops.md) ou [IMAPIProp::GetPropList](imapiprop-getproplist.md) da seção de perfil para recuperar propriedades individuais ou uma lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="05148-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="05148-114">Para definir propriedades de informações do usuário</span><span class="sxs-lookup"><span data-stu-id="05148-114">To set properties from user information</span></span>
  
<span data-ttu-id="05148-115">Exibir uma folha de propriedades, se MAPI não tiver definido um sinalizador proibindo a exibição.</span><span class="sxs-lookup"><span data-stu-id="05148-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="05148-116">Os sinalizadores a seguir indicam que uma interface do usuário não pode ser apresentada.</span><span class="sxs-lookup"><span data-stu-id="05148-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="05148-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="05148-117">**Flag**</span></span>|<span data-ttu-id="05148-118">**Provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="05148-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05148-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="05148-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="05148-120">Provedor de agendas</span><span class="sxs-lookup"><span data-stu-id="05148-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="05148-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="05148-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="05148-122">Provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="05148-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="05148-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="05148-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="05148-124">Provedor de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="05148-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="05148-125">Se o provedor não armazenar todas as suas propriedades de configuração no perfil, exigindo interação do usuário, e o MAPI passar um dos sinalizadores de supressão da caixa de diálogo para o método de logon, retorne MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="05148-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="05148-126">Também retornará esse erro quando o sinalizador de supressão de caixa de diálogo não estiver definido, mas o usuário não fornecerá todas as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="05148-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="05148-127">Quando o provedor de serviços falha no método de logon com MAPI_E_UNCONFIGURED, o MAPI chama sua função de ponto de entrada novamente.</span><span class="sxs-lookup"><span data-stu-id="05148-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="05148-128">Se as informações não puderem ser localizadas com a segunda chamada, a sessão poderá ser encerrada, dependendo da importância do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="05148-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="05148-129">A ilustração a seguir mostra a lógica necessária para a configuração no método de logon do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="05148-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="05148-130">**Configuration verification flowchart**</span><span class="sxs-lookup"><span data-stu-id="05148-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="05148-131">![Fluxograma verificação de configuração](media/amapi_62.gif "Fluxograma verificação de configuração")</span><span class="sxs-lookup"><span data-stu-id="05148-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05148-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="05148-132">See also</span></span>

- [<span data-ttu-id="05148-133">Implementando o logon do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="05148-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

