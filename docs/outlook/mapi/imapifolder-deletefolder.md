---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 02815c60b6bfc9809871af19e922913622588fc9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584313"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="66f7a-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="66f7a-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="66f7a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66f7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66f7a-105">Exclui uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="66f7a-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="66f7a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66f7a-106">Parameters</span></span>

 <span data-ttu-id="66f7a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="66f7a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="66f7a-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="66f7a-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="66f7a-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="66f7a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="66f7a-110">[in] Um ponteiro para o identificador de entrada da subpasta para excluir.</span><span class="sxs-lookup"><span data-stu-id="66f7a-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="66f7a-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="66f7a-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="66f7a-112">[in] Um identificador para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="66f7a-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="66f7a-113">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="66f7a-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="66f7a-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="66f7a-114">_lpProgress_</span></span>
  
> <span data-ttu-id="66f7a-115">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="66f7a-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="66f7a-116">Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="66f7a-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="66f7a-117">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG está definido na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="66f7a-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="66f7a-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="66f7a-118">_ulFlags_</span></span>
  
> <span data-ttu-id="66f7a-119">[in] Uma bitmask dos sinalizadores que controla a exclusão da subpasta.</span><span class="sxs-lookup"><span data-stu-id="66f7a-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="66f7a-120">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="66f7a-120">The following flags can be set:</span></span>
    
<span data-ttu-id="66f7a-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="66f7a-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="66f7a-122">Todas as subpastas da subpasta apontado pela _lpEntryID_ devem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="66f7a-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="66f7a-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="66f7a-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="66f7a-124">Todas as mensagens na subpasta apontado pela _lpEntryID_ devem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="66f7a-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="66f7a-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="66f7a-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="66f7a-126">Um indicador de progresso deve ser exibido enquanto continua a operação.</span><span class="sxs-lookup"><span data-stu-id="66f7a-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="66f7a-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="66f7a-127">Return value</span></span>

<span data-ttu-id="66f7a-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="66f7a-128">S_OK</span></span> 
  
> <span data-ttu-id="66f7a-129">A pasta especificada foi excluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="66f7a-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="66f7a-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="66f7a-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="66f7a-131">A subpasta que está sendo excluída contém subpastas e o sinalizador DEL_FOLDERS não foi definido.</span><span class="sxs-lookup"><span data-stu-id="66f7a-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="66f7a-132">As subpastas não foram excluídas.</span><span class="sxs-lookup"><span data-stu-id="66f7a-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="66f7a-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="66f7a-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="66f7a-134">A subpasta que está sendo excluída contém mensagens e o sinalizador DEL_MESSAGES não foi definido.</span><span class="sxs-lookup"><span data-stu-id="66f7a-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="66f7a-135">A subpasta não foi excluída.</span><span class="sxs-lookup"><span data-stu-id="66f7a-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="66f7a-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="66f7a-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="66f7a-137">A chamada foi bem-sucedida, mas nem todas as entradas foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="66f7a-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="66f7a-138">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="66f7a-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="66f7a-139">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="66f7a-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="66f7a-140">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="66f7a-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66f7a-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="66f7a-141">Remarks</span></span>

<span data-ttu-id="66f7a-142">O método **IMAPIFolder::DeleteFolder** exclui uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="66f7a-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="66f7a-143">Por padrão, **DeleteFolder** opera somente em pastas vazias, mas você pode usá-lo com êxito em pastas não vazias definindo dois sinalizadores: DEL_FOLDERS e DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="66f7a-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="66f7a-144">Apenas pastas vazias ou pastas que definir sinalizadores DEL_FOLDERS tanto o DEL_MESSAGES na chamada **DeleteFolder** podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="66f7a-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="66f7a-145">DEL_FOLDERS habilita todas as subpastas da pasta a ser removida; DEL_MESSAGES habilita todas as mensagens da pasta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="66f7a-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="66f7a-146">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="66f7a-146">Notes to implementers</span></span>

<span data-ttu-id="66f7a-147">Quando a operação de exclusão envolve mais de uma pasta, execute a operação como completamente para cada pasta.</span><span class="sxs-lookup"><span data-stu-id="66f7a-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="66f7a-148">Em alguns casos, uma das pastas a ser excluído não existe ou foi movida ou copiada em outro local.</span><span class="sxs-lookup"><span data-stu-id="66f7a-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="66f7a-149">Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="66f7a-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="66f7a-150">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="66f7a-150">Notes to callers</span></span>

<span data-ttu-id="66f7a-151">Espera esses valores de retorno sob as condições a seguintes.</span><span class="sxs-lookup"><span data-stu-id="66f7a-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="66f7a-152">**Condição**</span><span class="sxs-lookup"><span data-stu-id="66f7a-152">**Condition**</span></span>|<span data-ttu-id="66f7a-153">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="66f7a-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66f7a-154">**DeleteFolder** excluiu com êxito cada mensagem e a subpasta.</span><span class="sxs-lookup"><span data-stu-id="66f7a-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="66f7a-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="66f7a-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="66f7a-156">**DeleteFolder** não pôde ser excluído com êxito a cada mensagem e a subpasta.</span><span class="sxs-lookup"><span data-stu-id="66f7a-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="66f7a-157">MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="66f7a-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="66f7a-158">**DeleteFolder** não pôde concluir.</span><span class="sxs-lookup"><span data-stu-id="66f7a-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="66f7a-159">Qualquer valor de erro, exceto E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="66f7a-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="66f7a-160">Quando **DeleteFolder** é impossível concluir, não presuma que foi feito nenhum trabalho.</span><span class="sxs-lookup"><span data-stu-id="66f7a-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="66f7a-161">**DeleteFolder** podem ter sido capazes de excluir uma ou mais das mensagens e subpastas antes da ocorrência de erro.</span><span class="sxs-lookup"><span data-stu-id="66f7a-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="66f7a-162">Se uma ou mais subpastas não podem ser excluídas, **DeleteFolder** retorna MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND, dependendo da implementação do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="66f7a-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="66f7a-163">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="66f7a-163">MFCMAPI reference</span></span>

<span data-ttu-id="66f7a-164">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="66f7a-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="66f7a-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="66f7a-165">**File**</span></span>|<span data-ttu-id="66f7a-166">**Function**</span><span class="sxs-lookup"><span data-stu-id="66f7a-166">**Function**</span></span>|<span data-ttu-id="66f7a-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="66f7a-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="66f7a-168">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="66f7a-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="66f7a-169">CMsgStoreDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="66f7a-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="66f7a-170">MFCMAPI usa o método **IMAPIFolder::DeleteFolder** para excluir pastas.</span><span class="sxs-lookup"><span data-stu-id="66f7a-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66f7a-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="66f7a-171">See also</span></span>



[<span data-ttu-id="66f7a-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="66f7a-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="66f7a-173">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="66f7a-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

