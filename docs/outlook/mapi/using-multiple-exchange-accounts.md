---
title: Usar várias contas do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Última modificação: 25 de julho de 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723058"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="61ee5-103">Usar várias contas do Exchange</span><span class="sxs-lookup"><span data-stu-id="61ee5-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="61ee5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61ee5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61ee5-105">Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam integração com várias contas de email do exchange.</span><span class="sxs-lookup"><span data-stu-id="61ee5-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange email accounts.</span></span> <span data-ttu-id="61ee5-106">No Outlook 2010 ou Outlook 2013, um usuário pode adicionar duas contas do exchange para o mesmo perfil e ainda aproveitar os recursos avançados do Exchange como a lista publicada de endereços global (GAL), a configuração do Exchange de ausência temporária e compartilhamento de pastas.</span><span class="sxs-lookup"><span data-stu-id="61ee5-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="61ee5-107">Esses familiarizado com as seções de perfil MAPI do Microsoft Office Outlook 2007 e versões anteriores sabem que as configurações do Exchange, como o nome de usuário de email e o nome do servidor, são armazenadas na seção perfil Global do Exchange fixa, **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the email user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="61ee5-108">No Outlook 2010 e o Outlook 2013, cada conta Exchange precisa sua própria seção de perfil para armazenar as configurações, tornando o **pbGlobalProfileSectionGuid** obsoleto.</span><span class="sxs-lookup"><span data-stu-id="61ee5-108">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="61ee5-109">Configurações do Outlook 2010 e o Outlook 2013 Exchange ainda são armazenadas no perfil, mas um identificador exclusivo para a seção de perfil que contém suas configurações, que é alocado dinamicamente por perfil.</span><span class="sxs-lookup"><span data-stu-id="61ee5-109">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile.</span></span> <span data-ttu-id="61ee5-110">A localização das configurações do Exchange no perfil é armazenada na [Propriedade canônico de PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), que podem ser encontradas na seção de perfil de serviço de mensagem da conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="61ee5-110">The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account.</span></span> <span data-ttu-id="61ee5-111">Essa propriedade também pode ser encontrada na seção de perfil de cada provedor neste serviço de mensagem da conta.</span><span class="sxs-lookup"><span data-stu-id="61ee5-111">This property can also be found in the profile section for each provider in this message service of the account.</span></span> <span data-ttu-id="61ee5-112">O identificador exclusivo não está armazenado no servidor e será diferente nos perfis.</span><span class="sxs-lookup"><span data-stu-id="61ee5-112">The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="61ee5-113">Outlook 2010 e o Outlook 2013 usam o **PidTagExchangeProfileSectionId** como um identificador exclusivo para especificar uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="61ee5-113">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account.</span></span> <span data-ttu-id="61ee5-114">Quando usado dessa maneira, esse identificador exclusivo é conhecido como o **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-114">When used in this manner, this unique identifier is known as the **emsmdbUID**.</span></span> <span data-ttu-id="61ee5-115">Para algumas operações MAPI e o Outlook, um **emsmdbUID** pode ser necessária para especificar qual conta Exchange deve ser usada para a operação.</span><span class="sxs-lookup"><span data-stu-id="61ee5-115">For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="61ee5-116">Para oferecer suporte a várias contas do Exchange, você deve usar algumas chamadas para novas funções em seu código.</span><span class="sxs-lookup"><span data-stu-id="61ee5-116">In order to support multiple Exchange accounts, you must use some calls to new functions in your code.</span></span> <span data-ttu-id="61ee5-117">Substitua qualquer chamada que usa uma **entryID** e [IAddrBook::OpenEntry](iaddrbook-openentry.md) ou [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) em [IMailUser: IMAPIProp](imailuserimapiprop.md) e [IDistList: IMAPIContainer](idistlistimapicontainer.md) com uma das funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ee5-117">Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="61ee5-118">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="61ee5-118">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="61ee5-119">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="61ee5-119">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="61ee5-120">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="61ee5-120">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="61ee5-121">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="61ee5-121">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="61ee5-122">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="61ee5-122">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="61ee5-123">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="61ee5-123">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="61ee5-124">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="61ee5-124">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="61ee5-125">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="61ee5-125">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="61ee5-126">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="61ee5-126">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="61ee5-127">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="61ee5-127">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="61ee5-128">Suporte de legado</span><span class="sxs-lookup"><span data-stu-id="61ee5-128">Legacy support</span></span>

<span data-ttu-id="61ee5-129">Todos os clientes MAPI escritos antes da criação da nova seção **emsmdbUID** ainda são suportados.</span><span class="sxs-lookup"><span data-stu-id="61ee5-129">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported.</span></span> <span data-ttu-id="61ee5-130">Esses clientes continuarão recuperar a seção global anterior, **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-130">These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="61ee5-131">Consultas para esta seção de perfil serão redirecionadas para uma conta do Exchange designada que processa consultas herdadas.</span><span class="sxs-lookup"><span data-stu-id="61ee5-131">Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries.</span></span> <span data-ttu-id="61ee5-132">A conta que processa as chamadas herdadas pode ser determinada olhando a tabela de serviços de mensagem e adicionando uma coluna para PR_EMSMDB_LEGACY.</span><span class="sxs-lookup"><span data-stu-id="61ee5-132">The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY.</span></span> <span data-ttu-id="61ee5-133">Somente um serviço de mensagem terá essa definição como true e seu **PidTagExchangeProfileSectionId** é chamado de legado **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-133">Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61ee5-134">Configurações de MAPI configuráveis, como o repositório padrão e a conta padrão não têm efeito no qual a conta processa as chamadas de legado.</span><span class="sxs-lookup"><span data-stu-id="61ee5-134">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls.</span></span> <span data-ttu-id="61ee5-135">A conta que processa as chamadas herdadas não pode ser configurada.</span><span class="sxs-lookup"><span data-stu-id="61ee5-135">The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="61ee5-136">O **emsmdbUID** da conta herdada é copiado para a seção perfil Global do Outlook.</span><span class="sxs-lookup"><span data-stu-id="61ee5-136">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section.</span></span> <span data-ttu-id="61ee5-137">Se essa propriedade não existir, consultando a tabela de serviços de mensagens determinar qual conta está o manipulador de legado e defina o valor na seção Global do perfil do Outlook.</span><span class="sxs-lookup"><span data-stu-id="61ee5-137">If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="61ee5-138">Seja claro, a seção de perfil do Outlook Global difere a seção de perfil Global do Exchange e no Outlook 2010 e o Outlook 2013 a seção de perfil Global do Exchange não é mais realmente global porque é possível ter várias contas do Exchange.</span><span class="sxs-lookup"><span data-stu-id="61ee5-138">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts.</span></span> <span data-ttu-id="61ee5-139">A seção de perfil do Outlook Global contém propriedades sobre o Outlook, como o estado da pasta MRU ou o estado da conexão a global.</span><span class="sxs-lookup"><span data-stu-id="61ee5-139">The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="61ee5-140">Contextos de contas do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="61ee5-140">Address Book Account Contexts</span></span>

<span data-ttu-id="61ee5-141">Para resolver endereços corretamente com várias contas do Exchange, use as novas funções que obtenha um contexto de conta, para que a conta do Exchange correta de pesquisa de chamadas para o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="61ee5-141">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="61ee5-142">Alguns catálogo de endereços anterior que APIs foram preteridas porque as APIs não foram totalmente vários Exchange capaz.</span><span class="sxs-lookup"><span data-stu-id="61ee5-142">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable.</span></span> <span data-ttu-id="61ee5-143">Nesse contexto da conta geralmente é um **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-143">This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="61ee5-144">Além do **emsmdbUID**, várias contas do Exchange também têm um **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-144">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="61ee5-145">O valor de **emsmdbUID** identifica o contexto de conta.</span><span class="sxs-lookup"><span data-stu-id="61ee5-145">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="61ee5-146">O valor de **emsabpUID** identifica um fornecedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="61ee5-146">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="61ee5-147">O valor de **emsabpUID** geralmente é usado ao resolver um destinatário.</span><span class="sxs-lookup"><span data-stu-id="61ee5-147">The **emsabpUID** value is typically used when resolving a recipient.</span></span> <span data-ttu-id="61ee5-148">Ao resolver um destinatário usando [IAddrBook::ResolveName](iaddrbook-resolvename.md), uma linha de destinatário do Exchange contém a propriedade **PR_AB_PROVIDERS** (0x3D010102), que contém o valor de **emsabpUID** .</span><span class="sxs-lookup"><span data-stu-id="61ee5-148">When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value.</span></span> <span data-ttu-id="61ee5-149">Esse valor **emsabpUID** identifica o provedor de catálogo de endereços do Exchange para o destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="61ee5-149">This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="61ee5-150">Se você deseja determinar o valor de **emsabpUID** para um determinado **emsmdbUID**, abra a seção de perfil para o **emsmdbUID** e obter a propriedade **PR_EMSABP_USER_UID** (0x0x3D1A0102).</span><span class="sxs-lookup"><span data-stu-id="61ee5-150">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="61ee5-151">Se você estiver chamando [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), certifique-se de que os destinatários do Exchange na lista que você passar em contenham a propriedade **PR_AB_PROVIDERS** que tem o **emsabpUID** que corresponde ao provedor de catálogo de endereços que o destinatário pertence.</span><span class="sxs-lookup"><span data-stu-id="61ee5-151">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to.</span></span> <span data-ttu-id="61ee5-152">Chamar [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) em uma linha que você obteve de [IAddrBook::ResolveName](iaddrbook-resolvename.md) requer nenhuma ação adicional, mas alguns códigos chamará [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) em linhas que contêm apenas **PR_ENTRYID** propriedade.</span><span class="sxs-lookup"><span data-stu-id="61ee5-152">Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property.</span></span> <span data-ttu-id="61ee5-153">Linhas neste e situações semelhantes devem conter **PR_ENTRYID** e o **PR_AB_PROVIDERS** com a propriedade **PR_AB_PROVIDERS** definida como o correto **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-153">Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="61ee5-154">Uma descrição simples do que o processo de resolução de várias contas do Exchange é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="61ee5-154">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="61ee5-155">Dado o identificador exclusivo do serviço, seu código procura no índice de armazenamento de mensagens da propriedade **PR_SERVICE_UID** que corresponde ao que você precisa.</span><span class="sxs-lookup"><span data-stu-id="61ee5-155">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have.</span></span> <span data-ttu-id="61ee5-156">A partir daí, você pode determinar o correto **PR_MDB_PROVIDER**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-156">From there, you can determine the correct **PR_MDB_PROVIDER**.</span></span> <span data-ttu-id="61ee5-157">Esta linha contém o store apropriado.</span><span class="sxs-lookup"><span data-stu-id="61ee5-157">This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="61ee5-158">Dado um **emsmdbUID**, seu código procura na tabela de serviços de mensagem para a linha que expõe a **PidTagExchangeProfileSectionId** que corresponde a **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-158">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61ee5-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="61ee5-159">See also</span></span>



[<span data-ttu-id="61ee5-160">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="61ee5-160">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="61ee5-161">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="61ee5-161">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="61ee5-162">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="61ee5-162">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="61ee5-163">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="61ee5-163">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="61ee5-164">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="61ee5-164">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="61ee5-165">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="61ee5-165">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="61ee5-166">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="61ee5-166">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="61ee5-167">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="61ee5-167">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="61ee5-168">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="61ee5-168">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="61ee5-169">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="61ee5-169">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="61ee5-170">Propriedade canônica PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="61ee5-170">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="61ee5-171">Como abrir a seção perfil Global</span><span class="sxs-lookup"><span data-stu-id="61ee5-171">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

