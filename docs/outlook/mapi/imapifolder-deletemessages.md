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
ms.openlocfilehash: 7845abc4f3010daf8e13d56ac4b13d0333bad07e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766983"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="a3553-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="a3553-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="a3553-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3553-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3553-105">Exclui uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="a3553-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a3553-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3553-106">Parameters</span></span>

 <span data-ttu-id="a3553-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="a3553-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="a3553-108">[in] Um ponteiro para uma estrutura [ENTRYLIST](entrylist.md) que contém o número de mensagens para excluir e uma matriz de estruturas [ENTRYID](entryid.md) que identificam as mensagens.</span><span class="sxs-lookup"><span data-stu-id="a3553-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="a3553-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a3553-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="a3553-110">[in] Um identificador para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="a3553-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="a3553-111">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a3553-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a3553-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a3553-112">_lpProgress_</span></span>
  
> <span data-ttu-id="a3553-113">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="a3553-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a3553-114">Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="a3553-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="a3553-115">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a3553-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a3553-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3553-116">_ulFlags_</span></span>
  
> <span data-ttu-id="a3553-117">[in] Uma bitmask dos sinalizadores que controla como as mensagens são excluídas.</span><span class="sxs-lookup"><span data-stu-id="a3553-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="a3553-118">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a3553-118">The following flags can be set:</span></span>
    
<span data-ttu-id="a3553-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="a3553-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="a3553-120">Remove permanentemente todas as mensagens, incluindo aquelas excluída.</span><span class="sxs-lookup"><span data-stu-id="a3553-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="a3553-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a3553-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="a3553-122">Exibe um indicador de progresso conforme continua a operação.</span><span class="sxs-lookup"><span data-stu-id="a3553-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3553-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a3553-123">Return value</span></span>

<span data-ttu-id="a3553-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3553-124">S_OK</span></span> 
  
> <span data-ttu-id="a3553-125">A mensagem especificada ou mensagens foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="a3553-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="a3553-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a3553-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="a3553-127">A chamada foi bem-sucedida, mas nem todas as mensagens foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="a3553-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="a3553-128">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="a3553-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a3553-129">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="a3553-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a3553-130">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a3553-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3553-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3553-131">Remarks</span></span>

<span data-ttu-id="a3553-132">O método **IMAPIFolder::DeleteMessages** exclui mensagens de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="a3553-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="a3553-133">Mensagens que não existem, que foram movidos em outro lugar, que estão abertos com permissão de leitura/gravação ou que são enviados atualmente não podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="a3553-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a3553-134">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="a3553-134">Notes to implementers</span></span>

<span data-ttu-id="a3553-135">Quando a operação de exclusão envolve mais de uma mensagem, execute a operação como completamente para cada pasta, mesmo se um ou mais das mensagens não podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="a3553-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="a3553-136">Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a3553-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3553-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a3553-137">Notes to callers</span></span>

<span data-ttu-id="a3553-138">Espera esses valores de retorno sob as condições a seguintes.</span><span class="sxs-lookup"><span data-stu-id="a3553-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="a3553-139">**Condição**</span><span class="sxs-lookup"><span data-stu-id="a3553-139">**Condition**</span></span>|<span data-ttu-id="a3553-140">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="a3553-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3553-141">**DeleteMessages** excluiu com êxito a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="a3553-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="a3553-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3553-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="a3553-143">**DeleteMessages** não pôde ser excluído com êxito a cada mensagem e a subpasta.</span><span class="sxs-lookup"><span data-stu-id="a3553-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="a3553-144">MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a3553-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="a3553-145">**DeleteMessages** não pôde concluir.</span><span class="sxs-lookup"><span data-stu-id="a3553-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="a3553-146">Qualquer valor de erro, exceto E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a3553-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="a3553-147">Quando **DeleteMessages** é impossível concluir, não presuma que foi feito nenhum trabalho.</span><span class="sxs-lookup"><span data-stu-id="a3553-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="a3553-148">**DeleteMessages** podem ter sido capaz de excluir uma ou mais das mensagens antes da ocorrência de erro.</span><span class="sxs-lookup"><span data-stu-id="a3553-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="a3553-149">**DeleteMessages** retorna MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND, dependendo da implementação do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a3553-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a3553-150">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a3553-150">MFCMAPI reference</span></span>

<span data-ttu-id="a3553-151">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3553-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a3553-152">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a3553-152">**File**</span></span>|<span data-ttu-id="a3553-153">**Function**</span><span class="sxs-lookup"><span data-stu-id="a3553-153">**Function**</span></span>|<span data-ttu-id="a3553-154">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a3553-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a3553-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a3553-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="a3553-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="a3553-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="a3553-157">MFCMAPI usa o método **IMAPIFolder::DeleteMessages** para excluir as mensagens especificadas.</span><span class="sxs-lookup"><span data-stu-id="a3553-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3553-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3553-158">See also</span></span>



[<span data-ttu-id="a3553-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a3553-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="a3553-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="a3553-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="a3553-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a3553-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="a3553-162">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a3553-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a3553-163">Usar macros para lidar com erros</span><span class="sxs-lookup"><span data-stu-id="a3553-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

