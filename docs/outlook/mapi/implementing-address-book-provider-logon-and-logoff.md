---
title: Implementando logon e logoff do provedor de agendamento de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438733"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="3eabb-103">Implementando logon e logoff do provedor de agendamento de endereços</span><span class="sxs-lookup"><span data-stu-id="3eabb-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="3eabb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3eabb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3eabb-105">Os provedores de agendamento de endereços suportam logon e logoff de sessão implementando os métodos do [IABProvider : interface IUnknown.](iabprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="3eabb-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="3eabb-106">A interface \*\* IABProvider \*\* herda diretamente de **IUnknown** e adiciona apenas dois outros métodos: **Logon** e **Desligamento.**</span><span class="sxs-lookup"><span data-stu-id="3eabb-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="3eabb-107">Logoff</span><span class="sxs-lookup"><span data-stu-id="3eabb-107">Logoff</span></span>

<span data-ttu-id="3eabb-108">O MAPI chamará o método [IABProvider::Logon](iabprovider-logon.md) do provedor no início de cada sessão e sempre que o provedor for adicionado ao perfil atual e o cliente suportar a reconfiguração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="3eabb-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="3eabb-109">Quando o MAPI chama o **método IABProvider::Logon,** seu provedor de agendamento inicia o processo de logon.</span><span class="sxs-lookup"><span data-stu-id="3eabb-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="3eabb-110">**Para implementar IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="3eabb-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="3eabb-111">Inicialize todos os ponteiros do parâmetro de saída passados pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="3eabb-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="3eabb-112">Chame o método **IUnknown::AddRef** do objeto de suporte para incrementar sua contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="3eabb-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="3eabb-113">Chame o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) do objeto de suporte para abrir a seção do perfil que contém informações de configuração sobre seu provedor.</span><span class="sxs-lookup"><span data-stu-id="3eabb-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="3eabb-114">Passe NULL para  _o parâmetro lpUID_ e o sinalizador MAPI_MODIFY se você pretende fazer alterações.</span><span class="sxs-lookup"><span data-stu-id="3eabb-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="3eabb-115">Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) da seção de perfil para recuperar as propriedades que seu provedor precisa para logon, como o nome do arquivo de dados ou da tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3eabb-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="3eabb-116">Verifique se as propriedades estão disponíveis e válidas.</span><span class="sxs-lookup"><span data-stu-id="3eabb-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="3eabb-117">Se necessário e permitido, exiba uma caixa de diálogo para solicitar que o usuário faça correções ou adições a informações inválidas ou ausentes e chame o método [IMAPIProp::SetProps](imapiprop-setprops.md) da seção de perfil para salvar quaisquer alterações.</span><span class="sxs-lookup"><span data-stu-id="3eabb-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="3eabb-118">Algumas das propriedades comuns que devem estar disponíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="3eabb-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="3eabb-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3eabb-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="3eabb-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3eabb-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="3eabb-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3eabb-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="3eabb-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3eabb-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="3eabb-123">Não defina **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3eabb-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="3eabb-124">No momento do logon, essas propriedades são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3eabb-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="3eabb-125">Se uma ou mais propriedades de configuração não estão disponíveis, falhe e retorne o valor MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="3eabb-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="3eabb-126">Chame [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar um [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="3eabb-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="3eabb-127">Seu provedor pode criar um **MAPIUID:**</span><span class="sxs-lookup"><span data-stu-id="3eabb-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="3eabb-128">Chamando o [método IMAPISupport::NewUID.](imapisupport-newuid.md)</span><span class="sxs-lookup"><span data-stu-id="3eabb-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="3eabb-129">Chamar a UUIDGEN.EXE para definir um GUID que seu provedor usa para incluir em um de seus arquivos de header.</span><span class="sxs-lookup"><span data-stu-id="3eabb-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="3eabb-130">Se desejado, salve um **MAPIUID** recém-criado no perfil atual chamando o método \*\* IMAPIProp::SetProps \*\* da seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="3eabb-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="3eabb-131">Libere a seção de perfil chamando seu **método IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="3eabb-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="3eabb-132">In instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span><span class="sxs-lookup"><span data-stu-id="3eabb-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="3eabb-133">Como é possível que o MAPI chame seu método \*\* Logon \*\* várias vezes durante uma sessão, é sensato dar suporte a essa possibilidade em sua implementação, sendo capaz de criar vários objetos de logon e acompanhar cada objeto que é criado.</span><span class="sxs-lookup"><span data-stu-id="3eabb-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="3eabb-134">O suporte a várias chamadas de Logon permite que um usuário de um aplicativo cliente, por exemplo, faça **logon** em uma sessão com identidades diferentes ou use destinos de entrega diferentes.</span><span class="sxs-lookup"><span data-stu-id="3eabb-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="3eabb-135">**O** desligamento é chamado quando a sessão termina.</span><span class="sxs-lookup"><span data-stu-id="3eabb-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="3eabb-136">O MAPI chama [o método IABProvider::Shutdown](iabprovider-shutdown.md) como uma das últimas tarefas envolvidas no desligamento de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="3eabb-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="3eabb-137">A MAPI liberou todos os objetos de logon do provedor e, quando o provedor recebe essa chamada, pode assumir que esta é a última chamada que receberá.</span><span class="sxs-lookup"><span data-stu-id="3eabb-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="3eabb-138">Na implementação do **IABProvider::Shutdown,** execute qualquer limpeza final necessária.</span><span class="sxs-lookup"><span data-stu-id="3eabb-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="3eabb-139">Por exemplo, seu provedor pode chamar **MAPIDeinitIdle** se tiver chamado **MAPIInitIdle** para usar o mecanismo ocioso durante a sessão ou o método **IUnknown::Release** de quaisquer objetos que ainda não tenham sido liberados.</span><span class="sxs-lookup"><span data-stu-id="3eabb-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="3eabb-140">Se o provedor não tiver uma limpeza final, sua implementação poderá ser feita de uma única linha de código:</span><span class="sxs-lookup"><span data-stu-id="3eabb-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


