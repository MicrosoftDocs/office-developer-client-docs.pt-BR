---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Executa pós-enviar categorização em um item de email com base em sua PidTagConversationId.
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765823"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="d87fd-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="d87fd-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="d87fd-104">Executa pós-enviar categorização em um item de email com base em suas [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d87fd-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d87fd-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d87fd-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d87fd-106">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="d87fd-106">Exported by:</span></span>  <br/> |<span data-ttu-id="d87fd-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="d87fd-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="d87fd-108">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="d87fd-108">Called by:</span></span>  <br/> |<span data-ttu-id="d87fd-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="d87fd-109">Client</span></span>  <br/> |
|<span data-ttu-id="d87fd-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="d87fd-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d87fd-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="d87fd-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="d87fd-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d87fd-112">Parameters</span></span>

<span data-ttu-id="d87fd-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="d87fd-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="d87fd-114">[in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) do repositório ou o [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) do item de email.</span><span class="sxs-lookup"><span data-stu-id="d87fd-114">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="d87fd-115">Não pode ser NULL ou inválidas.</span><span class="sxs-lookup"><span data-stu-id="d87fd-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="d87fd-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="d87fd-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="d87fd-117">[in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) do item de email.</span><span class="sxs-lookup"><span data-stu-id="d87fd-117">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="d87fd-118">Não pode ser NULL ou inválidas.</span><span class="sxs-lookup"><span data-stu-id="d87fd-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="d87fd-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="d87fd-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="d87fd-120">[in] [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) do item de email.</span><span class="sxs-lookup"><span data-stu-id="d87fd-120">[in] The [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="d87fd-121">Não pode ser NULL ou inválidas.</span><span class="sxs-lookup"><span data-stu-id="d87fd-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="d87fd-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="d87fd-122">_dwFlags_</span></span>
  
> <span data-ttu-id="d87fd-123">[in] Uma máscara de bits que especifica informações adicionais sobre a chamada de método.</span><span class="sxs-lookup"><span data-stu-id="d87fd-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="d87fd-124">0 – há opções adicionais são usadas nessa chamada de método.</span><span class="sxs-lookup"><span data-stu-id="d87fd-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="d87fd-125">Este é o valor recomendado.</span><span class="sxs-lookup"><span data-stu-id="d87fd-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="d87fd-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ é realmente o [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d87fd-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="d87fd-127">Usando um **PidTagSearchKey** faz uso de recursos e deve ser evitado se um [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="d87fd-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d87fd-128">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="d87fd-128">Return values</span></span>

|<span data-ttu-id="d87fd-129">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d87fd-129">**HRESULT**</span></span>|<span data-ttu-id="d87fd-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d87fd-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d87fd-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="d87fd-131">S_OK</span></span>  <br/> |<span data-ttu-id="d87fd-132">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d87fd-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="d87fd-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d87fd-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="d87fd-134">_dwFlags_ contém um sinalizador desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d87fd-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d87fd-135">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="d87fd-135">Remarks</span></span>

<span data-ttu-id="d87fd-136">Categorias são consideradas informações pessoais e não devem ser transmitidas fora da caixa de correio do usuário.</span><span class="sxs-lookup"><span data-stu-id="d87fd-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="d87fd-137">Portanto, não chame **HrProcessConvActionForSentItem** em um item de email não enviados.</span><span class="sxs-lookup"><span data-stu-id="d87fd-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="d87fd-138">Em vez disso, enviar o item e, em seguida, chame **HrProcessConvActionForSentItem** na cópia arquivada.</span><span class="sxs-lookup"><span data-stu-id="d87fd-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="d87fd-139">A cópia arquivada pode ser armazenada na pasta Itens enviados, ou um local equivalente.</span><span class="sxs-lookup"><span data-stu-id="d87fd-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="d87fd-140">Seu aplicativo deve ser em processo com Outlook.exe, tais como um suplemento COM, chamar **HrProcessConvActionForSentItem**.</span><span class="sxs-lookup"><span data-stu-id="d87fd-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="d87fd-141">Se você tentar chamar fora do processo **HrProcessConvActionForSentItem** , **HrProcessConvActionForSentItem** lançará uma exceção de violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="d87fd-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

