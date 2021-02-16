---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438145"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="b94d7-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="b94d7-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="b94d7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b94d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b94d7-105">Confirma as informações de status externas disponíveis para o recurso MAPI ou o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="b94d7-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="b94d7-106">Esse método é suportado em todos os objetos de status.</span><span class="sxs-lookup"><span data-stu-id="b94d7-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b94d7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b94d7-107">Parameters</span></span>

<span data-ttu-id="b94d7-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b94d7-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="b94d7-109">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="b94d7-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="b94d7-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b94d7-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b94d7-111">[in] Uma máscara de bits de sinalizadores que controla a validação.</span><span class="sxs-lookup"><span data-stu-id="b94d7-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="b94d7-112">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b94d7-112">The following flags can be set:</span></span>
    
<span data-ttu-id="b94d7-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="b94d7-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="b94d7-114">O usuário cancelou a operação, normalmente clicando no botão **Cancelar** na caixa de diálogo correspondente.</span><span class="sxs-lookup"><span data-stu-id="b94d7-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="b94d7-115">O objeto de status tem duas opções:</span><span class="sxs-lookup"><span data-stu-id="b94d7-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="b94d7-116">Continue trabalhando na operação.</span><span class="sxs-lookup"><span data-stu-id="b94d7-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="b94d7-117">Pare a operação e retorne MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="b94d7-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="b94d7-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="b94d7-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="b94d7-119">Uma ou mais das propriedades de configuração do objeto de status foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="b94d7-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="b94d7-120">Os clientes podem definir esse sinalizador para permitir que o spooler MAPI corrija dinamicamente falhas críticas do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="b94d7-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="b94d7-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="b94d7-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="b94d7-122">O objeto de status deve executar uma conexão.</span><span class="sxs-lookup"><span data-stu-id="b94d7-122">The status object should perform a connection.</span></span> <span data-ttu-id="b94d7-123">Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a conexão ocorre sem armazenamento em cache.</span><span class="sxs-lookup"><span data-stu-id="b94d7-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="b94d7-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="b94d7-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="b94d7-125">O objeto de status deve executar uma operação de desconexão.</span><span class="sxs-lookup"><span data-stu-id="b94d7-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="b94d7-126">Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a desconexão ocorre sem armazenamento em cache.</span><span class="sxs-lookup"><span data-stu-id="b94d7-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="b94d7-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="b94d7-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="b94d7-128">As entradas na tabela de cache de MSGSTATUS_REMOTE_DOWNLOAD devem ser processadas, todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DOWNLOAD devem ser baixadas e todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DELETE devem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="b94d7-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="b94d7-129">As mensagens que possuem MSGSTATUS_REMOTE_DOWNLOAD e MSGSTATUS_REMOTE_DELETE definidas devem ser movidas.</span><span class="sxs-lookup"><span data-stu-id="b94d7-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="b94d7-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="b94d7-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="b94d7-131">Para um provedor de transporte remoto, uma nova lista de headers de mensagem deve ser baixada e todos os sinalizadores que marcam o status da mensagem devem ser limpos.</span><span class="sxs-lookup"><span data-stu-id="b94d7-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="b94d7-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="b94d7-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="b94d7-133">Impede que o objeto de status exibir uma interface do usuário como parte da operação.</span><span class="sxs-lookup"><span data-stu-id="b94d7-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b94d7-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b94d7-134">Return value</span></span>

<span data-ttu-id="b94d7-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="b94d7-135">S_OK</span></span> 
  
> <span data-ttu-id="b94d7-136">A validação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b94d7-136">The validation was successful.</span></span>
    
<span data-ttu-id="b94d7-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="b94d7-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="b94d7-138">Outra operação está em andamento; ela deve ter permissão para ser concluída, ou deve ser interrompida, antes que essa operação seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="b94d7-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="b94d7-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b94d7-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b94d7-140">O objeto de status não dá suporte ao método de validação, conforme indicado pela ausência do sinalizador STATUS_VALIDATE_STATE na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b94d7-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="b94d7-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="b94d7-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="b94d7-142">O usuário cancelou a operação de validação, normalmente clicando no **botão Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b94d7-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="b94d7-143">Esse valor é retornado apenas por provedores de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="b94d7-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b94d7-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="b94d7-144">Remarks</span></span>

<span data-ttu-id="b94d7-145">O **método IMAPIStatus::ValidateState** verifica o estado de um recurso associado a um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="b94d7-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="b94d7-146">**ValidateState** é o único método na interface [IMAPIStatus](imapistatusimapiprop.md) necessário para todos os objetos de status.</span><span class="sxs-lookup"><span data-stu-id="b94d7-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="b94d7-147">O comportamento exato desse método depende da implementação.</span><span class="sxs-lookup"><span data-stu-id="b94d7-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="b94d7-148">A tabela a seguir descreve a implementação de cada um dos diferentes tipos de objetos de status.</span><span class="sxs-lookup"><span data-stu-id="b94d7-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="b94d7-149">**Objeto Status**</span><span class="sxs-lookup"><span data-stu-id="b94d7-149">**Status object**</span></span>|<span data-ttu-id="b94d7-150">Implementação de ValidateState\*\*</span><span class="sxs-lookup"><span data-stu-id="b94d7-150">\*\*\*\*ValidateState\*\* implementation\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="b94d7-151">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="b94d7-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="b94d7-152">Valida o estado de todos os recursos que os provedores de serviços ativos no momento e o próprio subsistema possui.</span><span class="sxs-lookup"><span data-stu-id="b94d7-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="b94d7-153">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="b94d7-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="b94d7-154">Executa um logon de todos os provedores de transporte, independentemente de eles já estar conectados.</span><span class="sxs-lookup"><span data-stu-id="b94d7-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="b94d7-155">MapI address book</span><span class="sxs-lookup"><span data-stu-id="b94d7-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="b94d7-156">Verifica as entradas em sua seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="b94d7-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="b94d7-157">Provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="b94d7-157">Service provider</span></span>  <br/> |<span data-ttu-id="b94d7-158">A implementação depende do tipo de provedor e dos sinalizadores definidos no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="b94d7-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="b94d7-159">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="b94d7-159">Notes to implementers</span></span>

<span data-ttu-id="b94d7-160">Os aplicativos cliente remotos chamam **o método ValidateState** para iniciar o processamento remoto de várias ações.</span><span class="sxs-lookup"><span data-stu-id="b94d7-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="b94d7-161">Esse método existe principalmente para definir bits de status para se comunicar com o spooler MAPI, em vez de realmente fazer qualquer trabalho.</span><span class="sxs-lookup"><span data-stu-id="b94d7-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="b94d7-162">Normalmente, o provedor de transporte define sinalizadores em sua linha de status que indicam ao spooler MAPI quais ações precisam ser iniciadas para concluir a solicitação do cliente.</span><span class="sxs-lookup"><span data-stu-id="b94d7-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="b94d7-163">Nesse modelo de interação client-transport-spooler, as ações solicitadas pelo cliente são assíncronas, pois **ValidateState** retorna antes que as ações solicitadas sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="b94d7-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="b94d7-164">No entanto, ações que não necessariamente envolvem o sistema de mensagens subjacente, ou que envolvem uma interface específica de transporte, podem ser síncronas.</span><span class="sxs-lookup"><span data-stu-id="b94d7-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="b94d7-165">O aplicativo cliente passa uma máscara de bits dos sinalizadores a seguir para especificar quais ações o provedor de transporte remoto deve tomar.</span><span class="sxs-lookup"><span data-stu-id="b94d7-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="b94d7-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="b94d7-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="b94d7-167">Se possível, o provedor de transporte remoto deve cancelar qualquer operação que envolva o download de headers.</span><span class="sxs-lookup"><span data-stu-id="b94d7-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="b94d7-168">Para fazer isso, o provedor de transporte deve definir os seguintes valores de propriedade na linha de status do objeto de logon:</span><span class="sxs-lookup"><span data-stu-id="b94d7-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="b94d7-169">Limpe os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) para dizer ao spooler MAPI para interromper o processo de liberação de entrada para este provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="b94d7-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="b94d7-170">De definida STATUS_OFFLINE bit na **PR_STATUS_CODE** propriedade.</span><span class="sxs-lookup"><span data-stu-id="b94d7-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="b94d7-171">Definir a **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) como VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="b94d7-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="b94d7-172">Definir a **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário.</span><span class="sxs-lookup"><span data-stu-id="b94d7-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="b94d7-173">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="b94d7-173">Return S_OK.</span></span> <span data-ttu-id="b94d7-174">No entanto, se a operação em andamento não puder ser cancelada, **ValidateState** deverá retornar MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="b94d7-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="b94d7-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="b94d7-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="b94d7-176">Um provedor de transporte remoto nunca deve estabelecer uma conexão com um recurso compartilhado (por exemplo, um modem ou porta COM) fora do contexto da interação de transporte spooler MAPI envolvido no método [IXPLogon::FlushQueues.](ixplogon-flushqueues.md)</span><span class="sxs-lookup"><span data-stu-id="b94d7-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="b94d7-177">Se **ValidateState** for chamado com esse sinalizador, seu provedor de transporte deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b94d7-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="b94d7-178">Definir um sinalizador de status interno para indicar que a conexão remota deve ser estabelecida quando o método **IXPLogon::FlushQueues** for chamado.</span><span class="sxs-lookup"><span data-stu-id="b94d7-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="b94d7-179">De definir os valores corretos na tabela de status para fazer com que o spooler MAPI inicie o processo de liberação de filas.</span><span class="sxs-lookup"><span data-stu-id="b94d7-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="b94d7-180">Quando a liberação de filas estiver concluída, libere o recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b94d7-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="b94d7-181">Limpe o STATUS_OFFLINE bit na **propriedade PR_STATUS_CODE** trabalho.</span><span class="sxs-lookup"><span data-stu-id="b94d7-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="b94d7-182">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="b94d7-182">Return S_OK.</span></span>
    
<span data-ttu-id="b94d7-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="b94d7-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="b94d7-184">O provedor de transporte remoto deve liberar sua conexão com os recursos do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b94d7-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="b94d7-185">Depois de fazer isso, ele deve definir o STATUS_OFFLINE bit na propriedade **PR_STATUS_CODE** e retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="b94d7-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="b94d7-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="b94d7-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="b94d7-187">O provedor de transporte remoto deve processar mensagens remotas e carregar todas as mensagens que tenham sido adiadas.</span><span class="sxs-lookup"><span data-stu-id="b94d7-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="b94d7-188">Para fazer isso, o provedor de transporte deve definir os seguintes valores de propriedade na linha de status do objeto de logon:</span><span class="sxs-lookup"><span data-stu-id="b94d7-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="b94d7-189">De definida **PR_STATUS_STRING** propriedade como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário.</span><span class="sxs-lookup"><span data-stu-id="b94d7-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="b94d7-190">De definida STATUS_OUTBOUND_ENABLED bits STATUS_OUTBOUND_ACTIVE bits na **PR_STATUS_CODE** bits.</span><span class="sxs-lookup"><span data-stu-id="b94d7-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="b94d7-191">De definida **PR_REMOTE_VALIDATE_OK** propriedade na linha de status do provedor de transporte como FALSE.</span><span class="sxs-lookup"><span data-stu-id="b94d7-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="b94d7-192">Se outra operação estiver em andamento (como baixar os headers) quando **ValidateState** for chamado, **ValidateState** deverá retornar MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="b94d7-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="b94d7-193">Execute o código para processar o sinalizador REFRESH_XP_HEADER_CACHE, também, para atender aos requisitos do cliente Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="b94d7-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="b94d7-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="b94d7-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="b94d7-195">O provedor de transporte remoto deve recuperar quaisquer novos headers de mensagens do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b94d7-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="b94d7-196">Para fazer isso, o provedor de transporte deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b94d7-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="b94d7-197">De definida **PR_STATUS_STRING** propriedade como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário.</span><span class="sxs-lookup"><span data-stu-id="b94d7-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="b94d7-198">De definida STATUS_INBOUND_ENABLED bits STATUS_INBOUND_ACTIVE bits na **propriedade PR_STATUS_CODE** configuração.</span><span class="sxs-lookup"><span data-stu-id="b94d7-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="b94d7-199">Limpe o STATUS_OFFLINE bit na **propriedade PR_STATUS_CODE** trabalho.</span><span class="sxs-lookup"><span data-stu-id="b94d7-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="b94d7-200">De definida STATUS_ONLINE bit na **PR_STATUS_CODE** propriedade.</span><span class="sxs-lookup"><span data-stu-id="b94d7-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="b94d7-201">De definida **PR_REMOTE_VALIDATE_OK** propriedade na linha de status do provedor de transporte como FALSE.</span><span class="sxs-lookup"><span data-stu-id="b94d7-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="b94d7-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="b94d7-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="b94d7-203">Se o provedor de transporte tiver partes da interface do usuário para processar os headers de mensagem (como uma caixa de diálogo que confirma o download de mensagens), essa caixa de diálogo deverá ser exibida.</span><span class="sxs-lookup"><span data-stu-id="b94d7-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="b94d7-204">Caso contrário, **ValidateState** poderá retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="b94d7-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="b94d7-205">Se qualquer sinalizador diferente desses for passado, **ValidateState** deverá retornar MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="b94d7-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="b94d7-206">A chamada do cliente para o provedor de transporte geralmente será para o **método IMAPIStatus::ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="b94d7-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="b94d7-207">Durante o processamento de **ValidateState**, o provedor de transporte não deve executar ações que aloquem recursos de sistema fracos, como um modem ou uma porta COM.</span><span class="sxs-lookup"><span data-stu-id="b94d7-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="b94d7-208">Isso acontece porque, às vezes, o spooler MAPI precisará liberar filas em mais de um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="b94d7-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="b94d7-209">No entanto, o cliente pode chamar qualquer método **ValidateState** do provedor de transporte a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="b94d7-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="b94d7-210">Se seu provedor de transporte tentar alocar um recurso fraco durante o processamento de **ValidateState**, um erro pode resultar em conflito com outro provedor de transporte que o spooler MAPI instrutou para liberar suas filas.</span><span class="sxs-lookup"><span data-stu-id="b94d7-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="b94d7-211">Se você permitir que todas as alocações de recursos desaquedos ocorram sob a direção do spooler MAPI, poderá evitar esses conflitos.</span><span class="sxs-lookup"><span data-stu-id="b94d7-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="b94d7-212">Seu provedor de transporte deve dar suporte à propriedade **PR_REMOTE_VALIDATE_OK** para que os aplicativos cliente possam detectar quando seu provedor de transporte está ocupado ou aguardando o spooler MAPI iniciar uma ação.</span><span class="sxs-lookup"><span data-stu-id="b94d7-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b94d7-213">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b94d7-213">Notes to callers</span></span>

<span data-ttu-id="b94d7-214">Como esse método pode fazer com que outras chamadas potencialmente longas sejam feitas, **ValidateState** pode retornar MAPI_E_BUSY para informá-lo de que esse método está aguardando a conclusão de outra operação.</span><span class="sxs-lookup"><span data-stu-id="b94d7-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="b94d7-215">Você deve aguardar até que a operação pendente seja concluída antes de tentar outra tarefa.</span><span class="sxs-lookup"><span data-stu-id="b94d7-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="b94d7-216">Você tem mais controle sobre suas chamadas para objetos de status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="b94d7-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="b94d7-217">Você pode passar um ou mais sinalizadores para **ValidateState** que afetam as operações do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="b94d7-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="b94d7-218">Por exemplo, o ABORT_XP_HEADER_OPERATION sinalizador indica que o usuário cancelou a validação.</span><span class="sxs-lookup"><span data-stu-id="b94d7-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="b94d7-219">Os provedores de transporte podem optar por cancelar, retornar MAPI_E_USER_CANCELED ou podem continuar.</span><span class="sxs-lookup"><span data-stu-id="b94d7-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="b94d7-220">Você pode definir o sinalizador CONFIG_CHANGED em uma chamada para o objeto de status de um provedor de serviços ou o spooler MAPI para indicar que uma opção de configuração foi alterada.</span><span class="sxs-lookup"><span data-stu-id="b94d7-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="b94d7-221">Você pode usar o CONFIG_CHANGED para reconfigurar dinamicamente um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="b94d7-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="b94d7-222">Quando você CONFIG_CHANGED em uma chamada para o objeto de status de um provedor de serviços, o provedor responde com uma chamada para [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) para alertar o spooler MAPI da alteração.</span><span class="sxs-lookup"><span data-stu-id="b94d7-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="b94d7-223">Quando você CONFIG_CHANGED em uma chamada para o objeto de status do spooler MAPI, o spooler chama [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para cada provedor de transporte ativo.</span><span class="sxs-lookup"><span data-stu-id="b94d7-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="b94d7-224">**AddressTypes** informa ao spooler MAPI os tipos de endereço com suporte de um transporte.</span><span class="sxs-lookup"><span data-stu-id="b94d7-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="b94d7-225">Alguns provedores de serviços também exibem um indicador de progresso se a validação demorar muito.</span><span class="sxs-lookup"><span data-stu-id="b94d7-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="b94d7-226">Exibir um indicador de progresso é útil, mas não necessário.</span><span class="sxs-lookup"><span data-stu-id="b94d7-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="b94d7-227">Quando o SUPPRESS_UI sinalizador estiver definido, nenhuma das folhas de propriedades de configuração ou caixas de diálogo de progresso poderá ser exibida.</span><span class="sxs-lookup"><span data-stu-id="b94d7-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b94d7-228">Confira também</span><span class="sxs-lookup"><span data-stu-id="b94d7-228">See also</span></span>

- [<span data-ttu-id="b94d7-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="b94d7-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="b94d7-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="b94d7-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="b94d7-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="b94d7-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="b94d7-232">Propriedade canônica PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="b94d7-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="b94d7-233">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="b94d7-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="b94d7-234">Propriedade canônica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="b94d7-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="b94d7-235">Propriedade canônica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="b94d7-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="b94d7-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b94d7-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

