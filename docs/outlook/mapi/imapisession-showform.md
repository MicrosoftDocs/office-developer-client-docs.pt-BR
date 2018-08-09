---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d20c8e7432903ef9334f066df31694752384d034
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767202"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="71c70-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="71c70-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="71c70-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="71c70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="71c70-105">Exibe um formulário.</span><span class="sxs-lookup"><span data-stu-id="71c70-105">Displays a form.</span></span>
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="71c70-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71c70-106">Parameters</span></span>

 <span data-ttu-id="71c70-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="71c70-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="71c70-108">[in] Uma alça para a janela pai do formulário.</span><span class="sxs-lookup"><span data-stu-id="71c70-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="71c70-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="71c70-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="71c70-110">[in] Um ponteiro para o armazenamento de mensagens que contém a pasta apontado pelo parâmetro _lpParentFolder_ .</span><span class="sxs-lookup"><span data-stu-id="71c70-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="71c70-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="71c70-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="71c70-112">[in] Um ponteiro para a pasta na qual a mensagem associada com o parâmetro _ulMessageToken_ foi criada.</span><span class="sxs-lookup"><span data-stu-id="71c70-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="71c70-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="71c70-113">_lpInterface_</span></span>
  
> <span data-ttu-id="71c70-114">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a mensagem que é exibida no formulário.</span><span class="sxs-lookup"><span data-stu-id="71c70-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="71c70-115">O parâmetro _lpInterface_ deve ser NULL ou IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="71c70-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="71c70-116">Passagem nula resulta na interface padrão, [IMessage](imessageimapiprop.md), sendo usada.</span><span class="sxs-lookup"><span data-stu-id="71c70-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="71c70-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="71c70-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="71c70-118">[in] O token que está associado com a mensagem a ser exibido no formulário.</span><span class="sxs-lookup"><span data-stu-id="71c70-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="71c70-119">O parâmetro _ulMessageToken_ deve ser definido como o conteúdo do parâmetro _lpulMessageToken_ da chamada anterior para [PrepareForm](imapisession-prepareform.md).</span><span class="sxs-lookup"><span data-stu-id="71c70-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="71c70-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="71c70-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="71c70-121">[in] Reservado; deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="71c70-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="71c70-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="71c70-122">_ulFlags_</span></span>
  
> <span data-ttu-id="71c70-123">[in] Uma bitmask dos sinalizadores que controla como e se a mensagem será salva.</span><span class="sxs-lookup"><span data-stu-id="71c70-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="71c70-124">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="71c70-124">The following flags can be set:</span></span>
    
<span data-ttu-id="71c70-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="71c70-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="71c70-126">A mensagem nunca tiver sido salvo (ou seja, seu método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) tem nunca foi chamado).</span><span class="sxs-lookup"><span data-stu-id="71c70-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="71c70-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="71c70-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="71c70-128">A mensagem deve ser salvo em sua pasta pai.</span><span class="sxs-lookup"><span data-stu-id="71c70-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="71c70-129">A mensagem não é processada para enviar, mas é postada para a pasta.</span><span class="sxs-lookup"><span data-stu-id="71c70-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="71c70-130">Se esse sinalizador não estiver definida, a mensagem é copiada para a caixa de saída e é processada para enviar.</span><span class="sxs-lookup"><span data-stu-id="71c70-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="71c70-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="71c70-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="71c70-132">[in] Uma bitmask dos sinalizadores copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem associada com o token no parâmetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="71c70-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="71c70-133">Os sinalizadores fornecem informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="71c70-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="71c70-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="71c70-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="71c70-135">[in] Uma bitmask dos sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem associada com o token no parâmetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="71c70-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="71c70-136">Esses sinalizadores fornecem mais informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="71c70-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="71c70-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="71c70-137">_ulAccess_</span></span>
  
> <span data-ttu-id="71c70-138">[in] Um sinalizador que indica o nível de permissão para a mensagem que é exibida no formulário.</span><span class="sxs-lookup"><span data-stu-id="71c70-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="71c70-139">Essa informação é copiada da propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) da mensagem associada com o token no parâmetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="71c70-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="71c70-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="71c70-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="71c70-141">[in] Um ponteiro para a classe de mensagem da mensagem que está sendo exibida no formulário, copiado da propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem associada com o token no parâmetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="71c70-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="71c70-142">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="71c70-142">Return value</span></span>

<span data-ttu-id="71c70-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="71c70-143">S_OK</span></span> 
  
> <span data-ttu-id="71c70-144">O formulário foi exibido com êxito.</span><span class="sxs-lookup"><span data-stu-id="71c70-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="71c70-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="71c70-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="71c70-146">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="71c70-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="71c70-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="71c70-147">Remarks</span></span>

<span data-ttu-id="71c70-148">O método **IMAPISession:: ShowForm** exibe um formulário de mensagem que foi preparado pelo método **PrepareForm** .</span><span class="sxs-lookup"><span data-stu-id="71c70-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="71c70-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="71c70-149">Notes to callers</span></span>

<span data-ttu-id="71c70-150">Você deve ter uma única referência à mensagem passada no parâmetro de _lpMessage_ do método **PrepareForm** .</span><span class="sxs-lookup"><span data-stu-id="71c70-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="71c70-151">Lembre-se de que as implementações de formulário podem retornar valores de erro diferentes das documentados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="71c70-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="71c70-152">Se você pode usar estes valores de erro para tomar uma decisão mais precisa da condição de erro, fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="71c70-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="71c70-153">Caso contrário, lidar com esses erros ocorram conforme você usaria MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="71c70-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="71c70-154">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="71c70-154">MFCMAPI reference</span></span>

<span data-ttu-id="71c70-155">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="71c70-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="71c70-156">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="71c70-156">**File**</span></span>|<span data-ttu-id="71c70-157">**Function**</span><span class="sxs-lookup"><span data-stu-id="71c70-157">**Function**</span></span>|<span data-ttu-id="71c70-158">**Comment**</span><span class="sxs-lookup"><span data-stu-id="71c70-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="71c70-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="71c70-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="71c70-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="71c70-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="71c70-161">MFCMAPI usa o método **IMAPISession:: ShowForm** , junto com o método **PrepareForm** , exiba uma mensagem em um formulário restrito.</span><span class="sxs-lookup"><span data-stu-id="71c70-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71c70-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="71c70-162">See also</span></span>



[<span data-ttu-id="71c70-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="71c70-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="71c70-164">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="71c70-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="71c70-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="71c70-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="71c70-166">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71c70-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="71c70-167">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="71c70-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

