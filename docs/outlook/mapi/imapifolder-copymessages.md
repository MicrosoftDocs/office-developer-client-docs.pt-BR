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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e6e9e9cefc75ffc78ee7beb47e89063ea1a66ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766968"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="0f6fb-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="0f6fb-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="0f6fb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f6fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f6fb-105">Copia ou move uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0f6fb-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0f6fb-106">Parameters</span></span>

 <span data-ttu-id="0f6fb-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="0f6fb-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="0f6fb-108">[in] Um ponteiro para uma matriz de estruturas [ENTRYLIST](entrylist.md) que identificam a mensagem ou mensagens para copiar ou mover.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="0f6fb-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0f6fb-109">_lpInterface_</span></span>
  
> <span data-ttu-id="0f6fb-110">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a pasta de destino apontado pelo parâmetro _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="0f6fb-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="0f6fb-111">Passagem nula resulta em retornando a interface de pasta padrão, o provedor de serviços [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0f6fb-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="0f6fb-112">Os clientes devem passar NULL.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-112">Clients must pass NULL.</span></span> <span data-ttu-id="0f6fb-113">Outros chamadores podem definir o parâmetro _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="0f6fb-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="0f6fb-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="0f6fb-115">[in] Um ponteiro para a pasta aberta para receber as mensagens copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="0f6fb-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0f6fb-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="0f6fb-117">[in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="0f6fb-118">O parâmetro _ulUIParam_ é ignorado, a menos que o cliente define o sinalizador MESSAGE_DIALOG no parâmetro _ulFlags_ e transmite NULL no parâmetro _lpProgress_ .</span><span class="sxs-lookup"><span data-stu-id="0f6fb-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="0f6fb-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="0f6fb-119">_lpProgress_</span></span>
  
> <span data-ttu-id="0f6fb-120">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="0f6fb-121">Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="0f6fb-122">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG está definido na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="0f6fb-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0f6fb-123">_ulFlags_</span></span>
  
> <span data-ttu-id="0f6fb-124">[in] Uma bitmask dos sinalizadores que controla como a operação de cópia ou movimentação é realizada.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="0f6fb-125">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="0f6fb-125">The following flags can be set:</span></span>
    
<span data-ttu-id="0f6fb-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="0f6fb-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="0f6fb-127">Informa o provedor de armazenamento de mensagem para retornar imediatamente MAPI_E_DECLINE_COPY se ele implementa **IMAPIFolder::CopyMessages** chamando o método [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) de suporte do objeto.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="0f6fb-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0f6fb-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="0f6fb-129">Exibe um indicador de progresso conforme continua a operação.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="0f6fb-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="0f6fb-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="0f6fb-131">A mensagem ou mensagens deverão ser movidos, em vez de copiados.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="0f6fb-132">Se MESSAGE_MOVE não estiver definida, as mensagens serão copiadas.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f6fb-133">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0f6fb-133">Return value</span></span>

<span data-ttu-id="0f6fb-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f6fb-134">S_OK</span></span> 
  
> <span data-ttu-id="0f6fb-135">A mensagem ou mensagens foram com êxito copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="0f6fb-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="0f6fb-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="0f6fb-137">O provedor implemente esse método chamando um método de objeto de suporte e o chamador passou o sinalizador MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="0f6fb-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="0f6fb-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="0f6fb-139">A chamada foi bem-sucedida, mas nem todas as entradas foram copiadas ou movidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="0f6fb-140">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="0f6fb-141">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="0f6fb-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="0f6fb-142">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="0f6fb-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f6fb-143">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="0f6fb-143">Remarks</span></span>

<span data-ttu-id="0f6fb-144">O método **IMAPIFolder::CopyMessages** copia ou mova mensagens para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="0f6fb-145">Mensagens que são abertas com leitura/gravação permissão pode ser movido ou copiado.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0f6fb-146">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="0f6fb-146">Notes to implementers</span></span>

<span data-ttu-id="0f6fb-147">Se você estiver copiando mensagens para outro repositório de mensagens sem usar o método [IMAPISupport::CopyMessages](imapisupport-copymessages.md) , primeiro você deve chamar [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) com o sinalizador GENERATE_RECEIPT_ONLY definido.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="0f6fb-148">O armazenamento de recebimento de mensagens não é responsável por gerar relatórios de leitura para as mensagens copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="0f6fb-149">Se você estiver chamando **IMAPISupport::CopyMessages** para implementar **IMAPIFolder::CopyMessages**, não for chamado **SetReadFlags**; MAPI irá chamá-lo.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="0f6fb-150">A implementação pode mover ou copiar as mensagens em qualquer ordem e gerar relatórios de status de leitura em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="0f6fb-151">Ou seja, você pode concluir copiem mensagens antes de gerar qualquer um dos relatórios de status de leitura ou enviar relatórios antes de sua implementação inicia a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="0f6fb-152">No entanto, ler relatórios devem ser enviados para todas as mensagens a serem copiados, independentemente se a cópia é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="0f6fb-153">Quando a operação de cópia ou movimentação envolve mais de uma mensagem, execute a operação como completamente.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="0f6fb-154">Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="0f6fb-155">Tente manter os identificadores de entrada entre as operações de movimentação ou cópia.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="0f6fb-156">Você também deve preservar identificadores de entrada, embora não seja obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="0f6fb-157">Envie notificações quando você mover ou copiar mensagens para que os clientes seja informados de que suas chamadas para métodos de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) das mensagens podem falhar.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="0f6fb-158">Não incluir o status da mensagem na cópia ou operação de movimentação.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="0f6fb-159">Mover ou copiar um status de mensagem muito afeta o desempenho.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0f6fb-160">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0f6fb-160">Notes to callers</span></span>

<span data-ttu-id="0f6fb-161">Use **IMAPIFolder::CopyMessages** para preencher a pastas de resultados da pesquisa, onde as mensagens são frequentemente agrupadas por pasta pai.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="0f6fb-162">Espera esses valores de retorno sob as condições a seguintes.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="0f6fb-163">**Condição**</span><span class="sxs-lookup"><span data-stu-id="0f6fb-163">**Condition**</span></span>|<span data-ttu-id="0f6fb-164">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="0f6fb-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f6fb-165">**IMAPIFolder::CopyMessages** tem copiados ou movidos de cada mensagem com êxito.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="0f6fb-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f6fb-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="0f6fb-167">**IMAPIFolder::CopyMessages** foi capaz de copiar ou mover todas as mensagens com êxito.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="0f6fb-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="0f6fb-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="0f6fb-169">**IMAPIFolder::CopyMessages** não pôde concluir.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="0f6fb-170">Qualquer valor de erro</span><span class="sxs-lookup"><span data-stu-id="0f6fb-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="0f6fb-171">Quando **IMAPIFolder::CopyMessages** é impossível concluir, não presuma que foi feito nenhum trabalho.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="0f6fb-172">**IMAPIFolder::CopyMessages** podem ter sido capaz de copiar ou mover uma ou mais mensagens antes da ocorrência de erro.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f6fb-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f6fb-173">See also</span></span>



[<span data-ttu-id="0f6fb-174">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0f6fb-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

