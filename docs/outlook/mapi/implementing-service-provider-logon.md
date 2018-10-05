---
title: Implementar o logon do provedor de serviços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401640"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="70860-103">Implementar o logon do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="70860-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="70860-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70860-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70860-105">MAPI chama um método em seu objeto provedor para começar o processo de logon usando o ponteiro que você retornar de sua função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="70860-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="70860-106">O método varia, dependendo do tipo de provedor de serviços da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="70860-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="70860-107">[IABProvider::Logon](iabprovider-logon.md) para provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="70860-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="70860-108">[IMSProvider::Logon](imsprovider-logon.md) para provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="70860-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="70860-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="70860-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="70860-110">Execute as seguintes tarefas em qualquer método de logon que você implementar:</span><span class="sxs-lookup"><span data-stu-id="70860-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="70860-111">Incrementa a contagem de referência no objeto suporte que é passada como um parâmetro de entrada chamando o método [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="70860-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="70860-112">Chame o suporte ao método do objeto [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para acessar a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="70860-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="70860-113">Chame o método de [IMAPIProp::SetProps](imapiprop-setprops.md) da seção perfil para definir as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="70860-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="70860-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70860-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="70860-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70860-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="70860-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70860-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="70860-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70860-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="70860-118">Não tente definir as propriedades da seção perfil **PR_RESOURCE_FLAGS** ou **PR_PROVIDER_DLL_NAME** .</span><span class="sxs-lookup"><span data-stu-id="70860-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="70860-119">Ao fazer logon, essas propriedades são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="70860-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="70860-120">Verifique se as propriedades que você precisa para que a configuração seja são armazenadas no perfil ou estão disponíveis a partir do usuário.</span><span class="sxs-lookup"><span data-stu-id="70860-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="70860-121">Para obter mais informações sobre como verificar sua configuração, consulte [Verificando a configuração de provedor de serviços](verifying-service-provider-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="70860-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="70860-122">Chame o método de [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) de suporte do objeto para registrar um identificador exclusivo, ou [MAPIUID](mapiuid.md), se seu provedor for um provedor de repositório de catálogo ou mensagem de endereço.</span><span class="sxs-lookup"><span data-stu-id="70860-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="70860-123">Provedores de transporte registrar estruturas **MAPIUID** quando o método seus [IXPLogon::AddressTypes](ixplogon-addresstypes.md) chamadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="70860-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="70860-124">Para obter mais informações sobre como registrar um **MAPIUID**, consulte [Registrando serviço provedor exclusivo identificadores](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="70860-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="70860-125">Criar uma instância de um objeto de logon e voltar com um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="70860-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="70860-126">S_OK para indicar um logon bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="70860-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="70860-127">MAPI_E_UNCONFIGURED para indicar que um ou mais das propriedades de configuração não estavam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="70860-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="70860-128">MAPI_E_USER_CANCEL para indicar que o usuário cancelou a caixa de diálogo Configuração, fazendo com que as propriedades de configuração estar disponível.</span><span class="sxs-lookup"><span data-stu-id="70860-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="70860-129">MAPI_E_FAILONEPROVIDER para indicar que o provedor não pôde ser configurado, mas que MAPI deve permitir que ela seja usada independentemente.</span><span class="sxs-lookup"><span data-stu-id="70860-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="70860-130">Métodos de logon devem retornar esse valor para reportar um erro não fatal, como quando o provedor exige uma senha e não pode solicitar ao usuário para que ele porque a interface do usuário está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="70860-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="70860-131">A lista anterior de tarefas descreve uma implementação mínima para um método de logon do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="70860-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="70860-132">Você pode incluir a funcionalidade adicional, se necessário.</span><span class="sxs-lookup"><span data-stu-id="70860-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="70860-133">Por exemplo, alguns provedores chamarem [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para atualizar a tabela de status em seu método de logon.</span><span class="sxs-lookup"><span data-stu-id="70860-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="70860-134">Para obter o melhor desempenho na hora do logon, evite chamar [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) ou [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="70860-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="70860-135">Antes que essas chamadas podem concluir e retornar o controle ao seu método de logon, o MAPI spooler deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="70860-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70860-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="70860-136">See also</span></span>

- [<span data-ttu-id="70860-137">Iniciar um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="70860-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

