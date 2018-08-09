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
ms.openlocfilehash: 3ff29ac7e7f9b7876bb678930390ca556351ecf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767233"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="f7b49-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="f7b49-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="f7b49-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7b49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7b49-105">Confirma as informações de status externos disponíveis para o recurso MAPI ou o provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="f7b49-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="f7b49-106">Esse método é suportado em todos os objetos de status.</span><span class="sxs-lookup"><span data-stu-id="f7b49-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f7b49-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7b49-107">Parameters</span></span>

<span data-ttu-id="f7b49-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f7b49-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="f7b49-109">[in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="f7b49-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="f7b49-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7b49-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f7b49-111">[in] Uma bitmask dos sinalizadores que controla a validação.</span><span class="sxs-lookup"><span data-stu-id="f7b49-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="f7b49-112">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f7b49-112">The following flags can be set:</span></span>
    
<span data-ttu-id="f7b49-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="f7b49-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="f7b49-114">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo correspondente.</span><span class="sxs-lookup"><span data-stu-id="f7b49-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="f7b49-115">O objeto de status tem duas opções:</span><span class="sxs-lookup"><span data-stu-id="f7b49-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="f7b49-116">Continue trabalhando na operação.</span><span class="sxs-lookup"><span data-stu-id="f7b49-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="f7b49-117">Interromper a operação e retornar MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="f7b49-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="f7b49-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="f7b49-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="f7b49-119">Um ou mais das propriedades de configuração do objeto status é alterado.</span><span class="sxs-lookup"><span data-stu-id="f7b49-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="f7b49-120">Clientes podem definir esse sinalizador para permitir que o spooler MAPI para dinamicamente corrigir falhas de provedor de transporte crítico.</span><span class="sxs-lookup"><span data-stu-id="f7b49-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="f7b49-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="f7b49-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="f7b49-122">O objeto de status deve realizar uma conexão.</span><span class="sxs-lookup"><span data-stu-id="f7b49-122">The status object should perform a connection.</span></span> <span data-ttu-id="f7b49-123">Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a conexão ocorre sem cache.</span><span class="sxs-lookup"><span data-stu-id="f7b49-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="f7b49-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="f7b49-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="f7b49-125">O objeto de status deve realizar uma operação de desconexão.</span><span class="sxs-lookup"><span data-stu-id="f7b49-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="f7b49-126">Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, a desconexão ocorre sem cache.</span><span class="sxs-lookup"><span data-stu-id="f7b49-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="f7b49-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="f7b49-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="f7b49-128">As entradas da tabela de cache de cabeçalho devem ser processadas, todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DOWNLOAD devem ser baixadas e todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DELETE devem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="f7b49-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="f7b49-129">Mensagens que tenham MSGSTATUS_REMOTE_DOWNLOAD e o MSGSTATUS_REMOTE_DELETE definido devem ser movidas.</span><span class="sxs-lookup"><span data-stu-id="f7b49-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="f7b49-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="f7b49-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="f7b49-131">Para um provedor de transporte remoto, uma nova lista de cabeçalhos de mensagem deve ser baixada e todos os sinalizadores que marcam o status da mensagem devem ser desmarcados.</span><span class="sxs-lookup"><span data-stu-id="f7b49-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="f7b49-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="f7b49-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="f7b49-133">Impede que o objeto de status exiba uma interface do usuário como parte da operação.</span><span class="sxs-lookup"><span data-stu-id="f7b49-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7b49-134">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f7b49-134">Return value</span></span>

<span data-ttu-id="f7b49-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7b49-135">S_OK</span></span> 
  
> <span data-ttu-id="f7b49-136">A validação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f7b49-136">The validation was successful.</span></span>
    
<span data-ttu-id="f7b49-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="f7b49-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="f7b49-138">Outra operação está em andamento. ele deve ter permissão para concluir ou ele deve ser interrompido, antes que esta operação seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="f7b49-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="f7b49-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f7b49-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f7b49-140">O objeto status não suporta o método de validação, conforme indicado pela ausência do sinalizador STATUS_VALIDATE_STATE na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f7b49-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="f7b49-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f7b49-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f7b49-142">O usuário cancelou a operação de validação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f7b49-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="f7b49-143">Esse valor será retornado somente por provedores de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="f7b49-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f7b49-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7b49-144">Remarks</span></span>

<span data-ttu-id="f7b49-145">O método **IMAPIStatus::ValidateState** verifica o estado de um recurso que está associado um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="f7b49-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="f7b49-146">**ValidateState** é o único método na interface do [IMAPIStatus](imapistatusimapiprop.md) que é necessário para todos os objetos de status.</span><span class="sxs-lookup"><span data-stu-id="f7b49-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="f7b49-147">O comportamento exato desse método depende da implementação.</span><span class="sxs-lookup"><span data-stu-id="f7b49-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="f7b49-148">A tabela a seguir descreve a implementação de cada um dos diferentes tipos de objetos de status.</span><span class="sxs-lookup"><span data-stu-id="f7b49-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="f7b49-149">**Objeto de status**</span><span class="sxs-lookup"><span data-stu-id="f7b49-149">**Status object**</span></span>|<span data-ttu-id="f7b49-150">ValidateState * * implementação * *</span><span class="sxs-lookup"><span data-stu-id="f7b49-150">****ValidateState** implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7b49-151">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="f7b49-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="f7b49-152">Valida o estado de todos os recursos que possuem os provedores de serviço ativas no momento e o subsistema em si.</span><span class="sxs-lookup"><span data-stu-id="f7b49-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="f7b49-153">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="f7b49-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="f7b49-154">Executa um logon de todos os provedores de transporte, independentemente dos se eles já estão conectados.</span><span class="sxs-lookup"><span data-stu-id="f7b49-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="f7b49-155">Catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="f7b49-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="f7b49-156">Verifica se as entradas em sua seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="f7b49-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="f7b49-157">Provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="f7b49-157">Service provider</span></span>  <br/> |<span data-ttu-id="f7b49-158">Implementação depende do tipo de provedor e os sinalizadores definidos no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f7b49-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="f7b49-159">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="f7b49-159">Notes to implementers</span></span>

<span data-ttu-id="f7b49-160">Aplicativos de cliente remoto chamam o método de **ValidateState** para iniciar remoto de processamento para várias ações.</span><span class="sxs-lookup"><span data-stu-id="f7b49-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="f7b49-161">Este método existe principalmente para definir os bits de status para se comunicar com o spooler MAPI, em vez de realmente fazer qualquer trabalho.</span><span class="sxs-lookup"><span data-stu-id="f7b49-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="f7b49-162">Normalmente, o provedor de transporte define sinalizadores em sua linha de status que indicam como o spooler MAPI quais ações precisam ser iniciadas a fim de concluir a solicitação do cliente.</span><span class="sxs-lookup"><span data-stu-id="f7b49-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="f7b49-163">Nesse modelo de interação spooler de transporte de cliente, as ações solicitadas pelo cliente são assíncronas, que **ValidateState** retorna antes das ações solicitadas tiverem sido concluídas.</span><span class="sxs-lookup"><span data-stu-id="f7b49-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="f7b49-164">No entanto, ações que não envolvem necessariamente o sistema de mensagens subjacente ou que envolvem uma interface específico de transporte, podem ser sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="f7b49-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="f7b49-165">O aplicativo cliente passa em uma bitmask dos sinalizadores a seguir para especificar quais ações o provedor de transporte remoto deve ser adotada.</span><span class="sxs-lookup"><span data-stu-id="f7b49-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="f7b49-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="f7b49-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="f7b49-167">Se possível, o provedor de transporte remoto deve cancelar qualquer operação que envolvem o download de cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="f7b49-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="f7b49-168">Para fazer isso, o provedor de transporte deve definir os seguintes valores de propriedade na linha de status do objeto logon:</span><span class="sxs-lookup"><span data-stu-id="f7b49-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="f7b49-169">Desmarque os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) para informar o spooler MAPI para interromper o processo de liberação de entrada para esse provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="f7b49-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="f7b49-170">Defina o STATUS_OFFLINE bit na propriedade **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="f7b49-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="f7b49-171">Defina a propriedade **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) como TRUE.</span><span class="sxs-lookup"><span data-stu-id="f7b49-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="f7b49-172">Defina a propriedade de **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f7b49-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="f7b49-173">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="f7b49-173">Return S_OK.</span></span> <span data-ttu-id="f7b49-174">No entanto, se a operação em andamento não pode ser cancelada, **ValidateState** deve retornar MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="f7b49-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="f7b49-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="f7b49-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="f7b49-176">Um provedor de transporte remoto nunca deve estabelecer uma conexão a um recurso compartilhado (por exemplo, um modem ou porta COM) fora do contexto da interação spooler-transporte MAPI envolvida no método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) .</span><span class="sxs-lookup"><span data-stu-id="f7b49-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="f7b49-177">Se **ValidateState** for chamado com esse sinalizador, seu provedor de transporte deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7b49-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="f7b49-178">Defina um sinalizador interno de status para indicar que a conexão remota deve ser estabelecida quando o método **IXPLogon::FlushQueues** é chamado.</span><span class="sxs-lookup"><span data-stu-id="f7b49-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="f7b49-179">Defina os valores corretos na tabela de status para fazer com que o MAPI spooler iniciar a fila de liberação do processo.</span><span class="sxs-lookup"><span data-stu-id="f7b49-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="f7b49-180">Quando estiver concluída liberação de filas, libere o recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f7b49-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="f7b49-181">Desmarque o STATUS_OFFLINE bit na propriedade **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="f7b49-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="f7b49-182">Retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="f7b49-182">Return S_OK.</span></span>
    
<span data-ttu-id="f7b49-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="f7b49-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="f7b49-184">O provedor de transporte remoto deve liberar a sua conexão aos recursos do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f7b49-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="f7b49-185">Depois de fazer isso, ele deve definido o bit STATUS_OFFLINE na propriedade **PR_STATUS_CODE** e retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="f7b49-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="f7b49-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="f7b49-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="f7b49-187">O provedor de transporte remoto deve processam remoto e carregar todas as mensagens que tenham sido adiadas.</span><span class="sxs-lookup"><span data-stu-id="f7b49-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="f7b49-188">Para fazer isso, o provedor de transporte deve definir os seguintes valores de propriedade na linha de status do objeto logon:</span><span class="sxs-lookup"><span data-stu-id="f7b49-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="f7b49-189">Defina a propriedade **PR_STATUS_STRING** como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f7b49-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="f7b49-190">Defina os bits STATUS_OUTBOUND_ENABLED e STATUS_OUTBOUND_ACTIVE na propriedade **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="f7b49-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="f7b49-191">Defina a propriedade **PR_REMOTE_VALIDATE_OK** na linha de status do provedor de transporte como FALSE.</span><span class="sxs-lookup"><span data-stu-id="f7b49-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="f7b49-192">Se outra operação está em andamento (por exemplo, o download de cabeçalhos) quando **ValidateState** é chamado, **ValidateState** deve retornar MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="f7b49-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="f7b49-193">Execute o código para processar o sinalizador REFRESH_XP_HEADER_CACHE, também, para atender aos requisitos do cliente do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="f7b49-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="f7b49-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="f7b49-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="f7b49-195">O provedor de transporte remoto deve recuperar quaisquer cabeçalhos de mensagens novas do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f7b49-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="f7b49-196">Para fazer isso, o provedor de transporte deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7b49-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="f7b49-197">Defina a propriedade **PR_STATUS_STRING** como uma cadeia de caracteres que indica o status do provedor de transporte para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f7b49-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="f7b49-198">Defina os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE na propriedade **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="f7b49-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="f7b49-199">Desmarque o STATUS_OFFLINE bit na propriedade **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="f7b49-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="f7b49-200">Defina o STATUS_ONLINE bit na propriedade **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="f7b49-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="f7b49-201">Defina a propriedade **PR_REMOTE_VALIDATE_OK** na linha de status do provedor de transporte como FALSE.</span><span class="sxs-lookup"><span data-stu-id="f7b49-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="f7b49-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="f7b49-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="f7b49-203">Se seu provedor de transporte tiver quaisquer partes da interface do usuário para processar os cabeçalhos de mensagem (por exemplo, uma caixa de diálogo que confirma que o download de mensagens), essa caixa de diálogo deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="f7b49-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="f7b49-204">Caso contrário, **ValidateState** pode retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="f7b49-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="f7b49-205">Se quaisquer sinalizadores diferentes desses sejam passados, **ValidateState** deve retornar MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="f7b49-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="f7b49-206">Chamada do cliente para o provedor de transporte frequentemente será para o método **IMAPIStatus::ValidateState** .</span><span class="sxs-lookup"><span data-stu-id="f7b49-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="f7b49-207">Durante o processamento de **ValidateState**, o provedor de transporte não deve executar nenhuma ação que aloca recursos escassos do sistema, como um modem ou porta COM.</span><span class="sxs-lookup"><span data-stu-id="f7b49-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="f7b49-208">Isso ocorre porque o MAPI spooler em alguns casos, será necessário liberar filas em mais de um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="f7b49-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="f7b49-209">No entanto, o cliente pode chamar o método de **ValidateState** de qualquer provedor de transporte a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="f7b49-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="f7b49-210">Se seu provedor de transporte tentar alocar um recurso escasso durante o processamento de **ValidateState**, pode resultar em um erro devido a conflito com outro provedor de transporte que o MAPI spooler tem instruído a liberar seus filas.</span><span class="sxs-lookup"><span data-stu-id="f7b49-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="f7b49-211">Se você permitir todas as alocações de recursos escassos ocorra sob a orientação do spooler MAPI, você pode evitar esses conflitos.</span><span class="sxs-lookup"><span data-stu-id="f7b49-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="f7b49-212">Seu provedor de transporte deve oferecer suporte a propriedade **PR_REMOTE_VALIDATE_OK** para que aplicativos cliente podem detectar quando seu provedor de transporte está ocupado ou aguardando o MAPI spooler iniciar uma ação.</span><span class="sxs-lookup"><span data-stu-id="f7b49-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f7b49-213">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f7b49-213">Notes to callers</span></span>

<span data-ttu-id="f7b49-214">Como este método pode causar outras potencialmente demoradas chamadas sejam feitas, **ValidateState** pode retornar MAPI_E_BUSY para informá-lo de que esse método está aguardando a conclusão de outra operação.</span><span class="sxs-lookup"><span data-stu-id="f7b49-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="f7b49-215">Você deve aguardar até que a operação pendente seja concluída antes de tentar outra tarefa.</span><span class="sxs-lookup"><span data-stu-id="f7b49-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="f7b49-216">Você tem mais controle sobre suas chamadas para objetos de status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="f7b49-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="f7b49-217">Você pode passar um ou mais sinalizadores para **ValidateState** que afetam de operações o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="f7b49-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="f7b49-218">Por exemplo, o sinalizador ABORT_XP_HEADER_OPERATION indica que o usuário cancelou a validação.</span><span class="sxs-lookup"><span data-stu-id="f7b49-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="f7b49-219">Provedores de transporte podem optar por anular, retornando MAPI_E_USER_CANCELED, ou podem continuar.</span><span class="sxs-lookup"><span data-stu-id="f7b49-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="f7b49-220">Você pode definir o sinalizador CONFIG_CHANGED em uma chamada para o objeto de status de um provedor de serviço ou o spooler MAPI para indicar que uma opção de configuração foi alterada.</span><span class="sxs-lookup"><span data-stu-id="f7b49-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="f7b49-221">Você pode usar CONFIG_CHANGED para reconfigurar dinamicamente um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="f7b49-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="f7b49-222">Quando você definir CONFIG_CHANGED em uma chamada para o objeto de status de um provedor de serviços, o provedor responde com uma chamada para [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) usado para alertar o MAPI spooler da alteração.</span><span class="sxs-lookup"><span data-stu-id="f7b49-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="f7b49-223">Quando você definir CONFIG_CHANGED em uma chamada para o objeto de status do spooler MAPI, o spooler chama [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para cada provedor de transporte ativa.</span><span class="sxs-lookup"><span data-stu-id="f7b49-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="f7b49-224">**AddressTypes** informa o MAPI spooler dos tipos de endereço com suporte de um transporte.</span><span class="sxs-lookup"><span data-stu-id="f7b49-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="f7b49-225">Alguns provedores de serviços também exibem um indicador de progresso se a validação é esperada para levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="f7b49-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="f7b49-226">Exibir um indicador de progresso é útil, mas não é necessário.</span><span class="sxs-lookup"><span data-stu-id="f7b49-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="f7b49-227">Quando o sinalizador SUPPRESS_UI é definido, nenhum dos caixas de diálogo de progresso ou folhas de propriedades de configuração podem ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="f7b49-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7b49-228">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7b49-228">See also</span></span>

- [<span data-ttu-id="f7b49-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="f7b49-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="f7b49-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="f7b49-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="f7b49-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="f7b49-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="f7b49-232">Propriedade canônica PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="f7b49-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="f7b49-233">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="f7b49-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="f7b49-234">Propriedade canônica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="f7b49-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="f7b49-235">Propriedade canônica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="f7b49-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="f7b49-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f7b49-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

