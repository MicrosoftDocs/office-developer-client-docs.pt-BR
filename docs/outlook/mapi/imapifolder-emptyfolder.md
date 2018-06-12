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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7d8653b8f0cb2196319c4a9c2b4bca89c8be5a24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766991"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="06af7-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="06af7-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="06af7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06af7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06af7-105">Exclui todas as mensagens e subpastas de uma pasta sem excluir na pasta propriamente dita.</span><span class="sxs-lookup"><span data-stu-id="06af7-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="06af7-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="06af7-106">Parameters</span></span>

 <span data-ttu-id="06af7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="06af7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="06af7-108">[in] Um identificador para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="06af7-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="06af7-109">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="06af7-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="06af7-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="06af7-110">_lpProgress_</span></span>
  
> <span data-ttu-id="06af7-111">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="06af7-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="06af7-112">Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="06af7-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="06af7-113">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="06af7-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="06af7-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="06af7-114">_ulFlags_</span></span>
  
> <span data-ttu-id="06af7-115">[in] Uma bitmask dos sinalizadores que controla como a pasta será esvaziada.</span><span class="sxs-lookup"><span data-stu-id="06af7-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="06af7-116">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="06af7-116">The following flags can be set:</span></span>
    
<span data-ttu-id="06af7-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="06af7-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="06af7-118">Exclui todas as subpastas, incluindo subpastas que contêm mensagens com conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="06af7-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="06af7-119">O sinalizador DEL_ASSOCIATED tem significado apenas para a pasta de nível superior que a chamada atua no.</span><span class="sxs-lookup"><span data-stu-id="06af7-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="06af7-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="06af7-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="06af7-121">Remove permanentemente todas as mensagens, incluindo aquelas excluída.</span><span class="sxs-lookup"><span data-stu-id="06af7-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="06af7-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="06af7-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="06af7-123">Exibe um indicador de progresso enquanto continua a operação.</span><span class="sxs-lookup"><span data-stu-id="06af7-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06af7-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="06af7-124">Return value</span></span>

<span data-ttu-id="06af7-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="06af7-125">S_OK</span></span> 
  
> <span data-ttu-id="06af7-126">A pasta foi esvaziada com êxito.</span><span class="sxs-lookup"><span data-stu-id="06af7-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="06af7-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="06af7-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="06af7-128">A chamada foi bem-sucedida, mas a pasta não foi esvaziada completamente.</span><span class="sxs-lookup"><span data-stu-id="06af7-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="06af7-129">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="06af7-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="06af7-130">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="06af7-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="06af7-131">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="06af7-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06af7-132">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="06af7-132">Remarks</span></span>

<span data-ttu-id="06af7-133">O método **IMAPIFolder::EmptyFolder** exclui todo o conteúdo de uma pasta sem excluir na pasta propriamente dita.</span><span class="sxs-lookup"><span data-stu-id="06af7-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="06af7-134">Durante uma chamada de **EmptyFolder** , as mensagens enviadas não são excluídas.</span><span class="sxs-lookup"><span data-stu-id="06af7-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="06af7-135">Conteúdo de uma pasta associado incluem mensagens que são usadas para descrever o armazenamento de soluções personalizadas, regras, formulários personalizados e modos de exibição e também podem incluir as definições do formulário.</span><span class="sxs-lookup"><span data-stu-id="06af7-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="06af7-136">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="06af7-136">Notes to implementers</span></span>

<span data-ttu-id="06af7-137">Não chame o método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para mensagens na pasta que foram enviadas.</span><span class="sxs-lookup"><span data-stu-id="06af7-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="06af7-138">Mensagens enviadas não são excluídas.</span><span class="sxs-lookup"><span data-stu-id="06af7-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="06af7-139">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="06af7-139">Notes to callers</span></span>

<span data-ttu-id="06af7-140">Espera esses valores de retorno sob as condições a seguintes.</span><span class="sxs-lookup"><span data-stu-id="06af7-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="06af7-141">**Condição**</span><span class="sxs-lookup"><span data-stu-id="06af7-141">**Condition**</span></span>|<span data-ttu-id="06af7-142">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="06af7-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06af7-143">**EmptyFolder** com êxito tem esvaziada a pasta.</span><span class="sxs-lookup"><span data-stu-id="06af7-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="06af7-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="06af7-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="06af7-145">**EmptyFolder** não pôde completamente esvazie a pasta.</span><span class="sxs-lookup"><span data-stu-id="06af7-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="06af7-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="06af7-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="06af7-147">**EmptyFolder** não pôde concluir.</span><span class="sxs-lookup"><span data-stu-id="06af7-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="06af7-148">Qualquer valor de erro</span><span class="sxs-lookup"><span data-stu-id="06af7-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="06af7-149">Quando **EmptyFolder** é impossível concluir, não presuma que foi feito nenhum trabalho.</span><span class="sxs-lookup"><span data-stu-id="06af7-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="06af7-150">**EmptyFolder** podem ter sido capazes de excluir uma parte do conteúdo da pasta antes da ocorrência de erro.</span><span class="sxs-lookup"><span data-stu-id="06af7-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="06af7-151">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="06af7-151">MFCMAPI reference</span></span>

<span data-ttu-id="06af7-152">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="06af7-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="06af7-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="06af7-153">**File**</span></span>|<span data-ttu-id="06af7-154">**Function**</span><span class="sxs-lookup"><span data-stu-id="06af7-154">**Function**</span></span>|<span data-ttu-id="06af7-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="06af7-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="06af7-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="06af7-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="06af7-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="06af7-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="06af7-158">MFCMAPI usa o método **IMAPIFolder::EmptyFolder** para excluir o conteúdo da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="06af7-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06af7-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="06af7-159">See also</span></span>



[<span data-ttu-id="06af7-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="06af7-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="06af7-161">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="06af7-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="06af7-162">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="06af7-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="06af7-163">Usando Macros para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="06af7-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

