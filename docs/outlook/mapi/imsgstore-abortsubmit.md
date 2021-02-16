---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414379"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="389c7-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="389c7-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="389c7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="389c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="389c7-105">Tenta remover uma mensagem da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="389c7-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="389c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="389c7-106">Parameters</span></span>

 <span data-ttu-id="389c7-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="389c7-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="389c7-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="389c7-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="389c7-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="389c7-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="389c7-110">[in] Um ponteiro para o identificador de entrada da mensagem a ser removido da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="389c7-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="389c7-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="389c7-111">_ulFlags_</span></span>
  
> <span data-ttu-id="389c7-112">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="389c7-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="389c7-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="389c7-113">Return value</span></span>

<span data-ttu-id="389c7-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="389c7-114">S_OK</span></span> 
  
> <span data-ttu-id="389c7-115">A mensagem foi removida com êxito da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="389c7-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="389c7-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="389c7-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="389c7-117">A mensagem identificada por  _lpEntryID_ não está mais na fila de saída do armazenamento de mensagens, normalmente porque ela já foi enviada.</span><span class="sxs-lookup"><span data-stu-id="389c7-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="389c7-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="389c7-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="389c7-119">A mensagem identificada por  _lpEntryID_ é bloqueada pelo spooler MAPI e a operação não pode ser anulada.</span><span class="sxs-lookup"><span data-stu-id="389c7-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="389c7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="389c7-120">Remarks</span></span>

<span data-ttu-id="389c7-121">O **método IMsgStore::AbortSubmit** tenta remover uma mensagem enviada da fila de saída do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="389c7-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="389c7-122">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="389c7-122">Notes to callers</span></span>

<span data-ttu-id="389c7-123">Depois que uma mensagem é enviada, a anulação do envio chamando **AbortSubmit** é a única ação que pode ser executada na mensagem.</span><span class="sxs-lookup"><span data-stu-id="389c7-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="389c7-124">Não espere que **AbortSubmit** seja sempre bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="389c7-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="389c7-125">Dependendo de como o sistema de mensagens subjacente é implementado, talvez não seja possível cancelar o envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="389c7-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="389c7-126">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="389c7-126">MFCMAPI reference</span></span>

<span data-ttu-id="389c7-127">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="389c7-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="389c7-128">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="389c7-128">**File**</span></span>|<span data-ttu-id="389c7-129">**Função**</span><span class="sxs-lookup"><span data-stu-id="389c7-129">**Function**</span></span>|<span data-ttu-id="389c7-130">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="389c7-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="389c7-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="389c7-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="389c7-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="389c7-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="389c7-133">MFCMAPI usa o **método IMsgStore::AbortSubmit** para anular o envio da mensagem selecionada.</span><span class="sxs-lookup"><span data-stu-id="389c7-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="389c7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="389c7-134">See also</span></span>



[<span data-ttu-id="389c7-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="389c7-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="389c7-136">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="389c7-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="389c7-137">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="389c7-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

