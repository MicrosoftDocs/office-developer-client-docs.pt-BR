---
title: Usando o CSISyncClient para controlar o cache de documentos do Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Saiba como usar o CSISyncClient para controlar o cache de documentos do Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346253"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="13e88-103">Usando o CSISyncClient para controlar o cache de documentos do Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="13e88-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="13e88-104">Saiba como usar o CSISyncClient para controlar o cache de documentos do Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="13e88-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="13e88-105">CSISyncClient é um servidor COM fora de processamento (CsiSyncClient. exe) que permite que o Microsoft OneDrive controle o comportamento do cache de documentos do Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="13e88-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="13e88-106">Por exemplo, o OneDrive pode chamar no ODC via CSISyncClient para carregar e baixar arquivos para e de pontos de extremidade habilitados para MS-FSSHTTP.</span><span class="sxs-lookup"><span data-stu-id="13e88-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="13e88-107">Isso permite recursos avançados de suporte de serviço no Office, como transições de coautoria e sem interrupções de offline para online.</span><span class="sxs-lookup"><span data-stu-id="13e88-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="13e88-108">O CsiSyncClient está disponível na área de trabalho do Office (tanto x86 quanto x64).</span><span class="sxs-lookup"><span data-stu-id="13e88-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="13e88-109">Observação: embora as versões mais recentes do Office possam ser fornecidas com o CsiSyncClient, o processo será usado apenas para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="13e88-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="13e88-110">A interface CsiSyncClient e a metodologia de controle do ODC serão alteradas em futuras versões do Office.</span><span class="sxs-lookup"><span data-stu-id="13e88-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="13e88-111">A ID de classe está atualmente definida para responder apenas ao OneDrive.</span><span class="sxs-lookup"><span data-stu-id="13e88-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="13e88-112">O objeto COM é utilizável como um servidor COM fora do processamento e é executado no CsiSyncClient. exe.</span><span class="sxs-lookup"><span data-stu-id="13e88-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="13e88-113">Devido às limitações com o Access (que o ODC usa), ele é fornecido com o tipo de bit que o Office entra, de modo que o Office x64 significa um objeto COM x64 ou o x86 Office significa um objeto COM x86.</span><span class="sxs-lookup"><span data-stu-id="13e88-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="13e88-114">Para contornar essa limitação, especificar CLSCTX_LOCAL_SERVER como parte do CoCreateInstance terá o objeto COM hospedado como um servidor COM fora de processamento, permitindo a compatibilidade de bits cruzados.</span><span class="sxs-lookup"><span data-stu-id="13e88-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="13e88-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="13e88-115">Interfaces</span></span>

<span data-ttu-id="13e88-116">O CSISyncClient usa as seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="13e88-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="13e88-117">Interface ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="13e88-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="13e88-118">Esta é a interface principal usada para sincronizar arquivos no Office.</span><span class="sxs-lookup"><span data-stu-id="13e88-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="13e88-119">ProgID: Office. LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="13e88-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="13e88-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="13e88-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="13e88-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="13e88-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="13e88-122">O objeto COM que é exposto é usado como um servidor fora de processamento.</span><span class="sxs-lookup"><span data-stu-id="13e88-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="13e88-123">A especificação de CLSCTX_LOCAL_SERVER como parte de CoCreateInstance permite a compatibilidade entre processos de 64 bits e 32 bits.</span><span class="sxs-lookup"><span data-stu-id="13e88-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="13e88-124">Depois de criar o objeto COM, você deve chamar [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) primeiro.</span><span class="sxs-lookup"><span data-stu-id="13e88-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="13e88-125">Após o [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ter sido concluída com êxito, você pode chamar qualquer API com a frequência desejada e em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="13e88-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="13e88-126">Você também pode chamar [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) em um objeto já inicializado, mas isso não faz nada.</span><span class="sxs-lookup"><span data-stu-id="13e88-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="13e88-127">As exceções para o parágrafo anterior são [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) e [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="13e88-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="13e88-128">Depois de chamar [ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) no objeto com, você deve destruir o objeto e criar um novo.</span><span class="sxs-lookup"><span data-stu-id="13e88-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="13e88-129">[ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) excluirá seu subcache, excluirá todas as informações de arquivo associadas no cache, mas deixará os documentos em disco.</span><span class="sxs-lookup"><span data-stu-id="13e88-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="13e88-130">Também deixa o estado intacto para se comunicar com o cache.</span><span class="sxs-lookup"><span data-stu-id="13e88-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="13e88-131">Isso permite chamar [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) novamente para criar um novo cache sem ter que destruir e recriar o objeto com.</span><span class="sxs-lookup"><span data-stu-id="13e88-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="13e88-132">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13e88-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="13e88-133">ILSCLocalSyncClient::D eleteFile</span><span class="sxs-lookup"><span data-stu-id="13e88-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="13e88-134">DeleteFile é usado para remover as informações de arquivo do cache.</span><span class="sxs-lookup"><span data-stu-id="13e88-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="13e88-135">No enTanto, esse método deixará o arquivo associado no disco e no servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="13e88-136">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-136">Parameters</span></span>

 <span data-ttu-id="13e88-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13e88-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="13e88-138">A cadeia de caracteres que identifica o reSourceid do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="13e88-139">Este valor deve ser não vazio com um máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-140">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-140">Return values</span></span>

|<span data-ttu-id="13e88-141">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-141">Value</span></span>|<span data-ttu-id="13e88-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-144">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-146">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-148">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13e88-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13e88-150">O reSourceid fornecido não está no cache.</span><span class="sxs-lookup"><span data-stu-id="13e88-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="13e88-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-152">A inicialização não foi chamada com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="13e88-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="13e88-154">O arquivo está atualmente sincronizando ou aberto e não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="13e88-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="13e88-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-155">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-156">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="13e88-157">ILSCLocalSyncClient:: getChanges</span><span class="sxs-lookup"><span data-stu-id="13e88-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="13e88-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-158"></span></span>

<span data-ttu-id="13e88-159">GetChanges retorna um enumerador de objetos ILSCEvent e também retorna um token que é fornecido à próxima chamada a getChanges, supondo que o consumidor tenha processado o conjunto de eventos anterior.</span><span class="sxs-lookup"><span data-stu-id="13e88-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="13e88-160">Os eventos antes do _nPreviousChangesToken_ especificado serão excluídos e não estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="13e88-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="13e88-161">Se não houver eventos a serem processados, _pnCurrentChangesToken_ deverá ser o mesmo valor que _NPreviousChangesToken_, mas _ppiEvents_ ainda será definido.</span><span class="sxs-lookup"><span data-stu-id="13e88-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="13e88-162">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-162">Parameters</span></span>

 <span data-ttu-id="13e88-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="13e88-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="13e88-164">Identifica qual evento foi processado pela última vez pelo consumidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="13e88-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="13e88-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="13e88-166">Identifica o evento mais recente que está sendo entregue ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="13e88-167">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-167">Must not be null.</span></span>
  
 <span data-ttu-id="13e88-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="13e88-168">_ppiEvents_</span></span>
  
<span data-ttu-id="13e88-169">Um enumerador para os eventos enviados para o consumidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="13e88-170">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-171">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-171">Return values</span></span>

|<span data-ttu-id="13e88-172">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-172">Value</span></span>|<span data-ttu-id="13e88-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-175">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-177">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-179">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-180">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-181">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="13e88-182">ILSCLocalSyncClient:: GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="13e88-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="13e88-183">O GetClientNetworkSyncPermission é usado para consultar se a heurística de sincronização do Office para o uso de custos e energia de rede é substituída.</span><span class="sxs-lookup"><span data-stu-id="13e88-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="13e88-184">Quando em uma rede 3G ou de alto custo ou durante a execução da bateria em vez de serem conectadas, o Office pode optar por bloquear o tráfego de rede até um tempo mais Opportune.</span><span class="sxs-lookup"><span data-stu-id="13e88-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="13e88-185">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-185">Parameters</span></span>

 <span data-ttu-id="13e88-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="13e88-186">_nspType_</span></span>
  
<span data-ttu-id="13e88-187">Um sinalizador que define o custo heurístico a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="13e88-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="13e88-188">Consulte [enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="13e88-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="13e88-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="13e88-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="13e88-190">Especifica se o heurístico de custo solicitado está substituído ou não no momento.</span><span class="sxs-lookup"><span data-stu-id="13e88-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="13e88-191">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-192">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-192">Return values</span></span>

|<span data-ttu-id="13e88-193">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-193">Value</span></span>|<span data-ttu-id="13e88-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-196">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-198">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-200">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-201">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-202">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="13e88-203">ILSCLocalSyncClient:: GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="13e88-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="13e88-204">O GetFileStatus é usado para coletar informações de um arquivo específico: se ele existe no cache, se ele tem comunicação pendente com a cópia do servidor e se o Office 2013 tem os dados mais atualizados da cópia local.</span><span class="sxs-lookup"><span data-stu-id="13e88-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="13e88-205">Requer um sinalizador bit a bit de [Enumeração LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) valores para determinar quais informações o objeto com do CsiSyncClient deve consultar.</span><span class="sxs-lookup"><span data-stu-id="13e88-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="13e88-206">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-206">Parameters</span></span>

 <span data-ttu-id="13e88-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13e88-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="13e88-208">A cadeia de caracteres que identifica o arquivo no cliente.</span><span class="sxs-lookup"><span data-stu-id="13e88-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="13e88-209">Este valor deve ser não vazio, com no máximo 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="13e88-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="13e88-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="13e88-211">Um sinalizador que define as informações a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="13e88-211">A flag which defines what information to return.</span></span> <span data-ttu-id="13e88-212">Consulte [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="13e88-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="13e88-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="13e88-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="13e88-214">A cadeia de caracteres que identifica o local do arquivo identificado por _bstrResourceID_ no cliente.</span><span class="sxs-lookup"><span data-stu-id="13e88-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="13e88-215">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-215">Must not be null.</span></span> 
  
 <span data-ttu-id="13e88-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="13e88-216">_pbstrETag_</span></span>
  
<span data-ttu-id="13e88-217">Uma cadeia de caracteres que conterá a eTag para o arquivo identificado por _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="13e88-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="13e88-218">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-218">Must not be null.</span></span> 
  
 <span data-ttu-id="13e88-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="13e88-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="13e88-220">Um sinalizador que conterá o status solicitado via _sfRequestedStatus_ para o arquivo identificado por _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="13e88-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="13e88-221">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-221">Must not be null.</span></span> <span data-ttu-id="13e88-222">Consulte [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="13e88-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-223">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-223">Return values</span></span>

|<span data-ttu-id="13e88-224">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-224">Value</span></span>|<span data-ttu-id="13e88-225">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-227">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-229">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13e88-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13e88-231">As informações de arquivo especificadas por _bstrResourceID_ não existem no cache.</span><span class="sxs-lookup"><span data-stu-id="13e88-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="13e88-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="13e88-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="13e88-233">LSCStatusFlag_LocalFileUnchanged foi solicitado ou o arquivo especificado por _bstrResourceID_ está bloqueado ou ausente.</span><span class="sxs-lookup"><span data-stu-id="13e88-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="13e88-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-235">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-236">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-237">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="13e88-238">ILSCLocalSyncClient:: GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="13e88-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="13e88-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-239"></span></span>

<span data-ttu-id="13e88-240">GetSupportedFileExtensions retorna uma lista de extensões de arquivo delimitadas por pipe que atualmente têm suporte no objeto COM do CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="13e88-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="13e88-241">Observe que essa lista pode ser alterada, e o consumidor será notificado sobre uma alteração por meio do objeto IPartnerActivityCallback fornecido em [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (consulte EventOccured).</span><span class="sxs-lookup"><span data-stu-id="13e88-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="13e88-242">Um exemplo da cadeia de caracteres retornada é o seguinte: "| docx | docm | pptx |"</span><span class="sxs-lookup"><span data-stu-id="13e88-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="13e88-243">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-243">Parameters</span></span>

 <span data-ttu-id="13e88-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="13e88-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="13e88-245">Uma cadeia de caracteres a ser definida com um conjunto delimitado por pipe de extensões de arquivo suportadas pelo objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="13e88-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="13e88-246">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-247">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-247">Return values</span></span>

|<span data-ttu-id="13e88-248">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-248">Value</span></span>|<span data-ttu-id="13e88-249">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-251">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-253">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-255">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-256">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-257">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="13e88-258">ILSCLocalSyncClient:: Initialize</span><span class="sxs-lookup"><span data-stu-id="13e88-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="13e88-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-259"></span></span>

<span data-ttu-id="13e88-260">Initialize deve ser o primeiro método chamado.</span><span class="sxs-lookup"><span data-stu-id="13e88-260">Initialize must be the first method called.</span></span> <span data-ttu-id="13e88-261">Caso contrário, todas as outras APIs retornarão E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="13e88-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="13e88-262">Chamar Initialize em um objeto já inicializado retorna S_OK e não faz nada.</span><span class="sxs-lookup"><span data-stu-id="13e88-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="13e88-263">Se E_LSC_CACHEMISMATCH for retornado, o chamador poderá chamar [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para excluir o cache associado ao fornecido fornecido.</span><span class="sxs-lookup"><span data-stu-id="13e88-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="13e88-264">No enTanto, nesse caso, outras APIs ainda retornarão E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="13e88-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="13e88-265">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-265">Parameters</span></span>

 <span data-ttu-id="13e88-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="13e88-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="13e88-267">Identifica o consumidor e o cache a ser usado.</span><span class="sxs-lookup"><span data-stu-id="13e88-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="13e88-268">Deve ser não vazio com um máximo de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="13e88-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="13e88-269">_bstrProgID_</span></span>
  
<span data-ttu-id="13e88-270">Identifica o objeto COM do consumidor para comunicação bidirecional.</span><span class="sxs-lookup"><span data-stu-id="13e88-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="13e88-271">Deve ser não vazio com um máximo de 39 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="13e88-272">Confira [ \<a tecla ProgID\> ](https://docs.microsoft.com/windows/desktop/com/-progid--key) para obter mais informações sobre ProgIDs.</span><span class="sxs-lookup"><span data-stu-id="13e88-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="13e88-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="13e88-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="13e88-274">Identifica a raiz do diretório no qual os arquivos locais serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="13e88-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="13e88-275">Deve ser não vazio com um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="13e88-276">O diretório já deve existir.</span><span class="sxs-lookup"><span data-stu-id="13e88-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="13e88-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="13e88-277">_pEventCallback_</span></span>
  
<span data-ttu-id="13e88-278">A interface de retorno de chamada para a qual o CsiSyncClient irá notificar as alterações.</span><span class="sxs-lookup"><span data-stu-id="13e88-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="13e88-279">Consulte IPartnerActivityCallback:: EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="13e88-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="13e88-280">Esse valor não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="13e88-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="13e88-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="13e88-282">Retorna se um novo cache foi criado.</span><span class="sxs-lookup"><span data-stu-id="13e88-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="13e88-283">Se nenhum cache estiver associado ao fornecido, será criado um.</span><span class="sxs-lookup"><span data-stu-id="13e88-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="13e88-284">Esse valor não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13e88-285">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-285">Return values</span></span>

|<span data-ttu-id="13e88-286">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-286">Value</span></span>|<span data-ttu-id="13e88-287">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-289">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-291">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="13e88-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="13e88-293">Um fornecido já tem um cache associado a ele, mas tem um ProgId ou FileSystemDirectoryHint diferente dos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="13e88-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="13e88-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="13e88-295">O FileSystemDirectoryHint (ou uma subpasta) já existe em um cache diferente.</span><span class="sxs-lookup"><span data-stu-id="13e88-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="13e88-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="13e88-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="13e88-297">O ProgID já existe em um cache diferente.</span><span class="sxs-lookup"><span data-stu-id="13e88-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="13e88-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-298">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-299">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="13e88-300">ILSCLocalSyncClient:: LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="13e88-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="13e88-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-301"></span></span>

<span data-ttu-id="13e88-302">LocalFileChange é usado para dizer ao objeto COM do CsiSyncClient que tentará carregar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="13e88-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="13e88-303">O método irá preparar o arquivo para carregamento, incluindo a leitura do conteúdo atual do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="13e88-304">Se um upload já estiver pendente, o carregamento anterior será descartado e o novo conteúdo preparado para carregar.</span><span class="sxs-lookup"><span data-stu-id="13e88-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="13e88-305">Se o arquivo estiver aberto para edição em um aplicativo, esse método retornará S_OK sem preparar o arquivo para carregamento (o aplicativo já deve fazer essa etapa se houver alterações).</span><span class="sxs-lookup"><span data-stu-id="13e88-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="13e88-306">Este método permitirá carregamentos se ele tiver sido marcado como uploads bloqueados anteriormente (consulte [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)RenameFile).</span><span class="sxs-lookup"><span data-stu-id="13e88-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="13e88-307">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-307">Parameters</span></span>

 <span data-ttu-id="13e88-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="13e88-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="13e88-309">Uma cadeia de caracteres que identifica o arquivo no cliente.</span><span class="sxs-lookup"><span data-stu-id="13e88-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="13e88-310">Este valor deve ser um caminho local não vazio com um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="13e88-311">Este caminho deve estar na árvore de diretório especificada por FileSystemDirectoryHint quando a chamada para [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) foi feita.</span><span class="sxs-lookup"><span data-stu-id="13e88-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="13e88-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13e88-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="13e88-313">Uma cadeia de caracteres que identifica a reSourceid do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="13e88-314">Este valor deve ser não vazio com um máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="13e88-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="13e88-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="13e88-316">Uma cadeia de caracteres que identifica o arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="13e88-317">Esse valor deve ser não vazio, uma URL válida, mas não mais de INTERNET_MAX_URL_LENGTH, conforme definido por https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="13e88-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-318">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-318">Return values</span></span>

|<span data-ttu-id="13e88-319">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-319">Value</span></span>|<span data-ttu-id="13e88-320">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-322">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-324">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="13e88-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="13e88-326">O arquivo especificado por _bstrFileSystemPath_ tem um ResourceId diferente do especificado.</span><span class="sxs-lookup"><span data-stu-id="13e88-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="13e88-327">Um evento do tipo LSCEventType_OnFilePathConflict é enviado quando esse erro é retornado.</span><span class="sxs-lookup"><span data-stu-id="13e88-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="13e88-328">ConFira [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)GetChanges.</span><span class="sxs-lookup"><span data-stu-id="13e88-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="13e88-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13e88-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13e88-330">O arquivo foi excluído de operação intermediária.</span><span class="sxs-lookup"><span data-stu-id="13e88-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="13e88-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="13e88-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="13e88-332">A extensão de arquivo fornecida não é suportada pelo objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="13e88-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="13e88-333">Consulte [ILSCLocalSyncClient:: GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="13e88-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="13e88-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="13e88-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="13e88-335">O objeto COM não agendou um carregamento porque o arquivo no cache tinha as alterações mais recentes do disco.</span><span class="sxs-lookup"><span data-stu-id="13e88-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="13e88-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="13e88-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="13e88-337">O arquivo especificado por _bstrFileSystemPath_ está ausente ou bloqueado.</span><span class="sxs-lookup"><span data-stu-id="13e88-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="13e88-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="13e88-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="13e88-339">O FileSystemPath fornecido não está na raiz do diretório especificado pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita.</span><span class="sxs-lookup"><span data-stu-id="13e88-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="13e88-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-341">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="13e88-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="13e88-343">O arquivo especificado por _bstrResourceID_ tem um FileSystemPath diferente do especificado.</span><span class="sxs-lookup"><span data-stu-id="13e88-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="13e88-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="13e88-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="13e88-345">O arquivo especificado já tem alterações pendentes em um cache diferente e ainda não pode ser associado ao cache do consumidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="13e88-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="13e88-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="13e88-347">O webPath fornecido está em um cache diferente.</span><span class="sxs-lookup"><span data-stu-id="13e88-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="13e88-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-348">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-349">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="13e88-350">ILSCLocalSyncClient:: RenameFile</span><span class="sxs-lookup"><span data-stu-id="13e88-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="13e88-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-351"></span></span>

<span data-ttu-id="13e88-352">RenameFile associará uma nova URL e um caminho local para um determinado reSourceid.</span><span class="sxs-lookup"><span data-stu-id="13e88-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="13e88-353">Se o arquivo especificado pelo reSourceid ainda não existir no cache, uma tentativa será feita para criá-lo e marcá-lo para download.</span><span class="sxs-lookup"><span data-stu-id="13e88-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="13e88-354">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-354">Parameters</span></span>

 <span data-ttu-id="13e88-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13e88-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="13e88-356">Uma cadeia de caracteres que identifica a reSourceid do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="13e88-357">Este valor deve ser não vazio com um máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="13e88-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="13e88-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="13e88-359">Uma cadeia de caracteres que especifica o novo caminho local para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="13e88-360">Este valor deve ser um caminho local não vazio com um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="13e88-361">Esse caminho deve estar na árvore de diretório especificada pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita.</span><span class="sxs-lookup"><span data-stu-id="13e88-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="13e88-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="13e88-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="13e88-363">Uma cadeia de caracteres que especifica a nova URL para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="13e88-364">Esse valor deve ser uma URL válida não vazia, mas não mais do que INTERNET_MAX_URL_LENGTH, conforme definido https://support.microsoft.com/kb/208427por.</span><span class="sxs-lookup"><span data-stu-id="13e88-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="13e88-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="13e88-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="13e88-366">Especifica se os carregamentos no novo local são permitidos no momento.</span><span class="sxs-lookup"><span data-stu-id="13e88-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-367">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-367">Return values</span></span>

|<span data-ttu-id="13e88-368">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-368">Value</span></span>|<span data-ttu-id="13e88-369">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-371">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-373">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="13e88-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="13e88-375">O _bstrNewFileSystemPath_ ou o _bstrNewWebPath_ já existem em outro arquivo em qualquer cache.</span><span class="sxs-lookup"><span data-stu-id="13e88-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="13e88-376">Um evento do tipo LSCEventType_OnFilePathConflict é enviado quando esse erro é retornado.</span><span class="sxs-lookup"><span data-stu-id="13e88-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="13e88-377">ConFira [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)GetChanges.</span><span class="sxs-lookup"><span data-stu-id="13e88-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="13e88-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13e88-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13e88-379">As informações do arquivo foram excluídas do cache enquanto esse método estava em execução.</span><span class="sxs-lookup"><span data-stu-id="13e88-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="13e88-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="13e88-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="13e88-381">O FileSystemPath fornecido não está na raiz do diretório especificado pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita.</span><span class="sxs-lookup"><span data-stu-id="13e88-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="13e88-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-383">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="13e88-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="13e88-385">O arquivo especificado está atualmente sincronizando em um aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="13e88-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="13e88-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-386">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-387">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="13e88-388">ILSCLocalSyncClient:: ResetCache</span><span class="sxs-lookup"><span data-stu-id="13e88-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="13e88-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-389"></span></span>

<span data-ttu-id="13e88-390">O ResetCache excluirá o cache associado ao fornecido, fornecido na inicialização.</span><span class="sxs-lookup"><span data-stu-id="13e88-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="13e88-391">Isso inclui todas as informações do arquivo, mas deixará os arquivos no cliente e no servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="13e88-392">Esse método também deixa o objeto em um estado parcialmente não inicializado.</span><span class="sxs-lookup"><span data-stu-id="13e88-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="13e88-393">As únicas chamadas válidas depois disso são [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="13e88-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="13e88-394">Este método pode ser chamado se a inicialização falhar e retornar E_LSC_CACHEMISMATCH, e excluirá o cache associado ao fornecido que foi fornecido com a chamada com falha.</span><span class="sxs-lookup"><span data-stu-id="13e88-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="13e88-395">Parameters</span><span class="sxs-lookup"><span data-stu-id="13e88-395">Parameters</span></span>

<span data-ttu-id="13e88-396">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="13e88-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13e88-397">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-397">Return values</span></span>

|<span data-ttu-id="13e88-398">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-398">Value</span></span>|<span data-ttu-id="13e88-399">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-401">Ocorreu uma falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13e88-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13e88-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-403">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-404">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-405">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="13e88-406">ILSCLocalSyncClient:: ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="13e88-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="13e88-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-407"></span></span>

<span data-ttu-id="13e88-408">ServerFileChange informa ao objeto COM do CsiSyncClient para marcar o arquivo especificado para download.</span><span class="sxs-lookup"><span data-stu-id="13e88-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="13e88-409">Se o arquivo estiver aberto em um aplicativo do Office para edição, este método retornará S_OK sem marcar o arquivo para download (o aplicativo já deve fazer essa etapa se houver alterações).</span><span class="sxs-lookup"><span data-stu-id="13e88-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="13e88-410">Este método permitirá downloads se ele foi marcado como downloads bloqueados anteriormente (consulte RenameFile).</span><span class="sxs-lookup"><span data-stu-id="13e88-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="13e88-411">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-411">Parameters</span></span>

|<span data-ttu-id="13e88-412">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="13e88-412">Parameter</span></span>|<span data-ttu-id="13e88-413">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="13e88-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="13e88-415">Uma cadeia de caracteres que identifica o arquivo no cliente.</span><span class="sxs-lookup"><span data-stu-id="13e88-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="13e88-416">Este valor deve ser um caminho local não vazio com um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="13e88-417">Esse caminho deve estar na árvore de diretório especificada pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita.</span><span class="sxs-lookup"><span data-stu-id="13e88-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="13e88-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="13e88-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="13e88-419">Uma cadeia de caracteres que identifica a reSourceid do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="13e88-420">Este valor deve ser não vazio com um máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13e88-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="13e88-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="13e88-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="13e88-422">Uma cadeia de caracteres que identifica o arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="13e88-423">Este valor deve ser uma URL válida não vazia, mas não mais de INTERNET_MAX_URL_LENGTH, conforme definido por https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="13e88-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="13e88-424">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-424">Return values</span></span>

|<span data-ttu-id="13e88-425">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-425">Value</span></span>|<span data-ttu-id="13e88-426">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-428">Falha ao definir o estado de conectividade do cache.</span><span class="sxs-lookup"><span data-stu-id="13e88-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="13e88-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="13e88-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="13e88-430">O arquivo especificado por _bstrFileSystemPath_ tem um ResourceId diferente do especificado.</span><span class="sxs-lookup"><span data-stu-id="13e88-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="13e88-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="13e88-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="13e88-432">A extensão de arquivo fornecida não é suportada pelo objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="13e88-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="13e88-433">Consulte GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="13e88-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="13e88-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13e88-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13e88-435">O arquivo foi excluído em meados da operação.</span><span class="sxs-lookup"><span data-stu-id="13e88-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="13e88-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-437">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="13e88-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="13e88-439">O FileSystemPath fornecido não está na raiz do diretório especificado pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita.</span><span class="sxs-lookup"><span data-stu-id="13e88-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="13e88-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-441">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="13e88-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="13e88-443">O arquivo especificado por _bstrResourceID_ tem um FileSystemPath diferente do especificado.</span><span class="sxs-lookup"><span data-stu-id="13e88-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="13e88-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="13e88-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="13e88-445">O arquivo especificado já tem alterações pendentes em um cache diferente e ainda não pode ser associado ao cache do consumidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="13e88-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="13e88-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="13e88-447">O webPath fornecido está em um cache diferente.</span><span class="sxs-lookup"><span data-stu-id="13e88-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="13e88-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-448">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-449">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="13e88-450">ILSCLocalSyncClient:: SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="13e88-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="13e88-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-451"></span></span>

<span data-ttu-id="13e88-452">Define o cache em um estado online ou offline.</span><span class="sxs-lookup"><span data-stu-id="13e88-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="13e88-453">Se estiver offline, o Office não tentará se comunicar com o servidor para nenhum arquivo desse cache, independentemente da configuração _fBlockUploads_ de cada arquivo individual.</span><span class="sxs-lookup"><span data-stu-id="13e88-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="13e88-454">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-454">Parameters</span></span>

 <span data-ttu-id="13e88-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="13e88-455">_fIsOnline_</span></span>
  
<span data-ttu-id="13e88-456">Um booliano que determina o estado de conectividade do cache.</span><span class="sxs-lookup"><span data-stu-id="13e88-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-457">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-457">Return values</span></span>

|<span data-ttu-id="13e88-458">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-458">Value</span></span>|<span data-ttu-id="13e88-459">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-461">Falha ao definir o estado de conectividade do cache.</span><span class="sxs-lookup"><span data-stu-id="13e88-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="13e88-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-463">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-465">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-466">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-467">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="13e88-468">ILSCLocalSyncClient:: SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="13e88-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="13e88-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-469"></span></span>

<span data-ttu-id="13e88-470">SetClientNetworkSyncPermission é usado para substituir ou restoreOffice a heurística de sincronização para o custo de rede e o uso de energia.</span><span class="sxs-lookup"><span data-stu-id="13e88-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="13e88-471">Quando em uma rede 3G ou de alto custo ou durante a execução da bateria em vez de serem conectadas, o Office pode optar por bloquear o tráfego de rede até um tempo mais Opportune.</span><span class="sxs-lookup"><span data-stu-id="13e88-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="13e88-472">O consumidor dessa API pode usá-la para substituir a heurística do Office e forçar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="13e88-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="13e88-473">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-473">Parameters</span></span>

 <span data-ttu-id="13e88-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="13e88-474">_nspType_</span></span>
  
<span data-ttu-id="13e88-475">Um sinalizador que define qual heurística de custo será substituída.</span><span class="sxs-lookup"><span data-stu-id="13e88-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="13e88-476">Consulte [enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="13e88-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="13e88-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="13e88-477">_fEnableSync_</span></span>
  
<span data-ttu-id="13e88-478">Especifica se a sincronização deve ser forçada, substituindo o custo heurístico ou não mais a substituir.</span><span class="sxs-lookup"><span data-stu-id="13e88-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-479">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-479">Return values</span></span>

|<span data-ttu-id="13e88-480">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-480">Value</span></span>|<span data-ttu-id="13e88-481">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-483">Falha ao substituir a heurística de sincronização.</span><span class="sxs-lookup"><span data-stu-id="13e88-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="13e88-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-485">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-486">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-487">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="13e88-488">ILSCLocalSyncClient:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="13e88-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="13e88-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-489"></span></span>

<span data-ttu-id="13e88-490">Descarrega o cache do objeto COM e realiza operações de fechamento.</span><span class="sxs-lookup"><span data-stu-id="13e88-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="13e88-491">[ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DEVE ser chamado antes de destruir o objeto COM.</span><span class="sxs-lookup"><span data-stu-id="13e88-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="13e88-492">Uma vez chamado, nenhuma outra API pode ser chamada, o objeto COM deve ser destruído e um novo criado se você quiser continuar as operações.</span><span class="sxs-lookup"><span data-stu-id="13e88-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="13e88-493">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-493">Parameters</span></span>

<span data-ttu-id="13e88-494">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="13e88-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13e88-495">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-495">Return values</span></span>

|<span data-ttu-id="13e88-496">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-496">Value</span></span>|<span data-ttu-id="13e88-497">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-499">Falha ao cancelar a inicialização.</span><span class="sxs-lookup"><span data-stu-id="13e88-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="13e88-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13e88-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="13e88-501">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13e88-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13e88-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-502">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-503">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="13e88-504">Interface IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="13e88-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="13e88-505">Esta interface representa uma lista de eventos ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="13e88-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="13e88-506">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13e88-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="13e88-507">IEnumLSCEvent:: FNext</span><span class="sxs-lookup"><span data-stu-id="13e88-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="13e88-508">Recupera o próximo evento da lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="13e88-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="13e88-509">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-509">Parameters</span></span>

 <span data-ttu-id="13e88-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="13e88-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="13e88-511">Um ponteiro para uma interface ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="13e88-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13e88-512">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-512">Return values</span></span>

|<span data-ttu-id="13e88-513">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-513">Value</span></span>|<span data-ttu-id="13e88-514">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-516">Não há mais eventos.</span><span class="sxs-lookup"><span data-stu-id="13e88-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="13e88-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-517">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-518">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="13e88-519">IEnumLSCEvent:: Reset</span><span class="sxs-lookup"><span data-stu-id="13e88-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="13e88-520">Redefine o enumerador para o primeiro evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="13e88-521">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-521">Parameters</span></span>

<span data-ttu-id="13e88-522">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="13e88-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13e88-523">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-523">Return values</span></span>

<span data-ttu-id="13e88-524">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13e88-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="13e88-525">Interface ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="13e88-525">Interface ILSCEvent</span></span>

<span data-ttu-id="13e88-526">Esta interface representa um evento de sincronização.</span><span class="sxs-lookup"><span data-stu-id="13e88-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="13e88-527">Todas as informações sobre o evento podem ser recuperadas da interface.</span><span class="sxs-lookup"><span data-stu-id="13e88-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="13e88-528">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13e88-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="13e88-529">ILSCEvent:: GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="13e88-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="13e88-530">Observe que esse valor é preenchido quando [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) GetChanges é chamado, não quando o evento foi criado, de modo que você só terá o status atual do arquivo, e não o status do arquivo quando o status de conflito for alterado.</span><span class="sxs-lookup"><span data-stu-id="13e88-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="13e88-531">Esse valor será preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento for LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="13e88-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="13e88-532">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-532">Parameters</span></span>

 <span data-ttu-id="13e88-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="13e88-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="13e88-534">O status atual de conflito do arquivo associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13e88-535">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-535">Return values</span></span>

<span data-ttu-id="13e88-536">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13e88-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="13e88-537">ILSCEvent:: GetError</span><span class="sxs-lookup"><span data-stu-id="13e88-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="13e88-538">Esse valor é preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="13e88-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="13e88-539">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-539">Parameters</span></span>

 <span data-ttu-id="13e88-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="13e88-540">_pnError_</span></span>
  
<span data-ttu-id="13e88-541">O erro associado a este evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13e88-542">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-542">Return values</span></span>

<span data-ttu-id="13e88-543">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13e88-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="13e88-544">ILSCEvent:: getETag</span><span class="sxs-lookup"><span data-stu-id="13e88-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="13e88-545">Esse valor é preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="13e88-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="13e88-546">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-546">Parameters</span></span>

 <span data-ttu-id="13e88-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="13e88-547">_pbstrETag_</span></span>
  
<span data-ttu-id="13e88-548">A ETag associada a este evento</span><span class="sxs-lookup"><span data-stu-id="13e88-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13e88-549">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-549">Return values</span></span>

<span data-ttu-id="13e88-550">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13e88-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="13e88-551">ILSCEvent:: getEventtype</span><span class="sxs-lookup"><span data-stu-id="13e88-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="13e88-552">Obtém o tipo deste evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="13e88-553">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-553">Parameters</span></span>

 <span data-ttu-id="13e88-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="13e88-554">_pnEventType_</span></span>
  
<span data-ttu-id="13e88-555">O tipo de evento desse evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-555">The event type of this event.</span></span> <span data-ttu-id="13e88-556">ConFira [enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para valores válidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="13e88-557">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-558">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-558">Return values</span></span>

|<span data-ttu-id="13e88-559">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-559">Value</span></span>|<span data-ttu-id="13e88-560">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-562">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-563">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-564">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="13e88-565">ILSCEvent:: GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="13e88-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="13e88-566">Obtém o caminho de trabalho local para esse evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="13e88-567">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-567">Parameters</span></span>

 <span data-ttu-id="13e88-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="13e88-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="13e88-569">O caminho local do arquivo ao qual esse evento pertence.</span><span class="sxs-lookup"><span data-stu-id="13e88-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-570">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-570">Return values</span></span>

<span data-ttu-id="13e88-571">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13e88-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="13e88-572">ILSCEvent:: getResourceid</span><span class="sxs-lookup"><span data-stu-id="13e88-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="13e88-573">Obtém a ID de recurso para o evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="13e88-574">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-574">Parameters</span></span>

 <span data-ttu-id="13e88-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13e88-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="13e88-576">O reSourceid do arquivo associado a esse evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13e88-577">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-577">Return values</span></span>

<span data-ttu-id="13e88-578">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13e88-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="13e88-579">ILSCEvent:: GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="13e88-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="13e88-580">Esse valor será preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento for LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="13e88-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="13e88-581">Quando uma chamada para [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) renameFile causar um conflito de caminho local ou caminho da Web com outro arquivo no cache de arquivos do Office, essa evento é gerado.</span><span class="sxs-lookup"><span data-stu-id="13e88-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="13e88-582">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-582">Parameters</span></span>

 <span data-ttu-id="13e88-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="13e88-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="13e88-584">O reSourceid que provocou esse evento para ser gerado.</span><span class="sxs-lookup"><span data-stu-id="13e88-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="13e88-585">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-586">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-586">Return values</span></span>

<span data-ttu-id="13e88-587">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13e88-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="13e88-588">ILSCEvent:: GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="13e88-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="13e88-589">Esse valor é preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="13e88-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="13e88-590">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-590">Parameters</span></span>

 <span data-ttu-id="13e88-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="13e88-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="13e88-592">O tipo de erro associado a esse evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-592">The error type associated with this event.</span></span> <span data-ttu-id="13e88-593">Consulte [enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="13e88-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="13e88-594">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-595">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-595">Return values</span></span>

|<span data-ttu-id="13e88-596">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-596">Value</span></span>|<span data-ttu-id="13e88-597">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-599">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-600">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-601">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="13e88-602">ILSCEvent:: GetWebPath</span><span class="sxs-lookup"><span data-stu-id="13e88-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="13e88-603">Esse valor será preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento for LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="13e88-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="13e88-604">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-604">Parameters</span></span>

 <span data-ttu-id="13e88-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="13e88-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="13e88-606">Especifica o caminho da Web associado a esse evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="13e88-607">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-608">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-608">Return values</span></span>

<span data-ttu-id="13e88-609">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13e88-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="13e88-610">Interface ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="13e88-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="13e88-611">Esta interface contém informações adicionais sobre um evento de sincronização.</span><span class="sxs-lookup"><span data-stu-id="13e88-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="13e88-612">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13e88-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="13e88-613">ILSCEvent2:: GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="13e88-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="13e88-614">Obtém as informações da cadeia de erros sobre um evento de sincronização.</span><span class="sxs-lookup"><span data-stu-id="13e88-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="13e88-615">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-615">Parameters</span></span>

 <span data-ttu-id="13e88-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="13e88-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="13e88-617">Uma cadeia de caracteres para armazenar as informações da cadeia de erros.</span><span class="sxs-lookup"><span data-stu-id="13e88-617">A string to hold the error chain information.</span></span> <span data-ttu-id="13e88-618">Não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="13e88-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-619">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-619">Return values</span></span>

|<span data-ttu-id="13e88-620">Valor</span><span class="sxs-lookup"><span data-stu-id="13e88-620">Value</span></span>|<span data-ttu-id="13e88-621">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="13e88-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="13e88-623">A versão instalada do Office não tem suporte para essa interface</span><span class="sxs-lookup"><span data-stu-id="13e88-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="13e88-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13e88-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13e88-625">Um ou mais dos valores de parâmetro são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="13e88-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13e88-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="13e88-627">As informações da cadeia de erros não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="13e88-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="13e88-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e88-628">S_OK</span></span>  <br/> |<span data-ttu-id="13e88-629">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13e88-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="13e88-630">Interface IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="13e88-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="13e88-631">Esta interface fornece uma função de retorno de chamada para o objeto COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="13e88-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="13e88-632">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13e88-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="13e88-633">IPartnerActivityCallback:: EventOccurred</span><span class="sxs-lookup"><span data-stu-id="13e88-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="13e88-634">Esta é uma função de retorno de chamada no objeto fornecido ao objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="13e88-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="13e88-635">É esperado que, quando ocorrer um evento (consulte [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos de eventos válidos), o objeto com do CsiSyncClient chamará esse método, sinalizando o consumidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="13e88-636">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e88-636">Parameters</span></span>

 <span data-ttu-id="13e88-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="13e88-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="13e88-638">O tipo de evento desse evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-638">The event type of this event.</span></span> <span data-ttu-id="13e88-639">ConFira [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para valores válidos.</span><span class="sxs-lookup"><span data-stu-id="13e88-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13e88-640">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13e88-640">Return values</span></span>

<span data-ttu-id="13e88-641">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13e88-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="13e88-642">Enumerações</span><span class="sxs-lookup"><span data-stu-id="13e88-642">Enumerations</span></span>

<span data-ttu-id="13e88-643">O CSISyncClient usa as seguintes enumerações.</span><span class="sxs-lookup"><span data-stu-id="13e88-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="13e88-644">Enumerar LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="13e88-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="13e88-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-645"></span></span>

<span data-ttu-id="13e88-646">Essa enumeração Especifica as categorias de erros que podem ocorrer durante a sincronização de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="13e88-647">Enumera</span><span class="sxs-lookup"><span data-stu-id="13e88-647">Enumerator</span></span>|<span data-ttu-id="13e88-648">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="13e88-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="13e88-650">O erro de sincronização desse evento foi inesperado e pode exigir consideração especial.</span><span class="sxs-lookup"><span data-stu-id="13e88-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="13e88-651">Por padrão, o usuário pode ter que intervir.</span><span class="sxs-lookup"><span data-stu-id="13e88-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="13e88-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="13e88-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="13e88-653">O erro de sincronização desse evento não precisa de consideração especial.</span><span class="sxs-lookup"><span data-stu-id="13e88-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="13e88-654">O Office vai tratá-lo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="13e88-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="13e88-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="13e88-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="13e88-656">O erro de sincronização desse evento requer um usuário para resolvê-lo.</span><span class="sxs-lookup"><span data-stu-id="13e88-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="13e88-657">Por exemplo, o erro de conflito de mesclagem exige que um usuário abra o documento e mescle-o.</span><span class="sxs-lookup"><span data-stu-id="13e88-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="13e88-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="13e88-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="13e88-659">O erro de sincronização desse evento exige que o consumidor intervenha, mas não deve exigir consideração especial pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="13e88-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="13e88-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="13e88-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="13e88-661">O erro de sincronização desse evento exige que o consumidor fique interinterveniente como um caso especial.</span><span class="sxs-lookup"><span data-stu-id="13e88-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="13e88-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="13e88-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="13e88-663">Enumerar LSCEventType</span><span class="sxs-lookup"><span data-stu-id="13e88-663">Enum LSCEventType</span></span>
<span data-ttu-id="13e88-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-664"></span></span>

<span data-ttu-id="13e88-665">Essa enumeração Especifica o tipo de eventos que podem ocorrer para um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="13e88-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="13e88-666">Enumera</span><span class="sxs-lookup"><span data-stu-id="13e88-666">Enumerator</span></span>|<span data-ttu-id="13e88-667">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="13e88-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="13e88-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="13e88-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="13e88-670">Foram feitas alterações em um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="13e88-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="13e88-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="13e88-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="13e88-672">Um usuário abriu um arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="13e88-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="13e88-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="13e88-674">Concluído o download de alterações de arquivo do servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="13e88-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="13e88-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="13e88-676">Concluído o carregamento de alterações de arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="13e88-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="13e88-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="13e88-678">O estado de conflito de mesclagem de um arquivo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="13e88-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="13e88-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="13e88-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="13e88-680">Um arquivo foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="13e88-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="13e88-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="13e88-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="13e88-682">Um arquivo foi excluído.</span><span class="sxs-lookup"><span data-stu-id="13e88-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="13e88-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="13e88-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="13e88-684">A sincronização foi habilitada para os arquivos de um usuário.</span><span class="sxs-lookup"><span data-stu-id="13e88-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="13e88-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="13e88-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="13e88-686">Iniciado o download de alterações de arquivo do servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="13e88-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="13e88-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="13e88-688">Iniciado o carregamento de alterações de arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="13e88-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="13e88-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="13e88-690">Esse evento é gerado quando uma chamada para [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) RenameFile causa um conflito de caminho local ou caminho da Web com outro arquivo no Cache de arquivos do Office.</span><span class="sxs-lookup"><span data-stu-id="13e88-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="13e88-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="13e88-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="13e88-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="13e88-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="13e88-693">Enumerar LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="13e88-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="13e88-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-694"></span></span>

<span data-ttu-id="13e88-695">Essa enumeração Especifica o tipo de eventos que podem ocorrer.</span><span class="sxs-lookup"><span data-stu-id="13e88-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="13e88-696">O consumidor precisa chamar funções específicas do ILSCLocalSyncClient com base no tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="13e88-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="13e88-697">Enumera</span><span class="sxs-lookup"><span data-stu-id="13e88-697">Enumerator</span></span>|<span data-ttu-id="13e88-698">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="13e88-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="13e88-700">Ocorreu um ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="13e88-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="13e88-701">O consumidor deve chamar [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) GetChanges para recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="13e88-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="13e88-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="13e88-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="13e88-703">As extensões de arquivo com suporte foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="13e88-703">The supported file extensions have changed.</span></span> <span data-ttu-id="13e88-704">O consumidor deve chamar [ILSCLocalSyncClient:: GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar a nova lista de extensões com suporte.</span><span class="sxs-lookup"><span data-stu-id="13e88-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="13e88-705">Enumerar LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="13e88-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="13e88-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-706"></span></span>

<span data-ttu-id="13e88-707">Essa enumeração Especifica os sinalizadores usados para um heurístico de custo de rede.</span><span class="sxs-lookup"><span data-stu-id="13e88-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="13e88-708">Enumera</span><span class="sxs-lookup"><span data-stu-id="13e88-708">Enumerator</span></span>|<span data-ttu-id="13e88-709">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="13e88-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="13e88-711">True se o custo heurístico para redes caras (como 3G) é substituído.</span><span class="sxs-lookup"><span data-stu-id="13e88-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="13e88-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="13e88-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="13e88-713">True se o custo heurístico para uso de energia (como uma bateria) é substituído.</span><span class="sxs-lookup"><span data-stu-id="13e88-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="13e88-714">Enumerar LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="13e88-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="13e88-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="13e88-715"></span></span>

<span data-ttu-id="13e88-716">Essa enumeração é usada para representar o status de sincronização de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="13e88-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="13e88-717">Enumera</span><span class="sxs-lookup"><span data-stu-id="13e88-717">Enumerator</span></span>|<span data-ttu-id="13e88-718">Descrição</span><span class="sxs-lookup"><span data-stu-id="13e88-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13e88-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="13e88-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="13e88-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="13e88-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="13e88-721">True se houver dados pendentes para enviar ao arquivo de servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="13e88-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="13e88-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="13e88-723">True se houver dados pendentes para baixar do arquivo de servidor.</span><span class="sxs-lookup"><span data-stu-id="13e88-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="13e88-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="13e88-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="13e88-725">True se os dados que o Office tem no arquivo em seu cache é a cópia mais recente dos dados no disco.</span><span class="sxs-lookup"><span data-stu-id="13e88-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

