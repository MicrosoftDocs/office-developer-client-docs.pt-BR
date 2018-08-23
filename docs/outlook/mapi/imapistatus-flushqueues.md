---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 30aaaaa250155215149a941da7f7e528d65b8dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592196"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="26dc5-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="26dc5-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="26dc5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26dc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26dc5-105">Força todas as mensagens aguardando para ser enviado ou recebido para ser carregadas ou baixadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="26dc5-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="26dc5-106">Os objetos de status que implementam provedores de transporte e o objeto de status do MAPI spooler suportam este método.</span><span class="sxs-lookup"><span data-stu-id="26dc5-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="26dc5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26dc5-107">Parameters</span></span>

 <span data-ttu-id="26dc5-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="26dc5-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="26dc5-109">[in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="26dc5-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="26dc5-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="26dc5-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="26dc5-111">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpTargetTransport_ .</span><span class="sxs-lookup"><span data-stu-id="26dc5-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="26dc5-112">O parâmetro _cbTargetTransport_ é definido somente em chamadas para objeto de status do MAPI spooler.</span><span class="sxs-lookup"><span data-stu-id="26dc5-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="26dc5-113">Para chamadas a um provedor de transporte, o parâmetro _cbTargetTransport_ é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="26dc5-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="26dc5-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="26dc5-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="26dc5-115">[in] Um ponteiro para o identificador de entrada do provedor de transporte que seja a liberar seus filas de mensagens.</span><span class="sxs-lookup"><span data-stu-id="26dc5-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="26dc5-116">O parâmetro _lpTargetTransport_ é definido somente em chamadas para objeto de status do MAPI spooler.</span><span class="sxs-lookup"><span data-stu-id="26dc5-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="26dc5-117">Para chamadas a um provedor de transporte, o parâmetro _lpTargetTransport_ é definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="26dc5-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="26dc5-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26dc5-118">_ulFlags_</span></span>
  
> <span data-ttu-id="26dc5-119">[in] Uma bitmask dos sinalizadores que controla a operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="26dc5-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="26dc5-120">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="26dc5-120">The following flags can be set:</span></span>
    
<span data-ttu-id="26dc5-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="26dc5-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="26dc5-122">A operação de liberação pode ocorrer assincronamente.</span><span class="sxs-lookup"><span data-stu-id="26dc5-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="26dc5-123">Esse sinalizador se aplica somente ao objeto de status do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="26dc5-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="26dc5-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="26dc5-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="26dc5-125">As filas de mensagens de entrada devem ser liberadas.</span><span class="sxs-lookup"><span data-stu-id="26dc5-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="26dc5-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="26dc5-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="26dc5-127">A operação de liberação deve ocorrer independentemente, apesar da possibilidade de que uma diminuição no desempenho.</span><span class="sxs-lookup"><span data-stu-id="26dc5-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="26dc5-128">Esse sinalizador deve ser definida quando um provedor de transporte assíncrono está programado.</span><span class="sxs-lookup"><span data-stu-id="26dc5-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="26dc5-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="26dc5-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="26dc5-130">O objeto status não deverá exibir um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="26dc5-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="26dc5-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="26dc5-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="26dc5-132">As filas de mensagens de saída devem ser liberadas.</span><span class="sxs-lookup"><span data-stu-id="26dc5-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="26dc5-133">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="26dc5-133">Return value</span></span>

<span data-ttu-id="26dc5-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="26dc5-134">S_OK</span></span> 
  
> <span data-ttu-id="26dc5-135">A operação de liberação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="26dc5-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="26dc5-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="26dc5-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="26dc5-137">Outra operação está em andamento. ele deve ter permissão para concluir ou ele deve ser interrompido, antes que esta operação pode ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="26dc5-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="26dc5-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="26dc5-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="26dc5-139">O objeto status não suporta essa operação, conforme indicado pela ausência do sinalizador STATUS_FLUSH_QUEUES na propriedade de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do objeto status.</span><span class="sxs-lookup"><span data-stu-id="26dc5-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26dc5-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="26dc5-140">Remarks</span></span>

<span data-ttu-id="26dc5-141">O método **IMAPIStatus::FlushQueues** solicita que o spooler MAPI ou um provedor de transporte imediatamente enviar todas as mensagens na fila de saída ou recebe todas as mensagens da fila de entrada.</span><span class="sxs-lookup"><span data-stu-id="26dc5-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="26dc5-142">**FlushQueues** é implementado apenas pelo objeto de status de spooler MAPI e por objetos de status que suprimentos de provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="26dc5-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="26dc5-143">MAPI_E_BUSY devem ser retornadas para solicitações assíncronas, para que os clientes possam continuar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="26dc5-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="26dc5-144">Por padrão, **FlushQueues** é uma operação síncrona; controle não retorna ao chamador até que a liberação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="26dc5-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="26dc5-145">Somente a liberação operação executada pelo spooler MAPI pode ser assíncrona; os clientes solicitam esse comportamento, definindo o sinalizador FLUSH_ASYNC_OK.</span><span class="sxs-lookup"><span data-stu-id="26dc5-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="26dc5-146">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="26dc5-146">Notes to implementers</span></span>

<span data-ttu-id="26dc5-147">Implementação do provedor de um transporte remoto **FlushQueues** define bits na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) na linha de status do objeto logon para controlar como as filas são liberadas.</span><span class="sxs-lookup"><span data-stu-id="26dc5-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="26dc5-148">Se um visualizador remoto passa na sinalizar FLUSH_UPLOAD, o método **FlushQueues** deve definir os bits STATUS_INBOUND_ENABLED e STATUS_INBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="26dc5-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="26dc5-149">Se um visualizador remoto passa na sinalizar FLUSH_DOWNLOAD, o método **FlushQueues** deve definir os bits STATUS_OUTBOUND_ENABLED e STATUS_OUTBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="26dc5-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="26dc5-150">**FlushQueues** , em seguida, deve retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="26dc5-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="26dc5-151">O MAPI spooler então iniciarão as ações apropriadas para carregar e baixar mensagens.</span><span class="sxs-lookup"><span data-stu-id="26dc5-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="26dc5-152">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="26dc5-152">Notes to callers</span></span>

<span data-ttu-id="26dc5-153">Uma chamada para o objeto de status do MAPI spooler é uma diretiva para transferir todas as mensagens de ou o provedor de transporte adequado.</span><span class="sxs-lookup"><span data-stu-id="26dc5-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="26dc5-154">Quando você chama o objeto de status de um provedor transporte individual, somente as mensagens desse provedor serão afetadas.</span><span class="sxs-lookup"><span data-stu-id="26dc5-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26dc5-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="26dc5-155">See also</span></span>



[<span data-ttu-id="26dc5-156">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="26dc5-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="26dc5-157">Propriedade canônica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="26dc5-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="26dc5-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="26dc5-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

