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
ms.openlocfilehash: a176b51577c7d4616d988a0b28f2afcfb554e9f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564980"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="d0537-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="d0537-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="d0537-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0537-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0537-105">Tenta remover uma mensagem da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="d0537-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d0537-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0537-106">Parameters</span></span>

 <span data-ttu-id="d0537-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d0537-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="d0537-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d0537-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d0537-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d0537-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="d0537-110">[in] Um ponteiro para o identificador de entrada da mensagem para remover da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="d0537-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="d0537-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0537-111">_ulFlags_</span></span>
  
> <span data-ttu-id="d0537-112">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d0537-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0537-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d0537-113">Return value</span></span>

<span data-ttu-id="d0537-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0537-114">S_OK</span></span> 
  
> <span data-ttu-id="d0537-115">A mensagem foi removida com êxito da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="d0537-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="d0537-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="d0537-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="d0537-117">A mensagem identificada pela _lpEntryID_ não está mais na fila de saída do armazenamento de mensagens, geralmente porque ele já foi enviado.</span><span class="sxs-lookup"><span data-stu-id="d0537-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="d0537-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="d0537-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="d0537-119">A mensagem identificada pela _lpEntryID_ está bloqueada pelo spooler MAPI e a operação não pode ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="d0537-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d0537-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0537-120">Remarks</span></span>

<span data-ttu-id="d0537-121">O método **IMsgStore::AbortSubmit** tenta remover uma mensagem enviada de fila de saída do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d0537-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d0537-122">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d0537-122">Notes to callers</span></span>

<span data-ttu-id="d0537-123">Depois que uma mensagem é enviada, anular o envio chamando **AbortSubmit** é a única ação que pode ser executada na mensagem.</span><span class="sxs-lookup"><span data-stu-id="d0537-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="d0537-124">Não espera **AbortSubmit** sempre ter sucesso.</span><span class="sxs-lookup"><span data-stu-id="d0537-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="d0537-125">Dependendo de como o sistema de mensagens subjacente é implementado, talvez não seja possível cancelar o envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d0537-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d0537-126">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d0537-126">MFCMAPI reference</span></span>

<span data-ttu-id="d0537-127">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0537-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d0537-128">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d0537-128">**File**</span></span>|<span data-ttu-id="d0537-129">**Function**</span><span class="sxs-lookup"><span data-stu-id="d0537-129">**Function**</span></span>|<span data-ttu-id="d0537-130">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d0537-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0537-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d0537-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="d0537-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="d0537-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="d0537-133">MFCMAPI usa o método **IMsgStore::AbortSubmit** anular o envio da mensagem selecionada.</span><span class="sxs-lookup"><span data-stu-id="d0537-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0537-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0537-134">See also</span></span>



[<span data-ttu-id="d0537-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d0537-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="d0537-136">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d0537-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="d0537-137">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d0537-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

