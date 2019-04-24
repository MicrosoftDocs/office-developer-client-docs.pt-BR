---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280124"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="ffe0f-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ffe0f-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="ffe0f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffe0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffe0f-105">Copia ou move uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-105">Copies or moves one or more messages.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ffe0f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffe0f-106">Parameters</span></span>

 <span data-ttu-id="ffe0f-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="ffe0f-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="ffe0f-108">no Um ponteiro para uma matriz de [](entrylist.md) estruturas de ENTRYLIST que identificam a mensagem ou mensagens a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="ffe0f-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ffe0f-109">_lpInterface_</span></span>
  
> <span data-ttu-id="ffe0f-110">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a pasta de destino indicada pelo parâmetro _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="ffe0f-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="ffe0f-111">Passar resultados nulos no provedor de serviços retornando a interface de pasta padrão, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="ffe0f-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="ffe0f-112">Os clientes devem passar NULL.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-112">Clients must pass NULL.</span></span> <span data-ttu-id="ffe0f-113">Outros chamadores podem definir o parâmetro _lpInterface_ como IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="ffe0f-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="ffe0f-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="ffe0f-115">no Um ponteiro para a pasta aberta para receber as mensagens copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="ffe0f-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ffe0f-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="ffe0f-117">no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="ffe0f-118">O parâmetro _ulUIParam_ é ignorado, a menos que o cliente defina o sinalizador MESSAGE_DIALOG no parâmetro _PARÂMETROULFLAGS_ e passe nulo no parâmetro _lpProgress_ .</span><span class="sxs-lookup"><span data-stu-id="ffe0f-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="ffe0f-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="ffe0f-119">_lpProgress_</span></span>
  
> <span data-ttu-id="ffe0f-120">no Um ponteiro para um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ffe0f-121">Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="ffe0f-122">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido em _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="ffe0f-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ffe0f-123">_ulFlags_</span></span>
  
> <span data-ttu-id="ffe0f-124">no Uma bitmask de sinalizadores que controlam como a operação de cópia ou movimentação é realizada.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="ffe0f-125">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ffe0f-125">The following flags can be set:</span></span>
    
<span data-ttu-id="ffe0f-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="ffe0f-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="ffe0f-127">Informa ao provedor de repositório de mensagens para retornar imediatamente o MAPI_E_DECLINE_COPY se ele implementar **IMAPIFolder:: CopyMessages** chamando o objeto support [IMAPISupport::D ocopyto](imapisupport-docopyto.md) ou [IMAPISupport::D método ocopyprops](imapisupport-docopyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="ffe0f-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="ffe0f-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ffe0f-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="ffe0f-129">Exibe um indicador de progresso à medida que a operação prossegue.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="ffe0f-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="ffe0f-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="ffe0f-131">A mensagem ou as mensagens devem ser movidas em vez de copiadas.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="ffe0f-132">Se MESSAGE_MOVE não for definido, as mensagens serão copiadas.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ffe0f-133">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ffe0f-133">Return value</span></span>

<span data-ttu-id="ffe0f-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="ffe0f-134">S_OK</span></span> 
  
> <span data-ttu-id="ffe0f-135">A mensagem ou mensagens foram copiadas ou movidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="ffe0f-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="ffe0f-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="ffe0f-137">O provedor implementa esse método chamando um método de objeto support e o chamador passou o sinalizador MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="ffe0f-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="ffe0f-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="ffe0f-139">A chamada teve êxito, mas nem todas as entradas foram copiadas ou movidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="ffe0f-140">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ffe0f-141">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="ffe0f-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ffe0f-142">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ffe0f-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ffe0f-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffe0f-143">Remarks</span></span>

<span data-ttu-id="ffe0f-144">O método **IMAPIFolder:: CopyMessages** copia ou move mensagens para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="ffe0f-145">As mensagens abertas com permissão de leitura/gravação podem ser movidas ou copiadas.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ffe0f-146">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ffe0f-146">Notes to implementers</span></span>

<span data-ttu-id="ffe0f-147">Se você estiver copiando mensagens para outro repositório de mensagens sem usar o método [IMAPISupport:: CopyMessages](imapisupport-copymessages.md) , primeiro você deve chamar [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) com o sinalizador GENERATE_RECEIPT_ONLY definido.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="ffe0f-148">O repositório de mensagens de recebimento não é responsável por gerar relatórios de leitura para as mensagens copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="ffe0f-149">Se você estiver chamando **IMAPISupport:: CopyMessages** para implementar **IMAPIFolder:: CopyMessages**, não chame **SetReadFlags**; O MAPI o chamará.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="ffe0f-150">Sua implementação pode mover ou copiar as mensagens em qualquer ordem e gerar relatórios de status de leitura em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="ffe0f-151">Ou seja, você pode concluir a cópia de mensagens antes de gerar qualquer um dos relatórios de status de leitura ou enviar os relatórios antes que sua implementação inicie a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="ffe0f-152">No enTanto, os relatórios de leitura devem ser enviados para que todas as mensagens sejam copiadas, independentemente da cópia ter sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="ffe0f-153">Quando a operação de cópia ou movimentação envolve mais de uma mensagem, execute a operação o mais completo possível.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="ffe0f-154">Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do seu controle, como a falta de memória, ficando sem espaço em disco ou corrupção no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="ffe0f-155">Tente manter os identificadores de entrada nas operações de movimentação ou cópia.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="ffe0f-156">Você também deve preservar os identificadores de entrada, embora não seja necessário.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="ffe0f-157">Enviar notificações quando você mover ou copiar mensagens para que os clientes sejam Forewarned que suas chamadas para as mensagens de [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) podem falhar.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="ffe0f-158">Não inclua o status de uma mensagem na operação de cópia ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="ffe0f-159">Mover ou copiar um status de mensagem afeta muito o desempenho.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ffe0f-160">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ffe0f-160">Notes to callers</span></span>

<span data-ttu-id="ffe0f-161">Use **IMAPIFolder:: CopyMessages** para preencher as pastas de resultados de pesquisa, onde as mensagens são agrupadas com frequência pela pasta pai.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="ffe0f-162">Espere estes valores de retorno sob as condições a seguir.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="ffe0f-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="ffe0f-163">**Condition**</span></span>|<span data-ttu-id="ffe0f-164">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="ffe0f-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffe0f-165">**IMAPIFolder:: CopyMessages** copiou ou moveu com êxito todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="ffe0f-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="ffe0f-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="ffe0f-167">**IMAPIFolder:: CopyMessages** não pôde copiar ou mover com êxito todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="ffe0f-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="ffe0f-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="ffe0f-169">**IMAPIFolder:: CopyMessages** não pôde ser concluída.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="ffe0f-170">Qualquer valor de erro</span><span class="sxs-lookup"><span data-stu-id="ffe0f-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="ffe0f-171">Quando o **IMAPIFolder:: CopyMessages** não consegue concluir, não presuma que nenhum trabalho foi realizado.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="ffe0f-172">**IMAPIFolder:: CopyMessages** pode ser capaz de copiar ou mover uma ou mais mensagens antes de encontrar o erro.</span><span class="sxs-lookup"><span data-stu-id="ffe0f-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ffe0f-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffe0f-173">See also</span></span>



[<span data-ttu-id="ffe0f-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ffe0f-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

