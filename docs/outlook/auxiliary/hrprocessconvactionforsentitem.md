---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Executa a categorização pós-envio em um item de email com base na sua PidTagConversationId.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318897"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="0f8e2-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="0f8e2-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="0f8e2-104">Executa a categorização pós-envio em um item de email com base na sua [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0f8e2-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0f8e2-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="0f8e2-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f8e2-106">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="0f8e2-106">Exported by:</span></span>  <br/> |<span data-ttu-id="0f8e2-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="0f8e2-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="0f8e2-108">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="0f8e2-108">Called by:</span></span>  <br/> |<span data-ttu-id="0f8e2-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="0f8e2-109">Client</span></span>  <br/> |
|<span data-ttu-id="0f8e2-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0f8e2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0f8e2-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="0f8e2-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="0f8e2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f8e2-112">Parameters</span></span>

<span data-ttu-id="0f8e2-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="0f8e2-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="0f8e2-114">[in] [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) do repositório ou [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) do item de email.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-114">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="0f8e2-115">Não pode ser nulo ou inválido.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="0f8e2-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="0f8e2-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="0f8e2-117">[in] [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) do item de email.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-117">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="0f8e2-118">Não pode ser nulo ou inválido.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="0f8e2-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="0f8e2-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="0f8e2-120">[in] [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) do item de email.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-120">[in] The [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="0f8e2-121">Não pode ser nulo ou inválido.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="0f8e2-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="0f8e2-122">_dwFlags_</span></span>
  
> <span data-ttu-id="0f8e2-123">[in] Um bitmask que especifica informações adicionais sobre a chamada do método.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="0f8e2-124">0—Nenhuma opção adicional é usada nesta chamada de método.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="0f8e2-125">Esse é o valor recomendado.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="0f8e2-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ é na verdade o [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="0f8e2-127">Usar **PidTagSearchKey** é um recurso intensivo e deve ser evitado se [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="0f8e2-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0f8e2-128">Return values</span></span>

|<span data-ttu-id="0f8e2-129">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0f8e2-129">**HRESULT**</span></span>|<span data-ttu-id="0f8e2-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0f8e2-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f8e2-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f8e2-131">S_OK</span></span>  <br/> |<span data-ttu-id="0f8e2-132">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="0f8e2-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0f8e2-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="0f8e2-134">_dwFlags_ contém um sinalizador desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f8e2-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f8e2-135">Remarks</span></span>

<span data-ttu-id="0f8e2-136">As categorias são consideradas informações pessoais e não devem ser transmitidas fora da caixa de correio do usuário.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="0f8e2-137">Portanto, não chame **HrProcessConvActionForSentItem** em um item de email não enviado.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="0f8e2-138">Em vez disso, envie o item e, em seguida, chame\*\* HrProcessConvActionForSentItem\*\* na cópia arquivada.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="0f8e2-139">A cópia arquivada pode ser armazenada na pasta Itens enviados ou em um local equivalente.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="0f8e2-140">Seu aplicativo deve estar em processo com o Outlook.exe, como de um suplemento COM, para chamar **HrProcessConvActionForSentItem**.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="0f8e2-141">Se você tentar chamar **HrProcessConvActionForSentItem** fora do processo, **HrProcessConvActionForSentItem** lançará uma exceção de violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="0f8e2-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

