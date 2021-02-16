---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416780"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="436bc-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="436bc-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="436bc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="436bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="436bc-105">Exclui todas as mensagens e subpastas de uma pasta sem excluir a própria pasta.</span><span class="sxs-lookup"><span data-stu-id="436bc-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="436bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="436bc-106">Parameters</span></span>

 <span data-ttu-id="436bc-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="436bc-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="436bc-108">[in] Um alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="436bc-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="436bc-109">O _parâmetro ulUIParam é_ ignorado, a menos que o FOLDER_DIALOG padrão seja definido no parâmetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="436bc-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="436bc-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="436bc-110">_lpProgress_</span></span>
  
> <span data-ttu-id="436bc-111">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="436bc-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="436bc-112">Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="436bc-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="436bc-113">O _parâmetro lpProgress_ é ignorado, a menos que o FOLDER_DIALOG padrão seja definido no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="436bc-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="436bc-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="436bc-114">_ulFlags_</span></span>
  
> <span data-ttu-id="436bc-115">[in] Uma máscara de bits de sinalizadores que controla como a pasta é esvaziada.</span><span class="sxs-lookup"><span data-stu-id="436bc-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="436bc-116">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="436bc-116">The following flags can be set:</span></span>
    
<span data-ttu-id="436bc-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="436bc-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="436bc-118">Exclui todas as subpastas, incluindo subpastas que contêm mensagens com conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="436bc-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="436bc-119">O DEL_ASSOCIATED sinalizador tem significado apenas para a pasta de nível superior em que a chamada atua.</span><span class="sxs-lookup"><span data-stu-id="436bc-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="436bc-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="436bc-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="436bc-121">Remove permanentemente todas as mensagens, incluindo as excluídas de forma suave.</span><span class="sxs-lookup"><span data-stu-id="436bc-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="436bc-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="436bc-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="436bc-123">Exibe um indicador de progresso enquanto a operação prosse segue.</span><span class="sxs-lookup"><span data-stu-id="436bc-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="436bc-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="436bc-124">Return value</span></span>

<span data-ttu-id="436bc-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="436bc-125">S_OK</span></span> 
  
> <span data-ttu-id="436bc-126">A pasta foi esvaziada com êxito.</span><span class="sxs-lookup"><span data-stu-id="436bc-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="436bc-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="436bc-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="436bc-128">A chamada foi bem-sucedida, mas a pasta não foi completamente esvaziada.</span><span class="sxs-lookup"><span data-stu-id="436bc-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="436bc-129">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="436bc-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="436bc-130">Para testar esse aviso, use a **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="436bc-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="436bc-131">Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="436bc-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="436bc-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="436bc-132">Remarks</span></span>

<span data-ttu-id="436bc-133">O **método IMAPIFolder::EmptyFolder** exclui todo o conteúdo de uma pasta sem excluir a própria pasta.</span><span class="sxs-lookup"><span data-stu-id="436bc-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="436bc-134">Durante uma **chamada EmptyFolder,** as mensagens enviadas não são excluídas.</span><span class="sxs-lookup"><span data-stu-id="436bc-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="436bc-135">O conteúdo associado de uma pasta inclui mensagens que são usadas para descrever exibições, regras, formulários personalizados e armazenamento de soluções personalizado, e também podem incluir definições de formulário.</span><span class="sxs-lookup"><span data-stu-id="436bc-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="436bc-136">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="436bc-136">Notes to implementers</span></span>

<span data-ttu-id="436bc-137">Não chame o [método IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para mensagens na pasta que foram enviadas.</span><span class="sxs-lookup"><span data-stu-id="436bc-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="436bc-138">As mensagens enviadas não são excluídas.</span><span class="sxs-lookup"><span data-stu-id="436bc-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="436bc-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="436bc-139">Notes to callers</span></span>

<span data-ttu-id="436bc-140">Espere esses valores de retorno sob as seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="436bc-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="436bc-141">**Condition**</span><span class="sxs-lookup"><span data-stu-id="436bc-141">**Condition**</span></span>|<span data-ttu-id="436bc-142">**Valor de retorno**</span><span class="sxs-lookup"><span data-stu-id="436bc-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="436bc-143">**EmptyFolder** esvaziou a pasta com êxito.</span><span class="sxs-lookup"><span data-stu-id="436bc-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="436bc-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="436bc-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="436bc-145">**EmptyFolder** não pôde esvaziar completamente a pasta.</span><span class="sxs-lookup"><span data-stu-id="436bc-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="436bc-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="436bc-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="436bc-147">**EmptyFolder** não pôde ser concluída.</span><span class="sxs-lookup"><span data-stu-id="436bc-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="436bc-148">Qualquer valor de erro</span><span class="sxs-lookup"><span data-stu-id="436bc-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="436bc-149">Quando **EmptyFolder** não puder ser concluída, não suponha que nenhum trabalho foi feito.</span><span class="sxs-lookup"><span data-stu-id="436bc-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="436bc-150">**EmptyFolder** pode ter sido capaz de excluir parte do conteúdo da pasta antes de encontrar o erro.</span><span class="sxs-lookup"><span data-stu-id="436bc-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="436bc-151">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="436bc-151">MFCMAPI reference</span></span>

<span data-ttu-id="436bc-152">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="436bc-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="436bc-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="436bc-153">**File**</span></span>|<span data-ttu-id="436bc-154">**Função**</span><span class="sxs-lookup"><span data-stu-id="436bc-154">**Function**</span></span>|<span data-ttu-id="436bc-155">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="436bc-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="436bc-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="436bc-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="436bc-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="436bc-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="436bc-158">MFCMAPI usa o **método IMAPIFolder::EmptyFolder** para excluir o conteúdo da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="436bc-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="436bc-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="436bc-159">See also</span></span>



[<span data-ttu-id="436bc-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="436bc-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="436bc-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="436bc-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="436bc-162">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="436bc-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="436bc-163">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="436bc-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

