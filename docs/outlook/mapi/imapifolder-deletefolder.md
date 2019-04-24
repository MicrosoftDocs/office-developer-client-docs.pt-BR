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
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280068"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="f7c8f-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="f7c8f-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="f7c8f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7c8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7c8f-105">Exclui uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f7c8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7c8f-106">Parameters</span></span>

 <span data-ttu-id="f7c8f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f7c8f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f7c8f-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f7c8f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f7c8f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f7c8f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f7c8f-110">no Um ponteiro para o identificador de entrada da subpasta a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="f7c8f-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f7c8f-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="f7c8f-112">no Uma alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="f7c8f-113">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="f7c8f-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f7c8f-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="f7c8f-114">_lpProgress_</span></span>
  
> <span data-ttu-id="f7c8f-115">no Um ponteiro para um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="f7c8f-116">Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="f7c8f-117">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido em _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="f7c8f-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7c8f-118">_ulFlags_</span></span>
  
> <span data-ttu-id="f7c8f-119">no Uma bitmask de sinalizadores que controla a exclusão da subpasta.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="f7c8f-120">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f7c8f-120">The following flags can be set:</span></span>
    
<span data-ttu-id="f7c8f-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="f7c8f-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="f7c8f-122">Todas as subpastas da subpasta indicada por _lpEntryID_ devem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="f7c8f-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="f7c8f-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="f7c8f-124">Todas as mensagens na subpasta indicada por _lpEntryID_ devem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="f7c8f-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f7c8f-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="f7c8f-126">Um indicador de progresso deve ser exibido enquanto a operação prossegue.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7c8f-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f7c8f-127">Return value</span></span>

<span data-ttu-id="f7c8f-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7c8f-128">S_OK</span></span> 
  
> <span data-ttu-id="f7c8f-129">A pasta especificada foi excluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="f7c8f-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="f7c8f-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="f7c8f-131">A subpasta que está sendo excluída contém subpastas e o sinalizador DEL_FOLDERS não foi definido.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="f7c8f-132">As subpastas não foram excluídas.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="f7c8f-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="f7c8f-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="f7c8f-134">A subpasta que está sendo excluída contém mensagens e o sinalizador DEL_MESSAGES não foi definido.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="f7c8f-135">A subpasta não foi excluída.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="f7c8f-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="f7c8f-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="f7c8f-137">A chamada teve êxito, mas nem todas as entradas foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="f7c8f-138">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="f7c8f-139">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="f7c8f-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f7c8f-140">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="f7c8f-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7c8f-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7c8f-141">Remarks</span></span>

<span data-ttu-id="f7c8f-142">O método **IMAPIFolder::D eletefolder** exclui uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="f7c8f-143">Por padrão, o **DeleteFolder** funciona apenas em pastas vazias, mas você pode usá-lo com êxito em pastas não vazias Configurando dois sinalizadores: DEL_FOLDERS e DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="f7c8f-144">Somente pastas vazias ou pastas que definem os sinalizadores DEL_FOLDERS e DEL_MESSAGES na chamada **DeleteFolder** podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="f7c8f-145">O DEL_FOLDERS permite que todas as subpastas da pasta sejam removidas; DEL_MESSAGES habilita todas as mensagens da pasta a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f7c8f-146">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="f7c8f-146">Notes to implementers</span></span>

<span data-ttu-id="f7c8f-147">Quando a operação de exclusão envolver mais de uma pasta, execute a operação o mais completo possível para cada pasta.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="f7c8f-148">Às vezes, uma das pastas a serem excluídas não existe ou foi movida ou copiada em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="f7c8f-149">Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do seu controle, como a falta de memória, ficando sem espaço em disco ou corrupção no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f7c8f-150">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f7c8f-150">Notes to callers</span></span>

<span data-ttu-id="f7c8f-151">Espere estes valores de retorno sob as condições a seguir.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="f7c8f-152">**Condition**</span><span class="sxs-lookup"><span data-stu-id="f7c8f-152">**Condition**</span></span>|<span data-ttu-id="f7c8f-153">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="f7c8f-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7c8f-154">O **DeleteFolder** excluiu com êxito todas as mensagens e subpastas.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="f7c8f-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7c8f-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="f7c8f-156">O **DeleteFolder** não pôde excluir com êxito todas as mensagens e subpastas.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="f7c8f-157">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f7c8f-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="f7c8f-158">**DeleteFolder** não pôde ser concluída.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="f7c8f-159">Qualquer valor de erro, exceto MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f7c8f-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="f7c8f-160">Quando o **DeleteFolder** não puder ser concluído, não presuma que nenhum trabalho foi realizado.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="f7c8f-161">O **DeleteFolder** pode ter sido capaz de excluir uma ou mais das mensagens e subpastas antes de encontrar o erro.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="f7c8f-162">Se uma ou mais subpastas não puderem ser excluídas, **DeleteFolder** retornará MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, dependendo da implementação do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f7c8f-163">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f7c8f-163">MFCMAPI reference</span></span>

<span data-ttu-id="f7c8f-164">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f7c8f-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f7c8f-165">**File**</span></span>|<span data-ttu-id="f7c8f-166">**Função**</span><span class="sxs-lookup"><span data-stu-id="f7c8f-166">**Function**</span></span>|<span data-ttu-id="f7c8f-167">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f7c8f-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7c8f-168">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="f7c8f-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="f7c8f-169">CMsgStoreDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="f7c8f-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="f7c8f-170">MFCMAPI usa o método **IMAPIFolder::D eletefolder** para excluir pastas.</span><span class="sxs-lookup"><span data-stu-id="f7c8f-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7c8f-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7c8f-171">See also</span></span>



[<span data-ttu-id="f7c8f-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f7c8f-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="f7c8f-173">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f7c8f-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

