---
title: Implementar o logon e logoff do provedor do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f26e7b7ec607c9714012870d5367a0e775c62f34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572099"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="ebb0c-103">Implementar o logon e logoff do provedor do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="ebb0c-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="ebb0c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebb0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebb0c-105">Provedores de catálogo de endereços oferecem suporte a sessão logon e logoff Implementando os métodos para o [IABProvider: IUnknown](iabprovideriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="ebb0c-106">O \* \* IABProvider \* \* interface herda diretamente da **IUnknown** e adiciona apenas dois outros métodos: **Logon** e **desligamento**.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="ebb0c-107">Fazer logoff</span><span class="sxs-lookup"><span data-stu-id="ebb0c-107">Logoff</span></span>

<span data-ttu-id="ebb0c-108">MAPI chamará o método [IABProvider::Logon](iabprovider-logon.md) do seu provedor de serviço no início de cada sessão e sempre que o seu provedor é adicionado ao perfil atual e o cliente oferece suporte a reconfiguração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="ebb0c-109">Quando MAPI chama o método **IABProvider::Logon** , seu provedor de catálogo de endereços começa seu processo de logon.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="ebb0c-110">**Para implementar IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="ebb0c-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="ebb0c-111">Inicialize todos os ponteiros de parâmetro de saída passados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="ebb0c-112">Chame o suporte ao método do objeto **AddRef** para incrementar sua contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="ebb0c-113">Chame o suporte ao método do objeto [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para abrir a seção do perfil que contém informações sobre o seu provedor de configuração.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="ebb0c-114">Passe nulo para o parâmetro _lpUID_ e o sinalizador MAPI_MODIFY se você pretende fazer alterações.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="ebb0c-115">Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da seção perfil para recuperar as propriedades que precisa de seu provedor de logon, como o nome da tabela de banco de dados ou arquivo de dados.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="ebb0c-116">Verifique se as propriedades estão todos disponíveis e válido.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="ebb0c-117">Se necessário e permitidos, exibe uma caixa de diálogo para solicitar que o usuário faça correções ou adições à informações ausentes ou inválidas e chamar o método de [IMAPIProp::SetProps](imapiprop-setprops.md) da seção perfil para salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="ebb0c-118">Algumas das propriedades comuns que deveriam estar disponíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="ebb0c-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="ebb0c-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ebb0c-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="ebb0c-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ebb0c-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="ebb0c-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ebb0c-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="ebb0c-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ebb0c-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="ebb0c-123">Não defina **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ebb0c-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="ebb0c-124">Ao fazer logon, essas propriedades são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="ebb0c-125">Se uma ou mais propriedades de configuração não estiverem disponíveis, falhar e retornar o valor MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="ebb0c-126">Chame [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar um [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="ebb0c-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="ebb0c-127">Seu provedor pode criar um **MAPIUID** por:</span><span class="sxs-lookup"><span data-stu-id="ebb0c-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="ebb0c-128">Chamando o método [IMAPISupport::NewUID](imapisupport-newuid.md) .</span><span class="sxs-lookup"><span data-stu-id="ebb0c-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="ebb0c-129">Chamar o UUIDGEN. Ferramenta EXE para definir um GUID que seu provedor usa para incluir em um dos seus arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="ebb0c-130">Se preferir, salve um recém-criado **MAPIUID** no perfil atual chamando-se a seção de perfil \* \* IMAPIProp::SetProps \* \* método.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="ebb0c-131">Libere a seção perfil chamando seu método **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="ebb0c-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="ebb0c-132">Criar uma instância de um novo objeto de logon e defina o conteúdo do parâmetro _lppABLogon_ como o endereço desse novo objeto.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="ebb0c-133">Porque é possível de MAPI chamar seu \* \* Logon \* \* método várias vezes durante uma sessão, é recomendável suportar essa possibilidade em sua implementação por ser capaz de criar vários objetos de logon e manter um registro de cada objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="ebb0c-134">Suporte a várias chamadas de **Logon** permite que um usuário de um aplicativo cliente, por exemplo, para fazer logon em uma sessão com diferentes identidades ou destinos de entrega diferente de uso.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="ebb0c-135">**Desligamento** é chamado quando a sessão está terminando.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="ebb0c-136">MAPI chama seu método [IABProvider::Shutdown](iabprovider-shutdown.md) como uma das últimas tarefas envolvidas na desligando a uma sessão.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="ebb0c-137">MAPI lançou todos os objetos de logon do seu provedor e, quando o seu provedor recebe essa chamada, ele pode assumir que esta é a última chamada, que ele receberá.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="ebb0c-138">Na sua implementação do **IABProvider::Shutdown**, execute qualquer limpeza final que você acha que é necessário.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="ebb0c-139">Por exemplo, seu provedor pode chamar **MAPIDeinitIdle** se ele tiver chamado **MAPIInitIdle** para usar o mecanismo de ociosidade durante a sessão ou o método **IUnknown:: Release** todos os objetos que ainda precisam ser liberada.</span><span class="sxs-lookup"><span data-stu-id="ebb0c-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="ebb0c-140">Se o seu provedor não tem nenhuma limpeza final, sua implementação pode ser constituída de uma única linha de código:</span><span class="sxs-lookup"><span data-stu-id="ebb0c-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


