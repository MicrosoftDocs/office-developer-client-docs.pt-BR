---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426069"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="dc20e-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="dc20e-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="dc20e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc20e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc20e-105">Exclui uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc20e-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dc20e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc20e-106">Parameters</span></span>

 <span data-ttu-id="dc20e-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="dc20e-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="dc20e-108">[in] Um ponteiro para uma [estrutura ENTRYLIST](entrylist.md) que contém o número de mensagens a excluir e uma matriz de estruturas [ENTRYID](entryid.md) que identificam as mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc20e-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="dc20e-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="dc20e-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="dc20e-110">[in] Um alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="dc20e-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="dc20e-111">O _parâmetro ulUIParam é_ ignorado, a menos que o MESSAGE_DIALOG padrão seja definido no parâmetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="dc20e-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="dc20e-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="dc20e-112">_lpProgress_</span></span>
  
> <span data-ttu-id="dc20e-113">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="dc20e-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="dc20e-114">Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="dc20e-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="dc20e-115">O _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG seja definido no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="dc20e-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="dc20e-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dc20e-116">_ulFlags_</span></span>
  
> <span data-ttu-id="dc20e-117">[in] Uma máscara de bits de sinalizadores que controla como as mensagens são excluídas.</span><span class="sxs-lookup"><span data-stu-id="dc20e-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="dc20e-118">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="dc20e-118">The following flags can be set:</span></span>
    
<span data-ttu-id="dc20e-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="dc20e-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="dc20e-120">Remove permanentemente todas as mensagens, incluindo as excluídas de forma suave.</span><span class="sxs-lookup"><span data-stu-id="dc20e-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="dc20e-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="dc20e-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="dc20e-122">Exibe um indicador de progresso à medida que a operação prosse segue.</span><span class="sxs-lookup"><span data-stu-id="dc20e-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dc20e-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dc20e-123">Return value</span></span>

<span data-ttu-id="dc20e-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc20e-124">S_OK</span></span> 
  
> <span data-ttu-id="dc20e-125">A mensagem ou mensagens especificadas foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="dc20e-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="dc20e-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="dc20e-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="dc20e-127">A chamada foi bem-sucedida, mas nem todas as mensagens foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="dc20e-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="dc20e-128">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dc20e-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="dc20e-129">Para testar esse aviso, use a **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="dc20e-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="dc20e-130">Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="dc20e-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc20e-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc20e-131">Remarks</span></span>

<span data-ttu-id="dc20e-132">O **método IMAPIFolder::D eleteMessages** exclui mensagens de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="dc20e-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="dc20e-133">Mensagens que não existem, que foram movidas para outro lugar, abertas com permissão de leitura/gravação ou que estão enviadas atualmente não podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="dc20e-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dc20e-134">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="dc20e-134">Notes to implementers</span></span>

<span data-ttu-id="dc20e-135">Quando a operação de exclusão envolver mais de uma mensagem, execute a operação o mais completamente possível para cada pasta, mesmo se uma ou mais das mensagens não puderem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="dc20e-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="dc20e-136">Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do controle, como falta de memória, falta de espaço em disco ou corrupção no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc20e-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="dc20e-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="dc20e-137">Notes to callers</span></span>

<span data-ttu-id="dc20e-138">Espere esses valores de retorno sob as seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="dc20e-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="dc20e-139">**Condition**</span><span class="sxs-lookup"><span data-stu-id="dc20e-139">**Condition**</span></span>|<span data-ttu-id="dc20e-140">**Valor de retorno**</span><span class="sxs-lookup"><span data-stu-id="dc20e-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc20e-141">**DeleteMessages** excluiu todas as mensagens com êxito.</span><span class="sxs-lookup"><span data-stu-id="dc20e-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="dc20e-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc20e-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="dc20e-143">**DeleteMessages** não pôde excluir todas as mensagens e subpastas com êxito.</span><span class="sxs-lookup"><span data-stu-id="dc20e-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="dc20e-144">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dc20e-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="dc20e-145">**DeleteMessages** não pôde ser concluído.</span><span class="sxs-lookup"><span data-stu-id="dc20e-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="dc20e-146">Qualquer valor de erro, exceto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dc20e-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="dc20e-147">Quando **DeleteMessages** não puder ser concluído, não suponha que nenhum trabalho foi feito.</span><span class="sxs-lookup"><span data-stu-id="dc20e-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="dc20e-148">**DeleteMessages** pode ter sido capaz de excluir uma ou mais das mensagens antes de encontrar o erro.</span><span class="sxs-lookup"><span data-stu-id="dc20e-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="dc20e-149">**DeleteMessages** retorna MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, dependendo da implementação do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc20e-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dc20e-150">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dc20e-150">MFCMAPI reference</span></span>

<span data-ttu-id="dc20e-151">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc20e-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dc20e-152">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="dc20e-152">**File**</span></span>|<span data-ttu-id="dc20e-153">**Função**</span><span class="sxs-lookup"><span data-stu-id="dc20e-153">**Function**</span></span>|<span data-ttu-id="dc20e-154">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="dc20e-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc20e-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dc20e-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="dc20e-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="dc20e-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="dc20e-157">MFCMAPI usa o **método IMAPIFolder::D eleteMessages** para excluir as mensagens especificadas.</span><span class="sxs-lookup"><span data-stu-id="dc20e-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc20e-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc20e-158">See also</span></span>



[<span data-ttu-id="dc20e-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="dc20e-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="dc20e-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="dc20e-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="dc20e-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="dc20e-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="dc20e-162">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="dc20e-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="dc20e-163">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="dc20e-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

