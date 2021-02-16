---
title: Implementando o logon do provedor de serviços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310084"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="34184-103">Implementando o logon do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="34184-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="34184-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34184-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span><span class="sxs-lookup"><span data-stu-id="34184-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="34184-106">O método varia da seguinte forma, dependendo do tipo de seu provedor de serviços:</span><span class="sxs-lookup"><span data-stu-id="34184-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="34184-107">[IABProvider::Logon para](iabprovider-logon.md) provedores de agendas</span><span class="sxs-lookup"><span data-stu-id="34184-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="34184-108">[IMSProvider::Logon para](imsprovider-logon.md) provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="34184-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="34184-109">[IXPProvider::TransportLogon para](ixpprovider-transportlogon.md) provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="34184-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="34184-110">Execute as seguintes tarefas em qualquer método de logon implementado:</span><span class="sxs-lookup"><span data-stu-id="34184-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="34184-111">Incremente a contagem de referência no objeto de suporte que é passado como um parâmetro de entrada chamando seu [método IUnknown::AddRef.](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34184-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="34184-112">Chame o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) do objeto de suporte para acessar sua seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="34184-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="34184-113">Chame o método [IMAPIProp::SetProps](imapiprop-setprops.md) da seção de perfil para definir as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="34184-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="34184-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34184-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="34184-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34184-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="34184-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34184-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="34184-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34184-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="34184-118">Não tente definir as propriedades de PR_RESOURCE_FLAGS **ou** PR_PROVIDER_DLL_NAME **perfil.**</span><span class="sxs-lookup"><span data-stu-id="34184-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="34184-119">No momento do logon, essas propriedades são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="34184-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="34184-120">Verifique se as propriedades que você precisa para a configuração estão armazenadas no perfil ou estão disponíveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="34184-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="34184-121">Para obter mais informações sobre como verificar sua configuração, consulte [Verificando a configuração do provedor de serviços.](verifying-service-provider-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="34184-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="34184-122">Chame o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) do objeto de suporte para registrar um identificador exclusivo, ou [MAPIUID,](mapiuid.md)se seu provedor for um provedor de armazenamento de mensagens ou de um address book.</span><span class="sxs-lookup"><span data-stu-id="34184-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="34184-123">Os provedores de transporte **registram estruturas MAPIUID** quando o MAPI chama seu [método IXPLogon::AddressTypes.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="34184-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="34184-124">Para obter mais informações sobre como registrar um **MAPIUID,** consulte Registro de identificadores exclusivos do [provedor de serviços.](registering-service-provider-unique-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="34184-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="34184-125">Insinue um objeto de logon e retorne com um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="34184-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="34184-126">S_OK para indicar um logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="34184-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="34184-127">MAPI_E_UNCONFIGURED para indicar que uma ou mais das propriedades de configuração não estavam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="34184-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="34184-128">MAPI_E_USER_CANCEL para indicar que o usuário cancelou a caixa de diálogo de configuração, causando a indisponibilidade das propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="34184-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="34184-129">MAPI_E_FAILONEPROVIDER para indicar que seu provedor não pôde ser configurado, mas que o MAPI deve permitir que ele seja usado independentemente.</span><span class="sxs-lookup"><span data-stu-id="34184-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="34184-130">Os métodos de logon devem retornar esse valor para relatar um erro não funcional, como quando o provedor exige uma senha e não pode solicitar ao usuário porque a interface do usuário está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="34184-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="34184-131">A lista anterior de tarefas descreve uma implementação mínima para um método de logon do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="34184-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="34184-132">Você pode incluir funcionalidade adicional, se necessário.</span><span class="sxs-lookup"><span data-stu-id="34184-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="34184-133">Por exemplo, alguns provedores chamam [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para atualizar a tabela de status no método de logon.</span><span class="sxs-lookup"><span data-stu-id="34184-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="34184-134">Para obter o melhor desempenho no momento do logon, evite chamar [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) ou [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="34184-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="34184-135">Antes que essas chamadas possam ser concluídas e retornem o controle ao método de logon, o spooler MAPI deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="34184-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34184-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="34184-136">See also</span></span>

- [<span data-ttu-id="34184-137">Iniciando um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="34184-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

