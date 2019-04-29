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
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="a9ffb-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="a9ffb-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="a9ffb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9ffb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9ffb-105">Exclui uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a9ffb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9ffb-106">Parameters</span></span>

 <span data-ttu-id="a9ffb-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="a9ffb-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="a9ffb-108">no Um ponteiro para uma [](entrylist.md) estrutura ENTRYLIST que contém o número de mensagens a serem excluídas e uma matriz de estruturas [EntryID](entryid.md) que identificam as mensagens.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="a9ffb-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a9ffb-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="a9ffb-110">no Uma alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="a9ffb-111">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="a9ffb-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a9ffb-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a9ffb-112">_lpProgress_</span></span>
  
> <span data-ttu-id="a9ffb-113">no Um ponteiro para um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a9ffb-114">Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="a9ffb-115">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="a9ffb-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a9ffb-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a9ffb-116">_ulFlags_</span></span>
  
> <span data-ttu-id="a9ffb-117">no Uma bitmask de sinalizadores que controlam como as mensagens são excluídas.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="a9ffb-118">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a9ffb-118">The following flags can be set:</span></span>
    
<span data-ttu-id="a9ffb-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="a9ffb-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="a9ffb-120">Remove permanentemente todas as mensagens, incluindo as excluídas de forma reversível.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="a9ffb-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a9ffb-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="a9ffb-122">Exibe um indicador de progresso à medida que a operação prossegue.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a9ffb-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a9ffb-123">Return value</span></span>

<span data-ttu-id="a9ffb-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9ffb-124">S_OK</span></span> 
  
> <span data-ttu-id="a9ffb-125">A mensagem ou mensagens especificadas foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="a9ffb-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a9ffb-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="a9ffb-127">A chamada teve êxito, mas nem todas as mensagens foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="a9ffb-128">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a9ffb-129">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="a9ffb-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a9ffb-130">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a9ffb-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9ffb-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9ffb-131">Remarks</span></span>

<span data-ttu-id="a9ffb-132">O método **IMAPIFolder::D eletemessages** exclui mensagens de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="a9ffb-133">As mensagens que não existem, que foram movidas em outro lugar, que estão abertas com permissão de leitura/gravação ou não podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a9ffb-134">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="a9ffb-134">Notes to implementers</span></span>

<span data-ttu-id="a9ffb-135">Quando a operação de exclusão envolve mais de uma mensagem, execute a operação o mais completo possível para cada pasta, mesmo que uma ou mais das mensagens não possam ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="a9ffb-136">Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do seu controle, como a falta de memória, ficando sem espaço em disco ou corrupção no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a9ffb-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a9ffb-137">Notes to callers</span></span>

<span data-ttu-id="a9ffb-138">Espere estes valores de retorno sob as condições a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="a9ffb-139">**Condition**</span><span class="sxs-lookup"><span data-stu-id="a9ffb-139">**Condition**</span></span>|<span data-ttu-id="a9ffb-140">**Valor de retorno**</span><span class="sxs-lookup"><span data-stu-id="a9ffb-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a9ffb-141">O **DeleteMessages** excluiu com êxito todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="a9ffb-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9ffb-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="a9ffb-143">O **DeleteMessages** não pôde excluir com êxito todas as mensagens e subpastas.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="a9ffb-144">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a9ffb-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="a9ffb-145">**DeleteMessages** não pôde ser concluída.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="a9ffb-146">Qualquer valor de erro, exceto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a9ffb-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="a9ffb-147">Quando o **DeleteMessages** não puder ser concluído, não presuma que nenhum trabalho foi realizado.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="a9ffb-148">O **DeleteMessages** pode ter sido capaz de excluir uma ou mais mensagens antes de encontrar o erro.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="a9ffb-149">**DeleteMessages** retorna MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, dependendo da implementação do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a9ffb-150">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a9ffb-150">MFCMAPI reference</span></span>

<span data-ttu-id="a9ffb-151">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a9ffb-152">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a9ffb-152">**File**</span></span>|<span data-ttu-id="a9ffb-153">**Função**</span><span class="sxs-lookup"><span data-stu-id="a9ffb-153">**Function**</span></span>|<span data-ttu-id="a9ffb-154">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="a9ffb-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a9ffb-155">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="a9ffb-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="a9ffb-156">CFolderDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="a9ffb-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="a9ffb-157">MFCMAPI usa o método **IMAPIFolder::D eletemessages** para excluir as mensagens especificadas.</span><span class="sxs-lookup"><span data-stu-id="a9ffb-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9ffb-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9ffb-158">See also</span></span>



[<span data-ttu-id="a9ffb-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a9ffb-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="a9ffb-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="a9ffb-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="a9ffb-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a9ffb-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="a9ffb-162">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a9ffb-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a9ffb-163">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="a9ffb-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

