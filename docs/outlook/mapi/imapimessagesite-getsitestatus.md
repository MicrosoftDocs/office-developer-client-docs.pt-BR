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
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430123"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="c2af5-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="c2af5-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="c2af5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2af5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2af5-105">Retorna informações de um objeto de site de mensagem sobre os recursos do site da mensagem para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="c2af5-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="c2af5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2af5-106">Parameters</span></span>

 <span data-ttu-id="c2af5-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="c2af5-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="c2af5-108">bota Um ponteiro para uma bitmask de sinalizadores que fornece informações sobre o status da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c2af5-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="c2af5-109">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c2af5-109">The following flags can be set:</span></span>
    
<span data-ttu-id="c2af5-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="c2af5-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="c2af5-111">A mensagem pode ser copiada.</span><span class="sxs-lookup"><span data-stu-id="c2af5-111">The message can be copied.</span></span> 
    
<span data-ttu-id="c2af5-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="c2af5-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="c2af5-113">A mensagem pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="c2af5-113">The message can be deleted.</span></span>
    
<span data-ttu-id="c2af5-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="c2af5-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="c2af5-115">Quando excluído, uma mensagem é movida para uma pasta **itens excluídos** em seu repositório de mensagens, em vez de ser imediatamente removida do seu repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c2af5-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="c2af5-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="c2af5-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="c2af5-117">A mensagem pode ser movida.</span><span class="sxs-lookup"><span data-stu-id="c2af5-117">The message can be moved.</span></span>
    
<span data-ttu-id="c2af5-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c2af5-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="c2af5-119">Uma nova mensagem pode ser criada.</span><span class="sxs-lookup"><span data-stu-id="c2af5-119">A new message can be created.</span></span>
    
<span data-ttu-id="c2af5-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="c2af5-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="c2af5-121">A mensagem pode ser salva.</span><span class="sxs-lookup"><span data-stu-id="c2af5-121">The message can be saved.</span></span>
    
<span data-ttu-id="c2af5-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="c2af5-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="c2af5-123">A mensagem pode ser enviada.</span><span class="sxs-lookup"><span data-stu-id="c2af5-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c2af5-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c2af5-124">Return value</span></span>

<span data-ttu-id="c2af5-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2af5-125">S_OK</span></span> 
  
> <span data-ttu-id="c2af5-126">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c2af5-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2af5-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2af5-127">Remarks</span></span>

<span data-ttu-id="c2af5-128">Os objetos Form chamam o método **IMAPIMessageSite:: GetSiteStatus** para obter os recursos do objeto site da mensagem para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="c2af5-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="c2af5-129">Os sinalizadores retornados no parâmetro _lpulStatus_ fornecem informações sobre o site da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c2af5-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="c2af5-130">Normalmente, um formulário habilita ou desabilita comandos de menu, dependendo das informações que os sinalizadores fornecem sobre os recursos da implementação do site da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c2af5-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="c2af5-131">Se uma nova mensagem é carregada em um formulário pelo método [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) ou o método [IPersistMessage:: Load](ipersistmessage-load.md) , os sinalizadores de status devem ser verificados.</span><span class="sxs-lookup"><span data-stu-id="c2af5-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="c2af5-132">Alguns objetos do site de mensagens, especialmente objetos somente leitura, não permitem que as mensagens sejam salvas ou excluídas.</span><span class="sxs-lookup"><span data-stu-id="c2af5-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c2af5-133">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="c2af5-133">Notes to implementers</span></span>

<span data-ttu-id="c2af5-134">O método **IMAPIMessageSite:: GetSiteStatus** pode exigir que o aplicativo cliente faça alguns cálculos para determinar quais operações podem ou não ser realizadas na mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="c2af5-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="c2af5-135">Normalmente, isso envolve a análise da linha de status do provedor de repositório de mensagens da mensagem atual ou a consulta do provedor de repositório para determinar quais ações o aplicativo cliente pode executar usando o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c2af5-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="c2af5-136">Por exemplo, para determinar se o sinalizador MAPI_DELETE_IS_MOVE deve ser retornado, verifique a propriedade **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) do objeto do repositório de mensagens para ver se há uma pasta **itens excluídos** no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c2af5-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="c2af5-137">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c2af5-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c2af5-138">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c2af5-138">MFCMAPI reference</span></span>

<span data-ttu-id="c2af5-139">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c2af5-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c2af5-140">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c2af5-140">**File**</span></span>|<span data-ttu-id="c2af5-141">**Função**</span><span class="sxs-lookup"><span data-stu-id="c2af5-141">**Function**</span></span>|<span data-ttu-id="c2af5-142">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="c2af5-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c2af5-143">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="c2af5-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c2af5-144">CMyMAPIFormViewer:: GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="c2af5-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="c2af5-145">MFCMAPI usa o método **IMAPIMessageSite:: GetSiteStatus** para obter o status do site especificado.</span><span class="sxs-lookup"><span data-stu-id="c2af5-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="c2af5-146">Pode retornar VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE ou VCSTATUS_SUBMIT.</span><span class="sxs-lookup"><span data-stu-id="c2af5-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2af5-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2af5-147">See also</span></span>



[<span data-ttu-id="c2af5-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="c2af5-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="c2af5-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="c2af5-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="c2af5-150">Propriedade canônica PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="c2af5-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="c2af5-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2af5-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="c2af5-152">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c2af5-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c2af5-153">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="c2af5-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

