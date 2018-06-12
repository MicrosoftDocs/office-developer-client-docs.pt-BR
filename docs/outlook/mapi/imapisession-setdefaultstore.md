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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e3c4125bf4fcf1881a0cba9b04a8bb6aa71f527d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767192"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="ce02f-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="ce02f-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="ce02f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce02f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce02f-105">Estabelece um armazenamento de mensagens como o armazenamento de mensagens padrão para a sessão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ce02f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ce02f-106">Parameters</span></span>

 <span data-ttu-id="ce02f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce02f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ce02f-108">[in] Uma bitmask dos sinalizadores que controla a configuração de armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="ce02f-109">Esses sinalizadores são mutuamente exclusivos; pode ser definido somente um dos sinalizadores a seguir:</span><span class="sxs-lookup"><span data-stu-id="ce02f-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="ce02f-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="ce02f-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="ce02f-111">Estabelece o armazenamento de mensagens como o padrão de sessão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="ce02f-112">Atualiza a linha de tabela de status do armazenamento de mensagens, definindo o sinalizador STATUS_DEFAULT_STORE na coluna **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ce02f-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="ce02f-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="ce02f-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="ce02f-114">Estabelece o armazenamento de mensagens como o armazenamento a ser usado durante o logon.</span><span class="sxs-lookup"><span data-stu-id="ce02f-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="ce02f-115">Se o armazenamento de mensagens não for o repositório padrão, os clientes devem facilitam o padrão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="ce02f-116">Atualiza a linha de tabela de status do armazenamento de mensagens, definindo o sinalizador STATUS_PRIMARY_STORE na coluna **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="ce02f-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="ce02f-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="ce02f-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="ce02f-118">Estabelece o armazenamento de mensagens como o armazenamento a ser usado no logon se o armazenamento de mensagens principal não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="ce02f-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="ce02f-119">Se um cliente não é possível abrir o repositório principal, ele deverá abrir o armazenamento secundário e defini-la como padrão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="ce02f-120">Atualiza a linha de tabela de status do armazenamento de mensagens, definindo o sinalizador STATUS_SECONDARY_STORE na coluna **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="ce02f-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="ce02f-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="ce02f-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="ce02f-122">Define o sinalizador STATUS_SIMPLE_STORE na propriedade **PR_RESOURCE_FLAGS** do armazenamento de mensagens em sua linha de tabela de status, linha de tabela do repositório de mensagem e em perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="ce02f-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="ce02f-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="ce02f-124">Define o sinalizador STATUS_SIMPLE_STORE na propriedade **PR_RESOURCE_FLAGS** do armazenamento de mensagens em sua linha da tabela de status e a linha de tabela do repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ce02f-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="ce02f-125">O perfil não é modificado.</span><span class="sxs-lookup"><span data-stu-id="ce02f-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="ce02f-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ce02f-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="ce02f-127">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="ce02f-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ce02f-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ce02f-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="ce02f-129">[in] Um ponteiro para o identificador de entrada do repositório de mensagem que serve como o padrão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="ce02f-130">Se um cliente transmite NULL no _lpEntryID_, sem armazenamento de mensagens está selecionado como o padrão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce02f-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ce02f-131">Return value</span></span>

<span data-ttu-id="ce02f-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce02f-132">S_OK</span></span> 
  
> <span data-ttu-id="ce02f-133">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="ce02f-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce02f-134">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ce02f-134">Remarks</span></span>

<span data-ttu-id="ce02f-135">O método **IMAPISession::SetDefaultStore** estabelece um armazenamento de mensagens como um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="ce02f-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="ce02f-136">O repositório de mensagem padrão para a sessão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="ce02f-137">O repositório de mensagens principal para a sessão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="ce02f-138">O armazenamento de mensagens secundário para a sessão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="ce02f-139">Para estabelecer um armazenamento de mensagens como padrão, o armazenamento de mensagens deve ter os seguintes sinalizadores definidos em sua propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):</span><span class="sxs-lookup"><span data-stu-id="ce02f-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="ce02f-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="ce02f-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="ce02f-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="ce02f-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="ce02f-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="ce02f-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="ce02f-143">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ce02f-143">Notes to callers</span></span>

<span data-ttu-id="ce02f-144">Você pode determinar o armazenamento de mensagens padrão para a sessão Recuperando a tabela de status e a pesquisa para que a configuração do sinalizador STATUS_DEFAULT_STORE na coluna **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="ce02f-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="ce02f-145">Na linha que tem essa configuração representa o armazenamento de mensagens é designado como o padrão de sessão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="ce02f-146">Quando o MAPI_DEFAULT_STORE ou o sinalizador MAPI_SIMPLE_STORE_PERMANENT estiver definido, o MAPI atualiza o perfil, a tabela de repositório de mensagens e a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="ce02f-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="ce02f-147">Sempre que for feita uma alteração para a configuração de padrão do repositório de mensagem, as seguintes notificações são geradas:</span><span class="sxs-lookup"><span data-stu-id="ce02f-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="ce02f-148">Uma notificação de evento **fnevTableModified** é emitida para cada linha afetada em ambos os tabela de status e o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ce02f-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="ce02f-149">Uma notificação interna é emitida para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce02f-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="ce02f-150">Operações em andamento podem ser concluídas sem alteração; novas operações que envolvem o armazenamento de mensagens padrão, como mensagem Baixando os dados, são processadas para o novo repositório padrão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ce02f-151">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ce02f-151">MFCMAPI reference</span></span>

<span data-ttu-id="ce02f-152">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce02f-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ce02f-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ce02f-153">**File**</span></span>|<span data-ttu-id="ce02f-154">**Function**</span><span class="sxs-lookup"><span data-stu-id="ce02f-154">**Function**</span></span>|<span data-ttu-id="ce02f-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ce02f-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce02f-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ce02f-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="ce02f-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="ce02f-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="ce02f-158">MFCMAPI usa o método **IMAPISession::SetDefaultStore** para definir o repositório selecionado como o armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="ce02f-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce02f-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce02f-159">See also</span></span>



[<span data-ttu-id="ce02f-160">Propriedade canônico de PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="ce02f-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="ce02f-161">Propriedade canônico de PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="ce02f-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="ce02f-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ce02f-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="ce02f-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce02f-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="ce02f-164">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ce02f-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

