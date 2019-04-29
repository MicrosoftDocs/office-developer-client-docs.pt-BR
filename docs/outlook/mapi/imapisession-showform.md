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
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412524"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="664c3-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="664c3-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="664c3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="664c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="664c3-105">Exibe um formulário.</span><span class="sxs-lookup"><span data-stu-id="664c3-105">Displays a form.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="664c3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="664c3-106">Parameters</span></span>

 <span data-ttu-id="664c3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="664c3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="664c3-108">no Uma alça para a janela pai do formulário.</span><span class="sxs-lookup"><span data-stu-id="664c3-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="664c3-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="664c3-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="664c3-110">no Um ponteiro para o repositório de mensagens que contém a pasta apontada pelo parâmetro _lpParentFolder_ .</span><span class="sxs-lookup"><span data-stu-id="664c3-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="664c3-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="664c3-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="664c3-112">no Um ponteiro para a pasta na qual a mensagem associada ao parâmetro _ulMessageToken_ foi criada.</span><span class="sxs-lookup"><span data-stu-id="664c3-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="664c3-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="664c3-113">_lpInterface_</span></span>
  
> <span data-ttu-id="664c3-114">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a mensagem exibida no formulário.</span><span class="sxs-lookup"><span data-stu-id="664c3-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="664c3-115">O parâmetro _lpInterface_ deve ser nulo ou IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="664c3-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="664c3-116">Passar resultados nulos na interface padrão, [IMessage](imessageimapiprop.md), sendo usado.</span><span class="sxs-lookup"><span data-stu-id="664c3-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="664c3-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="664c3-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="664c3-118">no O token que está associado à mensagem a ser exibida no formulário.</span><span class="sxs-lookup"><span data-stu-id="664c3-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="664c3-119">O parâmetro _ulMessageToken_ deve ser definido como o conteúdo do parâmetro _lpulMessageToken_ da chamada anterior para [IMAPISession::P repareform](imapisession-prepareform.md).</span><span class="sxs-lookup"><span data-stu-id="664c3-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="664c3-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="664c3-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="664c3-121">no Serve deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="664c3-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="664c3-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="664c3-122">_ulFlags_</span></span>
  
> <span data-ttu-id="664c3-123">no Uma bitmask de sinalizadores que controla como e se a mensagem é salva.</span><span class="sxs-lookup"><span data-stu-id="664c3-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="664c3-124">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="664c3-124">The following flags can be set:</span></span>
    
<span data-ttu-id="664c3-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="664c3-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="664c3-126">A mensagem nunca foi salva (ou seja, seu método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) nunca foi chamado).</span><span class="sxs-lookup"><span data-stu-id="664c3-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="664c3-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="664c3-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="664c3-128">A mensagem deve ser salva em sua pasta pai.</span><span class="sxs-lookup"><span data-stu-id="664c3-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="664c3-129">A mensagem não é processada para envio, mas é publicada na pasta.</span><span class="sxs-lookup"><span data-stu-id="664c3-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="664c3-130">Se esse sinalizador não for definido, a mensagem será copiada para a saída e processada para envio.</span><span class="sxs-lookup"><span data-stu-id="664c3-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="664c3-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="664c3-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="664c3-132">no Uma bitmask de sinalizadores copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) da mensagem associada ao token no parâmetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="664c3-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="664c3-133">Os sinalizadores fornecem informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="664c3-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="664c3-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="664c3-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="664c3-135">no Uma bitmask de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem associada ao token no parâmetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="664c3-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="664c3-136">Esses sinalizadores fornecem mais informações sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="664c3-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="664c3-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="664c3-137">_ulAccess_</span></span>
  
> <span data-ttu-id="664c3-138">no Um sinalizador que indica o nível de permissão para a mensagem exibida no formulário.</span><span class="sxs-lookup"><span data-stu-id="664c3-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="664c3-139">Essas informações são copiadas da propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) da mensagem associada ao token no parâmetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="664c3-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="664c3-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="664c3-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="664c3-141">no Um ponteiro para a classe de mensagem da mensagem que está sendo exibida no formulário, copiado da propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) da mensagem associada ao token no parâmetro _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="664c3-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="664c3-142">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="664c3-142">Return value</span></span>

<span data-ttu-id="664c3-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="664c3-143">S_OK</span></span> 
  
> <span data-ttu-id="664c3-144">O formulário foi exibido com êxito.</span><span class="sxs-lookup"><span data-stu-id="664c3-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="664c3-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="664c3-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="664c3-146">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="664c3-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="664c3-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="664c3-147">Remarks</span></span>

<span data-ttu-id="664c3-148">O método **IMAPISession::** formulário exibe um formulário de mensagem que foi preparado pelo método **IMAPISession::P repareform** .</span><span class="sxs-lookup"><span data-stu-id="664c3-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="664c3-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="664c3-149">Notes to callers</span></span>

<span data-ttu-id="664c3-150">Você deve ter apenas uma única referência à mensagem passada no parâmetro _lpMessage_ do método **PrepareForm** .</span><span class="sxs-lookup"><span data-stu-id="664c3-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="664c3-151">Esteja ciente de que as implementações de formulários podem retornar valores de erro diferentes daqueles documentados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="664c3-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="664c3-152">Se você puder usar esses valores de erro para fazer uma determinação mais precisa da condição de erro, faça-o.</span><span class="sxs-lookup"><span data-stu-id="664c3-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="664c3-153">Caso contrário, manipule esses erros como faria com o MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="664c3-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="664c3-154">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="664c3-154">MFCMAPI reference</span></span>

<span data-ttu-id="664c3-155">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="664c3-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="664c3-156">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="664c3-156">**File**</span></span>|<span data-ttu-id="664c3-157">**Função**</span><span class="sxs-lookup"><span data-stu-id="664c3-157">**Function**</span></span>|<span data-ttu-id="664c3-158">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="664c3-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="664c3-159">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="664c3-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="664c3-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="664c3-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="664c3-161">MFCMAPI usa o método **IMAPISession:: CreateForm** , juntamente com o método **PrepareForm** , para exibir uma mensagem em um formulário de janela restrita.</span><span class="sxs-lookup"><span data-stu-id="664c3-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="664c3-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="664c3-162">See also</span></span>



[<span data-ttu-id="664c3-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="664c3-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="664c3-164">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="664c3-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="664c3-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="664c3-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="664c3-166">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="664c3-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="664c3-167">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="664c3-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

