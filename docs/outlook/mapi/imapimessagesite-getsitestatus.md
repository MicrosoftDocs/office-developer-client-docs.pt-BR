---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7d81533b13f4f44a0644215e009dc3477717e9a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767084"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="d7575-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="d7575-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="d7575-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7575-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7575-105">Retorna informações de um objeto de site de mensagem sobre a mensagem de recursos do site da mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="d7575-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="d7575-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7575-106">Parameters</span></span>

 <span data-ttu-id="d7575-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="d7575-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="d7575-108">[out] Um ponteiro para uma bitmask dos sinalizadores que fornece informações sobre o status da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7575-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="d7575-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="d7575-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d7575-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="d7575-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="d7575-111">A mensagem pode ser copiada.</span><span class="sxs-lookup"><span data-stu-id="d7575-111">The message can be copied.</span></span> 
    
<span data-ttu-id="d7575-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="d7575-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="d7575-113">A mensagem pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="d7575-113">The message can be deleted.</span></span>
    
<span data-ttu-id="d7575-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="d7575-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="d7575-115">Quando excluídas, uma mensagem é movida para uma pasta de **Itens excluídos** no seu armazenamento de mensagens em vez de sendo imediatamente removido do seu armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d7575-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="d7575-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="d7575-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="d7575-117">A mensagem pode ser movida.</span><span class="sxs-lookup"><span data-stu-id="d7575-117">The message can be moved.</span></span>
    
<span data-ttu-id="d7575-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="d7575-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="d7575-119">Uma nova mensagem pode ser criada.</span><span class="sxs-lookup"><span data-stu-id="d7575-119">A new message can be created.</span></span>
    
<span data-ttu-id="d7575-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="d7575-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="d7575-121">A mensagem pode ser salva.</span><span class="sxs-lookup"><span data-stu-id="d7575-121">The message can be saved.</span></span>
    
<span data-ttu-id="d7575-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="d7575-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="d7575-123">A mensagem pode ser enviada.</span><span class="sxs-lookup"><span data-stu-id="d7575-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7575-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d7575-124">Return value</span></span>

<span data-ttu-id="d7575-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7575-125">S_OK</span></span> 
  
> <span data-ttu-id="d7575-126">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="d7575-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7575-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7575-127">Remarks</span></span>

<span data-ttu-id="d7575-128">Objetos de formulário chame o método **IMAPIMessageSite::GetSiteStatus** para obter os recursos do objeto de site a mensagem para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="d7575-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="d7575-129">Os sinalizadores retornados no parâmetro _lpulStatus_ fornecem informações sobre o site da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7575-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="d7575-130">Normalmente, um formulário habilita ou desabilita o comandos de menu, dependendo de informações que os sinalizadores fornecem sobre os recursos da implementação do site de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7575-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="d7575-131">Se uma nova mensagem for carregada para um formulário, o método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) ou o método [IPersistMessage::Load](ipersistmessage-load.md) , os sinalizadores de status devem ser verificados.</span><span class="sxs-lookup"><span data-stu-id="d7575-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="d7575-132">Alguns objetos de site de mensagem, especialmente objetos de somente leitura, não permitir que as mensagens sejam salvos ou excluído.</span><span class="sxs-lookup"><span data-stu-id="d7575-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d7575-133">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="d7575-133">Notes to implementers</span></span>

<span data-ttu-id="d7575-134">O método **IMAPIMessageSite::GetSiteStatus** pode exigir o aplicativo cliente para realizar algumas cálculo para determinar quais operações podem ou não podem ser executadas na mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="d7575-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="d7575-135">Normalmente, o que envolve olhando a linha de status para o provedor de armazenamento de mensagem da mensagem atual, ou consultar o provedor de armazenamento para determinar quais ações o aplicativo cliente pode executar usando o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d7575-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="d7575-136">Por exemplo, para determinar se é necessário retornar o sinalizador MAPI_DELETE_IS_MOVE, verifique a mensagem repositório de propriedade do objeto **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) para ver se há uma pasta de **Itens excluídos** no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d7575-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="d7575-137">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d7575-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d7575-138">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d7575-138">MFCMAPI reference</span></span>

<span data-ttu-id="d7575-139">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7575-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d7575-140">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d7575-140">**File**</span></span>|<span data-ttu-id="d7575-141">**Function**</span><span class="sxs-lookup"><span data-stu-id="d7575-141">**Function**</span></span>|<span data-ttu-id="d7575-142">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d7575-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7575-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d7575-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d7575-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="d7575-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="d7575-145">MFCMAPI usa o método **IMAPIMessageSite::GetSiteStatus** para obter o status do site especificado.</span><span class="sxs-lookup"><span data-stu-id="d7575-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="d7575-146">Ele pode retornar VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE ou VCSTATUS_SUBMIT.</span><span class="sxs-lookup"><span data-stu-id="d7575-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7575-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7575-147">See also</span></span>



[<span data-ttu-id="d7575-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="d7575-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="d7575-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="d7575-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="d7575-150">Propriedade canônica PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="d7575-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="d7575-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7575-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d7575-152">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d7575-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d7575-153">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="d7575-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

