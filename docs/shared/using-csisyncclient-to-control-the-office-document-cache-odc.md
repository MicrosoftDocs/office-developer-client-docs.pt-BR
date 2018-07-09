---
title: Usando CSISyncClient para controlar o Cache de documentos do Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Aprenda a usar CSISyncClient para controlar o Cache de documentos do Office (ODC).
ms.openlocfilehash: adaa56bf040889bd8220506bcfab8fdb0b7ab6c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771224"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="13cb4-103">Usando CSISyncClient para controlar o Cache de documentos do Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="13cb4-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="13cb4-104">Aprenda a usar CSISyncClient para controlar o Cache de documentos do Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="13cb4-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="13cb4-105">CSISyncClient é um servidor COM limite de proc (CsiSyncClient.exe) que permite que o Microsoft OneDrive controlar o comportamento do Cache de documentos do Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="13cb4-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="13cb4-106">Por exemplo, o OneDrive pode chamar após o ODC via CSISyncClient para carregar e baixar arquivos de e para os pontos de extremidade do MS-FSSHTTP habilitado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="13cb4-107">Isso permite que o serviço reserva recursos avançados no Office, como transições de coautoria e contínuo de offline para online.</span><span class="sxs-lookup"><span data-stu-id="13cb4-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="13cb4-108">CsiSyncClient está disponível na área de trabalho do Office (x86 e x64).</span><span class="sxs-lookup"><span data-stu-id="13cb4-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="13cb4-109">Observação: Embora versões mais recentes do Office podem ser enviados com CsiSyncClient, o processo será usado apenas para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="13cb4-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="13cb4-110">A interface de CsiSyncClient e a metodologia de controlar o ODC serão alterado em futuras versões do Office.</span><span class="sxs-lookup"><span data-stu-id="13cb4-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="13cb4-111">A ID de classe está atualmente definida responda apenas a OneDrive.</span><span class="sxs-lookup"><span data-stu-id="13cb4-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="13cb4-112">O objeto COM pode ser usado como um servidor de COM limite de proc e executa no CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="13cb4-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="13cb4-113">Devido às limitações com acesso (que o ODC usa), ele é fornecido com o tipo de bit Office apresentarem, caso x64 Office significa uma x64 x86 ou objeto COM Office significa um x86 objeto COM.</span><span class="sxs-lookup"><span data-stu-id="13cb4-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="13cb4-114">Para contornar esta limitação, especificando CLSCTX_LOCAL_SERVER como parte do CoCreateInstance terão o objeto COM sejam hospedados como um servidor fora do proc COM, permitindo cross-bitness compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="13cb4-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="13cb4-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="13cb4-115">Interfaces</span></span>

<span data-ttu-id="13cb4-116">CSISyncClient usa as seguintes interfaces.</span><span class="sxs-lookup"><span data-stu-id="13cb4-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="13cb4-117">Interface ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="13cb4-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="13cb4-118">Esta é a interface principal usado para sincronizar arquivos no Office.</span><span class="sxs-lookup"><span data-stu-id="13cb4-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="13cb4-119">ProgID: Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="13cb4-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="13cb4-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="13cb4-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="13cb4-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="13cb4-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="13cb4-122">O objeto COM que é exposto é usado como um servidor fora do processo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="13cb4-123">Especificando CLSCTX_LOCAL_SERVER como parte do CoCreateInstance permite a compatibilidade entre os processos de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="13cb4-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="13cb4-124">Depois que você criou o objeto COM co, você deve chamar [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) primeiro.</span><span class="sxs-lookup"><span data-stu-id="13cb4-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="13cb4-125">Depois de [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) foi concluída com êxito, você pode chamar qualquer API sempre que desejar e em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="13cb4-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="13cb4-126">Você também pode chamar [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) em um objeto já inicializado, mas isso não faz nada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="13cb4-127">As exceções para o parágrafo anterior são [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) e [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="13cb4-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="13cb4-128">Depois de chamar [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) no objeto COM, você deve destruir esse objeto e crie um novo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="13cb4-129">[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) irá excluir sua subcache, excluir todas as informações do arquivo associado no cache, mas deixar os documentos no disco.</span><span class="sxs-lookup"><span data-stu-id="13cb4-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="13cb4-130">Ele também deixa intacta para se comunicar com o cache o estado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="13cb4-131">Isso permite que você chamar [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) novamente para criar um novo cache sem precisar destrua e recriar o objeto COM.</span><span class="sxs-lookup"><span data-stu-id="13cb4-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="13cb4-132">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13cb4-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="13cb4-133">ILSCLocalSyncClient::DeleteFile</span><span class="sxs-lookup"><span data-stu-id="13cb4-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="13cb4-134">DeleteFile é usado para remover as informações do arquivo do cache.</span><span class="sxs-lookup"><span data-stu-id="13cb4-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="13cb4-135">No entanto, esse método deixará o arquivo associado no disco e no servidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-136">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-136">Parameters</span></span>

 <span data-ttu-id="13cb4-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13cb4-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="13cb4-138">A cadeia de caracteres que identifica o ResourceID do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="13cb4-139">Este valor deve ser não vazias com um máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-140">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-140">Return values</span></span>

|<span data-ttu-id="13cb4-141">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-141">Value</span></span>|<span data-ttu-id="13cb4-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-144">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-146">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-148">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13cb4-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13cb4-150">O ResourceID determinado não está no cache.</span><span class="sxs-lookup"><span data-stu-id="13cb4-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="13cb4-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-152">Initialize não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="13cb4-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="13cb4-154">O arquivo está sendo sincronizado ou abra e não podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="13cb4-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="13cb4-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-155">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-156">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="13cb4-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="13cb4-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="13cb4-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-158"></span></span>

<span data-ttu-id="13cb4-159">GetChanges retorna um enumerador de objetos ILSCEvent e também retornará um token que é fornecido para a próxima chamada ao GetChanges, supondo que o consumidor tiver processado o conjunto de eventos anterior.</span><span class="sxs-lookup"><span data-stu-id="13cb4-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="13cb4-160">Eventos antes do _nPreviousChangesToken_ especificado serão excluídos e indisponível.</span><span class="sxs-lookup"><span data-stu-id="13cb4-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="13cb4-161">Se não houver nenhum evento a serem processados, _pnCurrentChangesToken_ deve ser o mesmo valor que _nPreviousChangesToken_, mas _ppiEvents_ ainda será definido.</span><span class="sxs-lookup"><span data-stu-id="13cb4-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-162">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-162">Parameters</span></span>

 <span data-ttu-id="13cb4-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="13cb4-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="13cb4-164">Identifica qual evento última foi processado pelo consumidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="13cb4-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="13cb4-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="13cb4-166">Identifica o evento mais recente que está sendo entregue ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="13cb4-167">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-167">Must not be null.</span></span>
  
 <span data-ttu-id="13cb4-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="13cb4-168">_ppiEvents_</span></span>
  
<span data-ttu-id="13cb4-169">Um enumerador para os eventos entregues ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="13cb4-170">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-171">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-171">Return values</span></span>

|<span data-ttu-id="13cb4-172">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-172">Value</span></span>|<span data-ttu-id="13cb4-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-175">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-177">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-179">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-180">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-181">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="13cb4-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="13cb4-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="13cb4-183">GetClientNetworkSyncPermission é usado para consultar se heurística de sincronização do Office de custo de rede e o uso de energia são substituídas.</span><span class="sxs-lookup"><span data-stu-id="13cb4-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="13cb4-184">Quando em um 3G ou outra rede de alto custo, ou quando executando em bateria versus sendo conectado, o Office pode optar por bloquear o tráfego de rede até um momento mais oportunidade.</span><span class="sxs-lookup"><span data-stu-id="13cb4-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-185">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-185">Parameters</span></span>

 <span data-ttu-id="13cb4-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="13cb4-186">_nspType_</span></span>
  
<span data-ttu-id="13cb4-187">Um sinalizador que define qual heurístico custo à consulta.</span><span class="sxs-lookup"><span data-stu-id="13cb4-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="13cb4-188">Consulte [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="13cb4-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="13cb4-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="13cb4-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="13cb4-190">Especifica se o heurístico custo solicitada no momento é substituído ou não.</span><span class="sxs-lookup"><span data-stu-id="13cb4-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="13cb4-191">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-192">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-192">Return values</span></span>

|<span data-ttu-id="13cb4-193">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-193">Value</span></span>|<span data-ttu-id="13cb4-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-196">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-198">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-200">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-201">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-202">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="13cb4-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="13cb4-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="13cb4-204">GetFileStatus é usado para coletar informações para um arquivo específico: se ela existir no cache, se ele tiver pendentes comunicação com a cópia do servidor e se o Office 2013 tem o máximo até dados de data a partir da cópia local.</span><span class="sxs-lookup"><span data-stu-id="13cb4-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="13cb4-205">Requer um sinalizador de bit a bit dos valores de [Enumeração LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) para determinar quais informações é o objeto COM CsiSyncClient consultar.</span><span class="sxs-lookup"><span data-stu-id="13cb4-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-206">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-206">Parameters</span></span>

 <span data-ttu-id="13cb4-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13cb4-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="13cb4-208">A cadeia de caracteres que identifica o arquivo no cliente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="13cb4-209">Este valor deve ser não vazias, com um máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="13cb4-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="13cb4-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="13cb4-211">Um sinalizador que define quais informações a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="13cb4-211">A flag which defines what information to return.</span></span> <span data-ttu-id="13cb4-212">Consulte [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="13cb4-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="13cb4-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="13cb4-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="13cb4-214">A cadeia de caracteres que identifica a localização do arquivo identificado por _bstrResourceID_ no cliente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="13cb4-215">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-215">Must not be null.</span></span> 
  
 <span data-ttu-id="13cb4-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="13cb4-216">_pbstrETag_</span></span>
  
<span data-ttu-id="13cb4-217">Uma cadeia de caracteres que conterá a eTag do arquivo identificado por _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="13cb4-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="13cb4-218">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-218">Must not be null.</span></span> 
  
 <span data-ttu-id="13cb4-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="13cb4-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="13cb4-220">Um sinalizador que conterá o status solicitado por meio de _sfRequestedStatus_ para o arquivo identificado por _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="13cb4-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="13cb4-221">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-221">Must not be null.</span></span> <span data-ttu-id="13cb4-222">Consulte [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="13cb4-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-223">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-223">Return values</span></span>

|<span data-ttu-id="13cb4-224">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-224">Value</span></span>|<span data-ttu-id="13cb4-225">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-227">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-229">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13cb4-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13cb4-231">As informações do arquivo especificadas por _bstrResourceID_ não existem no cache.</span><span class="sxs-lookup"><span data-stu-id="13cb4-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="13cb4-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="13cb4-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="13cb4-233">LSCStatusFlag_LocalFileUnchanged foi solicitado ou o arquivo especificado por _bstrResourceID_ está bloqueado ou ausente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="13cb4-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-235">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-236">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-237">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="13cb4-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="13cb4-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="13cb4-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-239"></span></span>

<span data-ttu-id="13cb4-240">GetSupportedFileExtensions retorna uma lista delimitada de extensões de arquivo que são suportados atualmente pelo objeto CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="13cb4-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="13cb4-241">Observe que esta lista pode mudar e do consumidor serão notificado sobre uma alteração através do objeto IPartnerActivityCallback fornecida no [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (consulte EventOccured).</span><span class="sxs-lookup"><span data-stu-id="13cb4-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="13cb4-242">Um exemplo da cadeia de caracteres retornada é o seguinte: "| docx | docm | pptx |"</span><span class="sxs-lookup"><span data-stu-id="13cb4-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-243">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-243">Parameters</span></span>

 <span data-ttu-id="13cb4-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="13cb4-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="13cb4-245">Uma cadeia de caracteres a ser definido com um conjunto delimitada das extensões de arquivo compatíveis com o objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="13cb4-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="13cb4-246">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-247">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-247">Return values</span></span>

|<span data-ttu-id="13cb4-248">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-248">Value</span></span>|<span data-ttu-id="13cb4-249">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-251">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-253">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-255">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-256">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-257">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="13cb4-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="13cb4-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="13cb4-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-259"></span></span>

<span data-ttu-id="13cb4-260">Initialize deve ser o primeiro método chamado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-260">Initialize must be the first method called.</span></span> <span data-ttu-id="13cb4-261">Caso contrário, todas as outras APIs retornará E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="13cb4-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="13cb4-262">Chamar Initialize em um objeto já inicializado Retorna S_OK e não faz nada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="13cb4-263">Se E_LSC_CACHEMISMATCH for retornado, o chamador pode chamar [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para excluir o cache associado a determinado SuppliedID.</span><span class="sxs-lookup"><span data-stu-id="13cb4-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="13cb4-264">No entanto, nesse caso outras APIs ainda retornará E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="13cb4-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-265">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-265">Parameters</span></span>

 <span data-ttu-id="13cb4-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="13cb4-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="13cb4-267">Identifica o consumidor e qual armazenar em cache para usar.</span><span class="sxs-lookup"><span data-stu-id="13cb4-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="13cb4-268">Deve ser não vazias com um máximo de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="13cb4-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="13cb4-269">_bstrProgID_</span></span>
  
<span data-ttu-id="13cb4-270">Identifica o objeto de COM do consumidor para comunicação bidirecional.</span><span class="sxs-lookup"><span data-stu-id="13cb4-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="13cb4-271">Deve ser não vazias com um máximo de 39 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="13cb4-272">Consulte [ \<ProgID\> chave](http://msdn.microsoft.com/pt-br/library/ms690196.aspx.aspx) para saber mais sobre ProgIDs.</span><span class="sxs-lookup"><span data-stu-id="13cb4-272">See [\<ProgID\> Key](http://msdn.microsoft.com/pt-br/library/ms690196.aspx.aspx) for more information on ProgIDs.</span></span> 
  
 <span data-ttu-id="13cb4-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="13cb4-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="13cb4-274">Identifica o diretório raiz em que serão armazenados os arquivos locais.</span><span class="sxs-lookup"><span data-stu-id="13cb4-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="13cb4-275">Deve ser não vazias com um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="13cb4-276">O diretório já deve existir.</span><span class="sxs-lookup"><span data-stu-id="13cb4-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="13cb4-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="13cb4-277">_pEventCallback_</span></span>
  
<span data-ttu-id="13cb4-278">A interface de retorno de chamada que CsiSyncClient receberá uma notificação sobre alterações.</span><span class="sxs-lookup"><span data-stu-id="13cb4-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="13cb4-279">Consulte IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="13cb4-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="13cb4-280">Este valor não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="13cb4-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="13cb4-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="13cb4-282">Retorna se um novo cache foi criado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="13cb4-283">Se nenhum cache está associado com o SuppliedID, um será criado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="13cb4-284">Este valor não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-285">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-285">Return values</span></span>

|<span data-ttu-id="13cb4-286">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-286">Value</span></span>|<span data-ttu-id="13cb4-287">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-289">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-291">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="13cb4-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="13cb4-293">Uma SuppliedID já tem um cache associado a ele, mas tem um ProgId diferente ou um FileSystemDirectoryHint que os fornecidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="13cb4-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="13cb4-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="13cb4-295">O FileSystemDirectoryHint (ou uma subpasta) já existe em um cache diferente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="13cb4-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="13cb4-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="13cb4-297">O ProgID já existe em um cache diferente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="13cb4-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-298">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-299">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="13cb4-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="13cb4-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="13cb4-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-301"></span></span>

<span data-ttu-id="13cb4-302">LocalFileChange é usado para informar ao objeto COM CsiSyncClient para tentar carregar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="13cb4-303">O método preparará o arquivo para carregar, incluindo ler o conteúdo do arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="13cb4-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="13cb4-304">Se um carregamento já estiver pendente, o carregamento anterior será descartado e o novo conteúdo preparado para carregar.</span><span class="sxs-lookup"><span data-stu-id="13cb4-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="13cb4-305">Se o arquivo está aberto para edição em um aplicativo, este método retornará S_OK sem preparar o arquivo para carregar (o aplicativo já faça esta etapa se há alterações).</span><span class="sxs-lookup"><span data-stu-id="13cb4-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="13cb4-306">Esse método permitirá que carregamentos se ela foi marcada como carrega bloqueado anteriormente (consulte [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="13cb4-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-307">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-307">Parameters</span></span>

 <span data-ttu-id="13cb4-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="13cb4-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="13cb4-309">Uma cadeia de caracteres que identifica o arquivo no cliente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="13cb4-310">Este valor deve ser um caminho de local não vazias com um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="13cb4-311">Esse caminho deve estar na árvore de pastas especificada pelo FileSystemDirectoryHint quando a chamada para [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) foi feita.</span><span class="sxs-lookup"><span data-stu-id="13cb4-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="13cb4-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13cb4-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="13cb4-313">Uma cadeia de caracteres que identifica o ResourceID do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="13cb4-314">Este valor deve ser não vazias com um máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="13cb4-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="13cb4-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="13cb4-316">Uma cadeia de caracteres que identifica o arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="13cb4-317">Este valor deve ser uma URL não vazias, válida, mas não tenha mais de INTERNET_MAX_URL_LENGTH, conforme definido pela http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="13cb4-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-318">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-318">Return values</span></span>

|<span data-ttu-id="13cb4-319">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-319">Value</span></span>|<span data-ttu-id="13cb4-320">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-322">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-324">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="13cb4-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="13cb4-326">O arquivo especificado por _bstrFileSystemPath_ tem um ResourceID diferente do especificado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="13cb4-327">Um evento do tipo LSCEventType_OnFilePathConflict é enviada quando esse erro é retornado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="13cb4-328">Consulte [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="13cb4-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="13cb4-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13cb4-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13cb4-330">O arquivo foi excluída operação intermediário.</span><span class="sxs-lookup"><span data-stu-id="13cb4-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="13cb4-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="13cb4-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="13cb4-332">Não há suporte para a extensão de arquivo fornecido pelo objeto CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="13cb4-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="13cb4-333">Consulte [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="13cb4-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="13cb4-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="13cb4-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="13cb4-335">O objeto COM não tenha agendado um carregamento porque o arquivo no cache tinha as alterações mais recentes do disco.</span><span class="sxs-lookup"><span data-stu-id="13cb4-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="13cb4-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="13cb4-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="13cb4-337">O arquivo especificado por _bstrFileSystemPath_ está ausente ou bloqueado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="13cb4-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="13cb4-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="13cb4-339">O FileSystemPath determinado não está sob o diretório raiz especificado pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita.</span><span class="sxs-lookup"><span data-stu-id="13cb4-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="13cb4-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-341">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="13cb4-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="13cb4-343">O arquivo especificado por _bstrResourceID_ tem um FileSystemPath diferente do especificado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="13cb4-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="13cb4-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="13cb4-345">O arquivo especificado já tem as alterações em um cache diferente pendentes e ainda não pode ser associado com o cache do consumidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="13cb4-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="13cb4-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="13cb4-347">O WebPath fornecido cai em um cache diferente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="13cb4-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-348">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-349">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="13cb4-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="13cb4-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="13cb4-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-351"></span></span>

<span data-ttu-id="13cb4-352">RenameFile associará uma nova URL e o caminho local para um determinado ResourceID.</span><span class="sxs-lookup"><span data-stu-id="13cb4-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="13cb4-353">Se o arquivo especificado pelo ResourceID ainda não existir no cache, será feita uma tentativa para criá-la e marcá-la para download.</span><span class="sxs-lookup"><span data-stu-id="13cb4-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-354">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-354">Parameters</span></span>

 <span data-ttu-id="13cb4-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13cb4-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="13cb4-356">Uma cadeia de caracteres que identifica o ResourceID do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="13cb4-357">Este valor deve ser não vazias com um máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="13cb4-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="13cb4-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="13cb4-359">Uma cadeia de caracteres que especifica o novo caminho local para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="13cb4-360">Este valor deve ser um caminho de local não vazias com um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="13cb4-361">Esse caminho deve estar na árvore de pastas especificada pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita.</span><span class="sxs-lookup"><span data-stu-id="13cb4-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="13cb4-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="13cb4-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="13cb4-363">Uma cadeia de caracteres que especifica a nova URL para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="13cb4-364">Este valor deve ser um URL válido do não vazias, mas não tenha mais de INTERNET_MAX_URL_LENGTH, conforme definido pela http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="13cb4-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="13cb4-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="13cb4-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="13cb4-366">Especifica se carregamentos para o novo local são permitidos no momento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-367">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-367">Return values</span></span>

|<span data-ttu-id="13cb4-368">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-368">Value</span></span>|<span data-ttu-id="13cb4-369">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-371">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-373">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="13cb4-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="13cb4-375">O _bstrNewFileSystemPath_ ou _bstrNewWebPath_ já existir no outro arquivo em qualquer cache.</span><span class="sxs-lookup"><span data-stu-id="13cb4-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="13cb4-376">Um evento do tipo LSCEventType_OnFilePathConflict é enviada quando esse erro é retornado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="13cb4-377">Consulte [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="13cb4-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="13cb4-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13cb4-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13cb4-379">As informações do arquivo foi excluídas do cache enquanto este método estava em execução.</span><span class="sxs-lookup"><span data-stu-id="13cb4-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="13cb4-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="13cb4-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="13cb4-381">O FileSystemPath determinado não está sob o diretório raiz especificado pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita.</span><span class="sxs-lookup"><span data-stu-id="13cb4-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="13cb4-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-383">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="13cb4-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="13cb4-385">O arquivo especificado está sendo sincronizado em um aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="13cb4-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="13cb4-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-386">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-387">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="13cb4-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="13cb4-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="13cb4-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-389"></span></span>

<span data-ttu-id="13cb4-390">ResetCache excluirá o cache associado a SuppliedID que foi fornecido em Initialize.</span><span class="sxs-lookup"><span data-stu-id="13cb4-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="13cb4-391">Isso inclui todas as informações do arquivo, mas deixará os arquivos no cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="13cb4-392">Este método também deixa o objeto em um estado parcialmente não inicializado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="13cb4-393">As chamadas válidas somente depois de fazer isso são [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="13cb4-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="13cb4-394">Este método pode ser chamado se Initialize falha e retorna E_LSC_CACHEMISMATCH e excluirá o cache associado a SuppliedID que foi fornecido com a chamada está falhando.</span><span class="sxs-lookup"><span data-stu-id="13cb4-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="13cb4-395">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13cb4-395">Parameters</span></span>

<span data-ttu-id="13cb4-396">None</span><span class="sxs-lookup"><span data-stu-id="13cb4-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-397">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-397">Return values</span></span>

|<span data-ttu-id="13cb4-398">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-398">Value</span></span>|<span data-ttu-id="13cb4-399">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-401">Falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-403">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-404">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-405">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="13cb4-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="13cb4-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="13cb4-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-407"></span></span>

<span data-ttu-id="13cb4-408">ServerFileChange informa ao objeto COM CsiSyncClient para marcar o arquivo especificado para download.</span><span class="sxs-lookup"><span data-stu-id="13cb4-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="13cb4-409">Se o arquivo está aberto em um aplicativo do Office para edição, este método retornará S_OK sem marcar o arquivo para download (o aplicativo já faça esta etapa se há alterações).</span><span class="sxs-lookup"><span data-stu-id="13cb4-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="13cb4-410">Esse método permitirá que downloads se ela foi marcada como downloads bloqueado anteriormente (consulte RenameFile).</span><span class="sxs-lookup"><span data-stu-id="13cb4-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-411">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13cb4-411">Parameters</span></span>

|<span data-ttu-id="13cb4-412">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="13cb4-412">Parameter</span></span>|<span data-ttu-id="13cb4-413">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="13cb4-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="13cb4-415">Uma cadeia de caracteres que identifica o arquivo no cliente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="13cb4-416">Este valor deve ser um caminho de local não vazias com um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="13cb4-417">Esse caminho deve estar na árvore de pastas especificada pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita.</span><span class="sxs-lookup"><span data-stu-id="13cb4-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="13cb4-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="13cb4-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="13cb4-419">Uma cadeia de caracteres que identifica o ResourceID do arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="13cb4-420">Este valor deve ser não vazias com um máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13cb4-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="13cb4-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="13cb4-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="13cb4-422">Uma cadeia de caracteres que identifica o arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="13cb4-423">Este valor deve ser uma URL válida não vazias, mas não tenha mais de INTERNET_MAX_URL_LENGTH, conforme definido pela http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="13cb4-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="13cb4-424">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-424">Return values</span></span>

|<span data-ttu-id="13cb4-425">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-425">Value</span></span>|<span data-ttu-id="13cb4-426">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-428">Falha para definir o estado de conectividade do cache.</span><span class="sxs-lookup"><span data-stu-id="13cb4-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="13cb4-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="13cb4-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="13cb4-430">O arquivo especificado por _bstrFileSystemPath_ tem um ResourceID diferente do especificado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="13cb4-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="13cb4-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="13cb4-432">Não há suporte para a extensão de arquivo fornecido pelo objeto CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="13cb4-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="13cb4-433">Consulte GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="13cb4-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="13cb4-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="13cb4-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="13cb4-435">O arquivo foi excluído em operação intermediário.</span><span class="sxs-lookup"><span data-stu-id="13cb4-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="13cb4-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-437">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="13cb4-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="13cb4-439">O FileSystemPath determinado não está sob o diretório raiz especificado pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita.</span><span class="sxs-lookup"><span data-stu-id="13cb4-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="13cb4-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-441">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="13cb4-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="13cb4-443">O arquivo especificado por _bstrResourceID_ tem um FileSystemPath diferente do especificado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="13cb4-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="13cb4-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="13cb4-445">O arquivo especificado já tem as alterações em um cache diferente pendentes e ainda não pode ser associado com o cache do consumidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="13cb4-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="13cb4-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="13cb4-447">O WebPath fornecido cai em um cache diferente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="13cb4-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-448">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-449">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="13cb4-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="13cb4-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="13cb4-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-451"></span></span>

<span data-ttu-id="13cb4-452">Define o cache em um estado online ou offline.</span><span class="sxs-lookup"><span data-stu-id="13cb4-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="13cb4-453">Se estiver offline, Office não tentará se comunicar com o servidor de arquivos nesse cache, independentemente da configuração de _fBlockUploads_ de cada arquivo individual.</span><span class="sxs-lookup"><span data-stu-id="13cb4-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-454">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-454">Parameters</span></span>

 <span data-ttu-id="13cb4-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="13cb4-455">_fIsOnline_</span></span>
  
<span data-ttu-id="13cb4-456">Um Booleano determinando o estado de conectividade do cache.</span><span class="sxs-lookup"><span data-stu-id="13cb4-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-457">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-457">Return values</span></span>

|<span data-ttu-id="13cb4-458">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-458">Value</span></span>|<span data-ttu-id="13cb4-459">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-461">Falha para definir o estado de conectividade do cache.</span><span class="sxs-lookup"><span data-stu-id="13cb4-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="13cb4-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-463">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-465">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-466">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-467">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="13cb4-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="13cb4-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="13cb4-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-469"></span></span>

<span data-ttu-id="13cb4-470">SetClientNetworkSyncPermission é usado para qualquer substituição ou heurística de sincronização do restoreOffice para uso de custo e alimentação de rede.</span><span class="sxs-lookup"><span data-stu-id="13cb4-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="13cb4-471">Quando em um 3G ou outra rede de alto custo, ou quando executando em bateria versus sendo conectado, o Office pode optar por bloquear o tráfego de rede até um momento mais oportunidade.</span><span class="sxs-lookup"><span data-stu-id="13cb4-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="13cb4-472">O consumidor desse API pode ser usada para substituir heurística do Office e forçar sincronizando para que ela ocorra.</span><span class="sxs-lookup"><span data-stu-id="13cb4-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-473">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-473">Parameters</span></span>

 <span data-ttu-id="13cb4-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="13cb4-474">_nspType_</span></span>
  
<span data-ttu-id="13cb4-475">Um sinalizador que define qual heurístico custo substituir.</span><span class="sxs-lookup"><span data-stu-id="13cb4-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="13cb4-476">Consulte [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="13cb4-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="13cb4-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="13cb4-477">_fEnableSync_</span></span>
  
<span data-ttu-id="13cb4-478">Especifica se é para forçar a sincronização on, substituindo assim que heurístico custo ou não são mais substituí-la.</span><span class="sxs-lookup"><span data-stu-id="13cb4-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-479">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-479">Return values</span></span>

|<span data-ttu-id="13cb4-480">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-480">Value</span></span>|<span data-ttu-id="13cb4-481">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-483">Falha ao substituir heurísticos de sincronização.</span><span class="sxs-lookup"><span data-stu-id="13cb4-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="13cb4-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-485">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-486">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-487">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="13cb4-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="13cb4-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="13cb4-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-489"></span></span>

<span data-ttu-id="13cb4-490">Descarrega o cache do objeto COM e realizar operações de fechamento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="13cb4-491">[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DEVE ser chamado antes destruir o objeto COM.</span><span class="sxs-lookup"><span data-stu-id="13cb4-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="13cb4-492">Depois que a chamada, outras APIs não pode ser chamados, o objeto COM deve ser destruído e um novo criada se você desejar operações contínuas.</span><span class="sxs-lookup"><span data-stu-id="13cb4-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="13cb4-493">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13cb4-493">Parameters</span></span>

<span data-ttu-id="13cb4-494">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="13cb4-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-495">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-495">Return values</span></span>

|<span data-ttu-id="13cb4-496">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-496">Value</span></span>|<span data-ttu-id="13cb4-497">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-499">Falha para reverter a.</span><span class="sxs-lookup"><span data-stu-id="13cb4-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="13cb4-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13cb4-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="13cb4-501">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="13cb4-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-502">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-503">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="13cb4-504">Interface IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="13cb4-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="13cb4-505">Essa interface representa uma lista de eventos ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="13cb4-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="13cb4-506">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13cb4-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="13cb4-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="13cb4-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="13cb4-508">Recupera o próximo evento da lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-509">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-509">Parameters</span></span>

 <span data-ttu-id="13cb4-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="13cb4-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="13cb4-511">Um ponteiro para uma interface ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="13cb4-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-512">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-512">Return values</span></span>

|<span data-ttu-id="13cb4-513">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-513">Value</span></span>|<span data-ttu-id="13cb4-514">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-516">Não existem mais eventos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="13cb4-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-517">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-518">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="13cb4-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="13cb4-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="13cb4-520">Redefine o enumerador para o primeiro evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="13cb4-521">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13cb4-521">Parameters</span></span>

<span data-ttu-id="13cb4-522">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="13cb4-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-523">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-523">Return values</span></span>

<span data-ttu-id="13cb4-524">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13cb4-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="13cb4-525">Interface ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="13cb4-525">Interface ILSCEvent</span></span>

<span data-ttu-id="13cb4-526">Essa interface representa um evento de sincronização.</span><span class="sxs-lookup"><span data-stu-id="13cb4-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="13cb4-527">Todas as informações sobre o evento podem ser recuperadas da interface.</span><span class="sxs-lookup"><span data-stu-id="13cb4-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="13cb4-528">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13cb4-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="13cb4-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="13cb4-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="13cb4-530">Observe que esse valor é preenchido quando [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) é chamado, não quando o evento tiver sido criado, portanto você terá somente o status atual do arquivo, não o status do arquivo quando o status de conflito alterado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="13cb4-531">Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="13cb4-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-532">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-532">Parameters</span></span>

 <span data-ttu-id="13cb4-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="13cb4-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="13cb4-534">O status atual de conflito do arquivo associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-535">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-535">Return values</span></span>

<span data-ttu-id="13cb4-536">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13cb4-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="13cb4-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="13cb4-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="13cb4-538">Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="13cb4-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-539">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-539">Parameters</span></span>

 <span data-ttu-id="13cb4-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="13cb4-540">_pnError_</span></span>
  
<span data-ttu-id="13cb4-541">O erro associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-542">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-542">Return values</span></span>

<span data-ttu-id="13cb4-543">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13cb4-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="13cb4-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="13cb4-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="13cb4-545">Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="13cb4-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-546">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-546">Parameters</span></span>

 <span data-ttu-id="13cb4-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="13cb4-547">_pbstrETag_</span></span>
  
<span data-ttu-id="13cb4-548">A ETag associada ao evento</span><span class="sxs-lookup"><span data-stu-id="13cb4-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-549">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-549">Return values</span></span>

<span data-ttu-id="13cb4-550">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13cb4-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="13cb4-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="13cb4-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="13cb4-552">Obtém o tipo para este evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-553">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-553">Parameters</span></span>

 <span data-ttu-id="13cb4-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="13cb4-554">_pnEventType_</span></span>
  
<span data-ttu-id="13cb4-555">O tipo de evento desse evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-555">The event type of this event.</span></span> <span data-ttu-id="13cb4-556">Consulte [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para valores válidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="13cb4-557">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-558">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-558">Return values</span></span>

|<span data-ttu-id="13cb4-559">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-559">Value</span></span>|<span data-ttu-id="13cb4-560">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-562">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-563">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-564">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="13cb4-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="13cb4-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="13cb4-566">Obtém o caminho local de trabalho para este evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-567">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-567">Parameters</span></span>

 <span data-ttu-id="13cb4-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="13cb4-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="13cb4-569">O caminho local do arquivo para o qual esse evento pertence.</span><span class="sxs-lookup"><span data-stu-id="13cb4-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-570">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-570">Return values</span></span>

<span data-ttu-id="13cb4-571">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13cb4-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="13cb4-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="13cb4-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="13cb4-573">Obtém a identificação do recurso para o evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-574">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-574">Parameters</span></span>

 <span data-ttu-id="13cb4-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="13cb4-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="13cb4-576">ResourceID do arquivo associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-577">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-577">Return values</span></span>

<span data-ttu-id="13cb4-578">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13cb4-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="13cb4-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="13cb4-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="13cb4-580">Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="13cb4-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="13cb4-581">Quando uma chamada para [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) pode causar um conflito de caminho da Web ou caminho Local com outro arquivo no cache de arquivo do Office, isso evento ser gerado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-582">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-582">Parameters</span></span>

 <span data-ttu-id="13cb4-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="13cb4-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="13cb4-584">O ResourceID que gerou esse evento obter gerado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="13cb4-585">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-586">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-586">Return values</span></span>

<span data-ttu-id="13cb4-587">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13cb4-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="13cb4-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="13cb4-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="13cb4-589">Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="13cb4-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-590">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-590">Parameters</span></span>

 <span data-ttu-id="13cb4-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="13cb4-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="13cb4-592">O tipo de erro associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-592">The error type associated with this event.</span></span> <span data-ttu-id="13cb4-593">Consulte [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="13cb4-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="13cb4-594">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-595">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-595">Return values</span></span>

|<span data-ttu-id="13cb4-596">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-596">Value</span></span>|<span data-ttu-id="13cb4-597">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-599">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-600">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-601">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="13cb4-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="13cb4-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="13cb4-603">Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="13cb4-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-604">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-604">Parameters</span></span>

 <span data-ttu-id="13cb4-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="13cb4-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="13cb4-606">Especifica o caminho da Web associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="13cb4-607">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-608">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-608">Return values</span></span>

<span data-ttu-id="13cb4-609">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13cb4-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="13cb4-610">Interface ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="13cb4-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="13cb4-611">Essa interface contém informações adicionais sobre um evento de sincronização.</span><span class="sxs-lookup"><span data-stu-id="13cb4-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="13cb4-612">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13cb4-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="13cb4-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="13cb4-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="13cb4-614">Obtém as informações de cadeia de erro sobre um evento de sincronização.</span><span class="sxs-lookup"><span data-stu-id="13cb4-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-615">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-615">Parameters</span></span>

 <span data-ttu-id="13cb4-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="13cb4-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="13cb4-617">Uma cadeia de caracteres para armazenar as informações de cadeia de erro.</span><span class="sxs-lookup"><span data-stu-id="13cb4-617">A string to hold the error chain information.</span></span> <span data-ttu-id="13cb4-618">Não deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="13cb4-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-619">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-619">Return values</span></span>

|<span data-ttu-id="13cb4-620">Value</span><span class="sxs-lookup"><span data-stu-id="13cb4-620">Value</span></span>|<span data-ttu-id="13cb4-621">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="13cb4-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="13cb4-623">A versão instalada do Office não oferece suporte a essa interface</span><span class="sxs-lookup"><span data-stu-id="13cb4-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="13cb4-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13cb4-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="13cb4-625">Um ou mais dos valores de parâmetro são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="13cb4-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="13cb4-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="13cb4-627">As informações de cadeia de erro não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="13cb4-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="13cb4-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="13cb4-628">S_OK</span></span>  <br/> |<span data-ttu-id="13cb4-629">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13cb4-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="13cb4-630">Interface IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="13cb4-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="13cb4-631">Essa interface fornece uma função de retorno de chamada para o objeto COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="13cb4-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="13cb4-632">**Funções de membro público**</span><span class="sxs-lookup"><span data-stu-id="13cb4-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="13cb4-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="13cb4-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="13cb4-634">Essa é uma função de retorno de chamada no objeto dado ao objeto CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="13cb4-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="13cb4-635">Espera-se que, quando ocorre um evento (consulte [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos de evento válidos), o objeto CsiSyncClient COM chamará este método, o consumidor de sinalização.</span><span class="sxs-lookup"><span data-stu-id="13cb4-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="13cb4-636">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13cb4-636">Parameters</span></span>

 <span data-ttu-id="13cb4-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="13cb4-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="13cb4-638">O tipo de evento desse evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-638">The event type of this event.</span></span> <span data-ttu-id="13cb4-639">Consulte [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para valores válidos.</span><span class="sxs-lookup"><span data-stu-id="13cb4-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="13cb4-640">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="13cb4-640">Return values</span></span>

<span data-ttu-id="13cb4-641">Sempre retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="13cb4-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="13cb4-642">Enumerações</span><span class="sxs-lookup"><span data-stu-id="13cb4-642">Enumerations</span></span>

<span data-ttu-id="13cb4-643">CSISyncClient usa as enumerações a seguir.</span><span class="sxs-lookup"><span data-stu-id="13cb4-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="13cb4-644">Enumeração LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="13cb4-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="13cb4-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-645"></span></span>

<span data-ttu-id="13cb4-646">Essa enumeração Especifica as categorias de erros que podem ocorrer durante a sincronização de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="13cb4-647">Enumerador</span><span class="sxs-lookup"><span data-stu-id="13cb4-647">Enumerator</span></span>|<span data-ttu-id="13cb4-648">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="13cb4-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="13cb4-650">O erro de sincronização desse evento era esperado e pode exigir uma consideração especial.</span><span class="sxs-lookup"><span data-stu-id="13cb4-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="13cb4-651">Por padrão, o usuário pode ter de intervir.</span><span class="sxs-lookup"><span data-stu-id="13cb4-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="13cb4-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="13cb4-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="13cb4-653">O erro de sincronização desse evento não precisa consideração especial.</span><span class="sxs-lookup"><span data-stu-id="13cb4-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="13cb4-654">Office manipulará-lo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="13cb4-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="13cb4-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="13cb4-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="13cb4-656">O erro de sincronização desse evento exige que um usuário resolvê-lo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="13cb4-657">Por exemplo, o erro de conflito de mesclagem requer um usuário abrir o documento e mesclar a ele.</span><span class="sxs-lookup"><span data-stu-id="13cb4-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="13cb4-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="13cb4-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="13cb4-659">O erro de sincronização desse evento exige que o consumidor intervir, mas não deve exigir uma consideração especial pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="13cb4-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="13cb4-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="13cb4-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="13cb4-661">O erro de sincronização desse evento requer o consumidor intervir como um caso especial.</span><span class="sxs-lookup"><span data-stu-id="13cb4-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="13cb4-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="13cb4-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="13cb4-663">Enumeração LSCEventType</span><span class="sxs-lookup"><span data-stu-id="13cb4-663">Enum LSCEventType</span></span>
<span data-ttu-id="13cb4-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-664"></span></span>

<span data-ttu-id="13cb4-665">Essa enumeração Especifica o tipo de eventos que podem ocorrer para um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="13cb4-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="13cb4-666">Enumerador</span><span class="sxs-lookup"><span data-stu-id="13cb4-666">Enumerator</span></span>|<span data-ttu-id="13cb4-667">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="13cb4-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="13cb4-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="13cb4-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="13cb4-670">Foram feitas alterações em um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="13cb4-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="13cb4-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="13cb4-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="13cb4-672">Um usuário abre um arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="13cb4-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="13cb4-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="13cb4-674">Download de alterações no arquivo do servidor concluído.</span><span class="sxs-lookup"><span data-stu-id="13cb4-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="13cb4-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="13cb4-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="13cb4-676">Concluir a carregar alterações no arquivo para o servidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="13cb4-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="13cb4-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="13cb4-678">O estado de conflito de mesclagem de um arquivo foi alterada.</span><span class="sxs-lookup"><span data-stu-id="13cb4-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="13cb4-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="13cb4-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="13cb4-680">Um arquivo foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="13cb4-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="13cb4-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="13cb4-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="13cb4-682">Um arquivo foi excluído.</span><span class="sxs-lookup"><span data-stu-id="13cb4-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="13cb4-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="13cb4-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="13cb4-684">Sincronizando foi habilitado para arquivos do usuário.</span><span class="sxs-lookup"><span data-stu-id="13cb4-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="13cb4-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="13cb4-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="13cb4-686">Iniciado o download de alterações de arquivo do servidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="13cb4-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="13cb4-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="13cb4-688">Iniciado carregar alterações no arquivo para o servidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="13cb4-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="13cb4-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="13cb4-690">Esse evento é gerado quando uma chamada para [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) faz com que um conflito de caminho da Web ou caminho Local com outro arquivo no Cache de arquivos do Office.</span><span class="sxs-lookup"><span data-stu-id="13cb4-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="13cb4-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="13cb4-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="13cb4-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="13cb4-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="13cb4-693">Enumeração LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="13cb4-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="13cb4-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-694"></span></span>

<span data-ttu-id="13cb4-695">Essa enumeração Especifica o tipo de eventos que podem ocorrer.</span><span class="sxs-lookup"><span data-stu-id="13cb4-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="13cb4-696">O consumidor precisa chamar funções específicas de ILSCLocalSyncClient com base no tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="13cb4-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="13cb4-697">Enumerador</span><span class="sxs-lookup"><span data-stu-id="13cb4-697">Enumerator</span></span>|<span data-ttu-id="13cb4-698">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="13cb4-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="13cb4-700">Ocorreu uma ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="13cb4-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="13cb4-701">O consumidor deve chamar [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) para recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="13cb4-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="13cb4-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="13cb4-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="13cb4-703">As extensões de arquivo com suporte foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="13cb4-703">The supported file extensions have changed.</span></span> <span data-ttu-id="13cb4-704">O consumidor deve chamar [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar a nova lista de extensões aceitas.</span><span class="sxs-lookup"><span data-stu-id="13cb4-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="13cb4-705">Enumeração LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="13cb4-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="13cb4-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-706"></span></span>

<span data-ttu-id="13cb4-707">Essa enumeração Especifica os sinalizadores usados para uma heurística de custo de rede.</span><span class="sxs-lookup"><span data-stu-id="13cb4-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="13cb4-708">Enumerador</span><span class="sxs-lookup"><span data-stu-id="13cb4-708">Enumerator</span></span>|<span data-ttu-id="13cb4-709">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="13cb4-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="13cb4-711">True se o heurístico custo para redes caros (por exemplo, 3G) será substituído.</span><span class="sxs-lookup"><span data-stu-id="13cb4-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="13cb4-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="13cb4-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="13cb4-713">True se o heurístico custo para o uso de energia (por exemplo, uma bateria) será substituído.</span><span class="sxs-lookup"><span data-stu-id="13cb4-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="13cb4-714">Enumeração LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="13cb4-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="13cb4-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="13cb4-715"></span></span>

<span data-ttu-id="13cb4-716">Esta enumeração é usada para representar o status de sincronização de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="13cb4-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="13cb4-717">Enumerador</span><span class="sxs-lookup"><span data-stu-id="13cb4-717">Enumerator</span></span>|<span data-ttu-id="13cb4-718">Descrição</span><span class="sxs-lookup"><span data-stu-id="13cb4-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="13cb4-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="13cb4-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="13cb4-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="13cb4-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="13cb4-721">True se não houver pendentes dados a serem enviados para o arquivo do servidor.</span><span class="sxs-lookup"><span data-stu-id="13cb4-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="13cb4-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="13cb4-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="13cb4-723">True se não houver dados para fazer o download do arquivo server pendentes.</span><span class="sxs-lookup"><span data-stu-id="13cb4-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="13cb4-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="13cb4-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="13cb4-725">True se os dados do Office tem no arquivo no seu cache é a cópia mais recente dos dados no disco.</span><span class="sxs-lookup"><span data-stu-id="13cb4-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

