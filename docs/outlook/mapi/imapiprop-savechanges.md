---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398840"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="9423e-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9423e-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="9423e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9423e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9423e-105">Torna permanente quaisquer alterações feitas a um objeto desde a última operação de salvamento.</span><span class="sxs-lookup"><span data-stu-id="9423e-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9423e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9423e-106">Parameters</span></span>

 <span data-ttu-id="9423e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9423e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9423e-108">[in] Uma bitmask dos sinalizadores que controla o que acontece ao objeto quando o método **IMAPIProp::SaveChanges** é chamado.</span><span class="sxs-lookup"><span data-stu-id="9423e-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="9423e-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="9423e-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="9423e-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="9423e-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="9423e-111">Indica que a mensagem não foi entregue a partir de um Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9423e-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="9423e-112">Esse sinalizador deve ser usado em conjunto com o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) e o sinalizador ITEMPROC_FORCE para indicar um repositório PST que a mensagem é qualificada para regras de processamento antes que o repositório de arquivos (. PST) de pastas particulares notifica qualquer um cliente de escuta que a mensagem foi entregue.</span><span class="sxs-lookup"><span data-stu-id="9423e-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="9423e-113">Este regras processamento só se aplica às novas mensagens que são criadas com [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) em um servidor que não seja um servidor do Exchange, caso em que o Exchange Server seriam já processados regras na mensagem.</span><span class="sxs-lookup"><span data-stu-id="9423e-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="9423e-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="9423e-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="9423e-115">As alterações devem ser gravadas no objeto, substituindo quaisquer alterações anteriores que foram feitas ao objeto, e o objeto deve ser fechado.</span><span class="sxs-lookup"><span data-stu-id="9423e-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="9423e-116">Permissão de leitura/gravação deve ser definida para a operação tenha êxito.</span><span class="sxs-lookup"><span data-stu-id="9423e-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="9423e-117">O sinalizador FORCE_SAVE é usado após uma chamada anterior para **SaveChanges** retornado MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="9423e-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="9423e-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="9423e-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="9423e-119">As alterações devem ser confirmadas e o objeto deve ser mantido aberto para leitura.</span><span class="sxs-lookup"><span data-stu-id="9423e-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="9423e-120">Nenhuma alteração adicional será feita.</span><span class="sxs-lookup"><span data-stu-id="9423e-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="9423e-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="9423e-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="9423e-122">As alterações devem ser confirmadas e o objeto deve ser mantido aberto para permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9423e-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="9423e-123">Esse sinalizador geralmente é definido quando o objeto foi aberto pela primeira vez para permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9423e-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="9423e-124">As alterações subsequentes ao objeto são permitidas.</span><span class="sxs-lookup"><span data-stu-id="9423e-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="9423e-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9423e-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9423e-126">Permite **SaveChanges** retornar com êxito, possivelmente antes que as alterações forem confirmadas totalmente.</span><span class="sxs-lookup"><span data-stu-id="9423e-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="9423e-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="9423e-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="9423e-128">Permite que o spam filtrados em uma mensagem que está sendo salva.</span><span class="sxs-lookup"><span data-stu-id="9423e-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="9423e-129">O suporte à filtragem de spam está disponível somente se o tipo de endereço de email do remetente for SMTP(Simple Mail Transfer Protocol) e a mensagem estiver sendo salva em um repositório de um arquivo de pastas particulares (PST).</span><span class="sxs-lookup"><span data-stu-id="9423e-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9423e-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9423e-130">Return value</span></span>

<span data-ttu-id="9423e-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="9423e-131">S_OK</span></span> 
  
> <span data-ttu-id="9423e-132">O compromisso de alterações foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9423e-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="9423e-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9423e-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9423e-134">**SaveChanges** não podem manter o objeto aberto para permissão somente leitura se KEEP_OPEN_READONLY for definido, ou permissão de leitura/gravação, se KEEP_OPEN_READWRITE estiver definida.</span><span class="sxs-lookup"><span data-stu-id="9423e-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="9423e-135">Sem alterações são confirmadas.</span><span class="sxs-lookup"><span data-stu-id="9423e-135">No changes are committed.</span></span> 
    
<span data-ttu-id="9423e-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="9423e-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="9423e-137">O objeto foi alterado desde que foi aberto.</span><span class="sxs-lookup"><span data-stu-id="9423e-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="9423e-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="9423e-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="9423e-139">O objeto foi excluído desde que ela foi aberta.</span><span class="sxs-lookup"><span data-stu-id="9423e-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9423e-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="9423e-140">Remarks</span></span>

<span data-ttu-id="9423e-141">O método **IMAPIProp::SaveChanges** faz com que as alterações de propriedade permanente para objetos que suportam o modelo de transação do processamento, como mensagens, anexos, recipientes do catálogo de endereços e objetos de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9423e-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="9423e-142">Objetos que não oferecem suporte a transações, como pastas, repositórios de mensagem e seções de perfil, faça alterações permanentes imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9423e-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="9423e-143">Nenhuma chamada para **SaveChanges** é necessária.</span><span class="sxs-lookup"><span data-stu-id="9423e-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="9423e-144">Porque não têm os provedores de serviço gerar um identificador de entrada para seus objetos até que todas as propriedades foram salvos, **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) propriedade de um objeto pode não estar disponível até após seu método **SaveChanges** foi chamado.</span><span class="sxs-lookup"><span data-stu-id="9423e-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="9423e-145">Alguns provedores de aguardar até que o sinalizador KEEP_OPEN_READONLY está definido na chamada **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="9423e-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="9423e-146">KEEP_OPEN_READONLY indica que as alterações sejam salvos na chamada atual será as últimas alterações serão feitas no objeto.</span><span class="sxs-lookup"><span data-stu-id="9423e-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="9423e-147">Algumas implementações de repositório de mensagem do não mostrar recém-criadas mensagens em uma pasta até que um cliente salva a mensagem altera usando **SaveChanges** e libera os objetos de mensagem usando o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9423e-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="9423e-148">Além disso, algumas implementações de objeto não é possível gerar uma propriedade **PR_ENTRYID** para um objeto recém-criado até depois **SaveChanges** foi chamado e alguns podem fazê-lo apenas depois **SaveChanges** tiver sido chamado usando KEEP_OPEN_READONLY Defina no _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="9423e-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9423e-149">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="9423e-149">Notes to implementers</span></span>

<span data-ttu-id="9423e-150">Se você receber o sinalizador KEEP_OPEN_READONLY, você tem a opção de deixar o acesso do objeto como leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9423e-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="9423e-151">No entanto, um provedor pode nunca deixe um objeto em um estado somente leitura quando o sinalizador KEEP_OPEN_READWRITE é passado.</span><span class="sxs-lookup"><span data-stu-id="9423e-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="9423e-152">Quando um cliente salva vários anexos para várias mensagens, ele chama o método **SaveChanges** para cada anexo e cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="9423e-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="9423e-153">Geralmente, clientes definirão MAPI_DEFERRED_ERRORS para cada uma dessas chamadas, exceto o último.</span><span class="sxs-lookup"><span data-stu-id="9423e-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="9423e-154">Você pode retornar erros com a última chamada ou chamadas anteriores.</span><span class="sxs-lookup"><span data-stu-id="9423e-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="9423e-155">Você pode até mesmo ignorar o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="9423e-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="9423e-156">Se KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY for definido em conjunto com MAPI_DEFERRED_ERRORS, você pode ignorar a solicitação de diferimento de erro.</span><span class="sxs-lookup"><span data-stu-id="9423e-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="9423e-157">Se MAPI_DEFERRED_ERRORS não estiver definida no _ulFlags_, um dos erros adiados anteriormente pode ser retornado para a chamada **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="9423e-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="9423e-158">Se um provedor de transporte remoto fornece uma implementação funcional deste método é opcional e depende de outras escolhas de design na sua implementação.</span><span class="sxs-lookup"><span data-stu-id="9423e-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="9423e-159">Se você implementar esse método, fazê-lo de acordo com a documentação aqui.</span><span class="sxs-lookup"><span data-stu-id="9423e-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="9423e-160">Porque os objetos de pasta e objetos de status não serão transacionados, no mínimo implementação do provedor de um transporte remoto **SaveChanges** deve retornar S_OK sem realmente fazer qualquer trabalho.</span><span class="sxs-lookup"><span data-stu-id="9423e-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9423e-161">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9423e-161">Notes to callers</span></span>

<span data-ttu-id="9423e-162">Se um cliente passa KEEP_OPEN_READONLY, chama o método [IMAPIProp::SetProps](imapiprop-setprops.md) e, em seguida, chama **SaveChanges** novamente, a mesma implementação pode falhar.</span><span class="sxs-lookup"><span data-stu-id="9423e-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="9423e-163">Após receber MAPI_E_NO_ACCESS de uma chamada no qual você definiu KEEP_OPEN_READWRITE, continuará a ter permissão de leitura/gravação para o objeto.</span><span class="sxs-lookup"><span data-stu-id="9423e-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="9423e-164">É possível chamar **SaveChanges** novamente, passando o sinalizador KEEP_OPEN_READONLY ou sem sinalizadores com KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="9423e-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="9423e-165">Se um provedor suporta o sinalizador KEEP_OPEN_READWRITE depende da implementação do provedor.</span><span class="sxs-lookup"><span data-stu-id="9423e-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="9423e-166">Para indicar que a chamada apenas ser feitas no objeto após **SaveChanges** é **IUnknown:: Release**, não defina nenhum sinalizadores para o parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9423e-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="9423e-167">Um erro de **SaveChanges** indica que ele não pôde tornar as alterações pendentes permanente.</span><span class="sxs-lookup"><span data-stu-id="9423e-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="9423e-168">Provedores diferentes manipulam a ausência de sinalizadores na chamada **SaveChanges** de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="9423e-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="9423e-169">Alguns provedores tratam nesse estado da mesma forma KEEP_OPEN_READONLY; outros provedores interpretam o mesmo KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="9423e-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="9423e-170">Ainda outros provedores desligar o objeto quando não recebem sinalizadores na chamada **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="9423e-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="9423e-171">Algumas propriedades, normalmente computadas propriedades, não podem ser processadas até que se chame **SaveChanges** e, em alguns casos, a **versão**.</span><span class="sxs-lookup"><span data-stu-id="9423e-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="9423e-172">Quando você faz alterações em massa, como salvar anexos de várias mensagens, adie o erro de processamento, definindo o sinalizador MAPI_DEFERRED_ERRORS no _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="9423e-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="9423e-173">Se você salvar vários anexos para várias mensagens, fazer um **SaveChanges** chamada para cada anexo e um **SaveChanges** chamada a cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="9423e-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="9423e-174">Defina o sinalizador MAPI_DEFERRED_ERRORS para cada chamada de anexo e para todas as mensagens, exceto o último.</span><span class="sxs-lookup"><span data-stu-id="9423e-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="9423e-175">Se **SaveChanges** retornar MAPI_E_OBJECT_CHANGED, verifique se o objeto original foi modificado.</span><span class="sxs-lookup"><span data-stu-id="9423e-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="9423e-176">Em caso afirmativo, avise o usuário, que pode solicitar que as alterações sobrescrever as alterações anteriores ou salvar o objeto em outro local.</span><span class="sxs-lookup"><span data-stu-id="9423e-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="9423e-177">Se o objeto original tiver sido excluído, avise o usuário para fornecer-lhes a oportunidade de salvar o objeto em outro local.</span><span class="sxs-lookup"><span data-stu-id="9423e-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="9423e-178">Você não pode chamar **SaveChanges** com o sinalizador FORCE_SAVE em um objeto aberto que tenha sido excluído.</span><span class="sxs-lookup"><span data-stu-id="9423e-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="9423e-179">Se **SaveChanges** retornará um erro, o objeto cujas alterações foram salvos permanece aberto, independentemente dos sinalizadores definidos no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9423e-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9423e-180">O _ulFlags_ NON_EMS_XP_SAVE e SPAMFILTER_ONSAVE não podem ser definidos no arquivo de cabeçalho para download que você possui atualmente, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="9423e-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="9423e-181">Para obter mais informações, consulte [Salvar Propriedades de MAPI](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9423e-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9423e-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="9423e-182">See also</span></span>



[<span data-ttu-id="9423e-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="9423e-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="9423e-184">Propriedade canônico PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="9423e-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="9423e-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9423e-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="9423e-186">Salvar propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9423e-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

