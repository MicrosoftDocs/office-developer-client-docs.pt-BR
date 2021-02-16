---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426104"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="07ec8-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="07ec8-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="07ec8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07ec8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07ec8-105">Estabelece um armazenamento de mensagens como o armazenamento de mensagens padrão para a sessão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="07ec8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07ec8-106">Parameters</span></span>

 <span data-ttu-id="07ec8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="07ec8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="07ec8-108">[in] Uma máscara de bits de sinalizadores que controla a configuração do armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="07ec8-109">Esses sinalizadores são mutuamente exclusivos; somente um dos sinalizadores a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="07ec8-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="07ec8-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="07ec8-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="07ec8-111">Estabelece o armazenamento de mensagens como o padrão da sessão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="07ec8-112">Atualiza a linha da tabela de status do armazenamento de mensagens definindo o sinalizador STATUS_DEFAULT_STORE na coluna **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="07ec8-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="07ec8-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="07ec8-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="07ec8-114">Estabelece o armazenamento de mensagens como o armazenamento a ser usado no logon.</span><span class="sxs-lookup"><span data-stu-id="07ec8-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="07ec8-115">Se o armazenamento de mensagens não for o armazenamento padrão, os clientes deverão torná-lo o padrão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="07ec8-116">Atualiza a linha da tabela de status do armazenamento de mensagens definindo o sinalizador STATUS_PRIMARY_STORE na **PR_RESOURCE_FLAGS** coluna.</span><span class="sxs-lookup"><span data-stu-id="07ec8-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="07ec8-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="07ec8-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="07ec8-118">Estabelece o armazenamento de mensagens como o armazenamento a ser usado no logon se o armazenamento de mensagens principal não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="07ec8-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="07ec8-119">Se um cliente não puder abrir o armazenamento principal, ele deverá abrir o armazenamento secundário e defini-lo como padrão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="07ec8-120">Atualiza a linha da tabela de status do armazenamento de mensagens definindo o sinalizador STATUS_SECONDARY_STORE na **PR_RESOURCE_FLAGS** coluna.</span><span class="sxs-lookup"><span data-stu-id="07ec8-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="07ec8-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="07ec8-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="07ec8-122">Define o STATUS_SIMPLE_STORE sinalizador de erro na propriedade **PR_RESOURCE_FLAGS** do armazenamento de mensagens na linha da tabela de status, na linha da tabela do armazenamento de mensagens e no perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="07ec8-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="07ec8-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="07ec8-124">Define o STATUS_SIMPLE_STORE sinalizador de erro  na propriedade PR_RESOURCE_FLAGS do armazenamento de mensagens na linha da tabela de status e na linha da tabela do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="07ec8-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="07ec8-125">O perfil não é modificado.</span><span class="sxs-lookup"><span data-stu-id="07ec8-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="07ec8-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="07ec8-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="07ec8-127">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="07ec8-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="07ec8-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="07ec8-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="07ec8-129">[in] Um ponteiro para o identificador de entrada do armazenamento de mensagens que se destina como padrão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="07ec8-130">Se um cliente passar NULL em  _lpEntryID_, nenhum armazenamento de mensagens será selecionado como padrão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="07ec8-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="07ec8-131">Return value</span></span>

<span data-ttu-id="07ec8-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="07ec8-132">S_OK</span></span> 
  
> <span data-ttu-id="07ec8-133">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="07ec8-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="07ec8-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="07ec8-134">Remarks</span></span>

<span data-ttu-id="07ec8-135">O **método IMAPISession::SetDefaultStore** estabelece um repositório de mensagens como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="07ec8-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="07ec8-136">O armazenamento de mensagens padrão da sessão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="07ec8-137">O armazenamento de mensagens principal da sessão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="07ec8-138">O armazenamento secundário de mensagens da sessão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="07ec8-139">Para estabelecer um repositório de mensagens como padrão, o repositório de mensagens deve ter os seguintes sinalizadores definidos em sua **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) propriedade:</span><span class="sxs-lookup"><span data-stu-id="07ec8-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="07ec8-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="07ec8-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="07ec8-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="07ec8-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="07ec8-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="07ec8-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="07ec8-143">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="07ec8-143">Notes to callers</span></span>

<span data-ttu-id="07ec8-144">Você pode determinar o armazenamento de mensagens padrão para a sessão recuperando a tabela de status e procurando a configuração do sinalizador STATUS_DEFAULT_STORE na **PR_RESOURCE_FLAGS** coluna.</span><span class="sxs-lookup"><span data-stu-id="07ec8-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="07ec8-145">A linha que tem essa configuração representa o armazenamento de mensagens designado como o padrão de sessão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="07ec8-146">Quando o MAPI_DEFAULT_STORE ou o sinalizador MAPI_SIMPLE_STORE_PERMANENT está definido, o MAPI atualiza o perfil, a tabela de armazenamento de mensagens e a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="07ec8-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="07ec8-147">Sempre que uma alteração é feita na configuração padrão do armazenamento de mensagens, as seguintes notificações são geradas:</span><span class="sxs-lookup"><span data-stu-id="07ec8-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="07ec8-148">Uma **notificação de evento fnevTableModified** é emitida para cada linha afetada no armazenamento de mensagens e na tabela de status.</span><span class="sxs-lookup"><span data-stu-id="07ec8-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="07ec8-149">Uma notificação interna é emitida para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="07ec8-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="07ec8-150">As operações já em andamento são concluídas sem alteração; novas operações que envolvem o armazenamento de mensagens padrão, como o download de mensagens, são processadas para o novo armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="07ec8-151">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="07ec8-151">MFCMAPI reference</span></span>

<span data-ttu-id="07ec8-152">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="07ec8-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="07ec8-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="07ec8-153">**File**</span></span>|<span data-ttu-id="07ec8-154">**Função**</span><span class="sxs-lookup"><span data-stu-id="07ec8-154">**Function**</span></span>|<span data-ttu-id="07ec8-155">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="07ec8-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="07ec8-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="07ec8-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="07ec8-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="07ec8-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="07ec8-158">MFCMAPI usa o **método IMAPISession::SetDefaultStore** para definir o repositório selecionado como o repositório padrão.</span><span class="sxs-lookup"><span data-stu-id="07ec8-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07ec8-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="07ec8-159">See also</span></span>



[<span data-ttu-id="07ec8-160">Propriedade canônica PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="07ec8-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="07ec8-161">Propriedade canônica PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="07ec8-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="07ec8-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="07ec8-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="07ec8-163">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="07ec8-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="07ec8-164">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="07ec8-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

