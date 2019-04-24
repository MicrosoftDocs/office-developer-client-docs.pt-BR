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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280103"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="30f7d-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="30f7d-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="30f7d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30f7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30f7d-105">Exclui todas as mensagens e subpastas de uma pasta sem excluir a própria pasta.</span><span class="sxs-lookup"><span data-stu-id="30f7d-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="30f7d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30f7d-106">Parameters</span></span>

 <span data-ttu-id="30f7d-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="30f7d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="30f7d-108">no Uma alça para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="30f7d-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="30f7d-109">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="30f7d-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="30f7d-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="30f7d-110">_lpProgress_</span></span>
  
> <span data-ttu-id="30f7d-111">no Um ponteiro para um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="30f7d-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="30f7d-112">Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="30f7d-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="30f7d-113">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="30f7d-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="30f7d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="30f7d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="30f7d-115">no Uma bitmask de sinalizadores que controla como a pasta é esvaziada.</span><span class="sxs-lookup"><span data-stu-id="30f7d-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="30f7d-116">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="30f7d-116">The following flags can be set:</span></span>
    
<span data-ttu-id="30f7d-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="30f7d-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="30f7d-118">Exclui todas as subpastas, incluindo as subpastas que contêm mensagens com conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="30f7d-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="30f7d-119">O sinalizador DEL_ASSOCIATED tem significado apenas para a pasta de nível superior na qual a chamada atua.</span><span class="sxs-lookup"><span data-stu-id="30f7d-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="30f7d-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="30f7d-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="30f7d-121">Remove permanentemente todas as mensagens, incluindo as excluídas de forma reversível.</span><span class="sxs-lookup"><span data-stu-id="30f7d-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="30f7d-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="30f7d-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="30f7d-123">Exibe um indicador de progresso enquanto a operação prossegue.</span><span class="sxs-lookup"><span data-stu-id="30f7d-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="30f7d-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="30f7d-124">Return value</span></span>

<span data-ttu-id="30f7d-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="30f7d-125">S_OK</span></span> 
  
> <span data-ttu-id="30f7d-126">A pasta foi esvaziada com êxito.</span><span class="sxs-lookup"><span data-stu-id="30f7d-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="30f7d-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="30f7d-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="30f7d-128">A chamada teve êxito, mas a pasta não foi completamente esvaziada.</span><span class="sxs-lookup"><span data-stu-id="30f7d-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="30f7d-129">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="30f7d-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="30f7d-130">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="30f7d-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="30f7d-131">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="30f7d-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30f7d-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="30f7d-132">Remarks</span></span>

<span data-ttu-id="30f7d-133">O método **IMAPIFolder:: EmptyFolder** exclui todo o conteúdo de uma pasta sem excluir a pasta propriamente dita.</span><span class="sxs-lookup"><span data-stu-id="30f7d-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="30f7d-134">Durante uma chamada **EmptyFolder** , as mensagens enviadas não são excluídas.</span><span class="sxs-lookup"><span data-stu-id="30f7d-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="30f7d-135">O conteúdo associado de uma pasta inclui mensagens usadas para descrever modos de exibição, regras, formulários personalizados e armazenamento de solução personalizada, e também pode incluir definições de formulário.</span><span class="sxs-lookup"><span data-stu-id="30f7d-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="30f7d-136">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="30f7d-136">Notes to implementers</span></span>

<span data-ttu-id="30f7d-137">Não chame o método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para mensagens na pasta que foi enviada.</span><span class="sxs-lookup"><span data-stu-id="30f7d-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="30f7d-138">As mensagens enviadas não são excluídas.</span><span class="sxs-lookup"><span data-stu-id="30f7d-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="30f7d-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="30f7d-139">Notes to callers</span></span>

<span data-ttu-id="30f7d-140">Espere estes valores de retorno sob as condições a seguir.</span><span class="sxs-lookup"><span data-stu-id="30f7d-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="30f7d-141">**Condition**</span><span class="sxs-lookup"><span data-stu-id="30f7d-141">**Condition**</span></span>|<span data-ttu-id="30f7d-142">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="30f7d-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30f7d-143">**EmptyFolder** esvaziar a pasta com êxito.</span><span class="sxs-lookup"><span data-stu-id="30f7d-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="30f7d-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="30f7d-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="30f7d-145">**EmptyFolder** não pôde esvaziar completamente a pasta.</span><span class="sxs-lookup"><span data-stu-id="30f7d-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="30f7d-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="30f7d-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="30f7d-147">**EmptyFolder** não pôde ser concluída.</span><span class="sxs-lookup"><span data-stu-id="30f7d-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="30f7d-148">Qualquer valor de erro</span><span class="sxs-lookup"><span data-stu-id="30f7d-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="30f7d-149">Quando o **EmptyFolder** não puder ser concluído, não presuma que nenhum trabalho foi realizado.</span><span class="sxs-lookup"><span data-stu-id="30f7d-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="30f7d-150">**EmptyFolder** pode ter sido possível excluir parte do conteúdo da pasta antes de encontrar o erro.</span><span class="sxs-lookup"><span data-stu-id="30f7d-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="30f7d-151">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="30f7d-151">MFCMAPI reference</span></span>

<span data-ttu-id="30f7d-152">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="30f7d-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="30f7d-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="30f7d-153">**File**</span></span>|<span data-ttu-id="30f7d-154">**Função**</span><span class="sxs-lookup"><span data-stu-id="30f7d-154">**Function**</span></span>|<span data-ttu-id="30f7d-155">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="30f7d-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30f7d-156">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="30f7d-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="30f7d-157">CMsgStoreDlg:: OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="30f7d-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="30f7d-158">MFCMAPI usa o método **IMAPIFolder:: EmptyFolder** para excluir o conteúdo da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="30f7d-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30f7d-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="30f7d-159">See also</span></span>



[<span data-ttu-id="30f7d-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="30f7d-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="30f7d-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="30f7d-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="30f7d-162">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="30f7d-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="30f7d-163">Usando macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="30f7d-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

