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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316629"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="8b4aa-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8b4aa-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="8b4aa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b4aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b4aa-105">Faz alterações permanentes que foram feitas em um objeto desde a última operação de salvar.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8b4aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b4aa-106">Parameters</span></span>

 <span data-ttu-id="8b4aa-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b4aa-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8b4aa-108">[in] Uma máscara de bits de sinalizadores que controla o que acontece com o objeto quando o método **IMAPIProp::SaveChanges** é chamado.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="8b4aa-109">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="8b4aa-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="8b4aa-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="8b4aa-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="8b4aa-111">Indica que a mensagem não foi entregue de um Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="8b4aa-112">Esse sinalizador deve ser usado em combinação com o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) e o sinalizador ITEMPROC_FORCE para indicar a um armazenamento PST que a mensagem está qualificada para processamento de regras antes que o armazenamento do arquivo de Pastas Particulares (PST) notifique qualquer cliente ouvinte de que a mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="8b4aa-113">Esse processamento de regras só se aplica a novas mensagens criadas com [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) em um servidor que não seja um Exchange Server. Nesse caso, o Exchange Server já teria processado regras na mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="8b4aa-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="8b4aa-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="8b4aa-115">As alterações devem ser escritas no objeto, substituindo quaisquer alterações anteriores feitas no objeto, e o objeto deve ser fechado.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="8b4aa-116">A permissão de leitura/gravação deve ser definida para que a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="8b4aa-117">O FORCE_SAVE sinalizador é usado após uma chamada anterior para **SaveChanges** retornada MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="8b4aa-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="8b4aa-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="8b4aa-119">As alterações devem ser comprometidas e o objeto deve ser mantido aberto para leitura.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="8b4aa-120">Nenhuma alteração adicional será feita.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="8b4aa-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="8b4aa-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="8b4aa-122">As alterações devem ser comprometidas e o objeto deve ser mantido aberto para permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="8b4aa-123">Esse sinalizador geralmente é definido quando o objeto foi aberto pela primeira vez para permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="8b4aa-124">Alterações subsequentes no objeto são permitidas.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="8b4aa-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8b4aa-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8b4aa-126">Permite que **SaveChanges** retorne com êxito, possivelmente antes que as alterações tenham sido totalmente comprometidas.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="8b4aa-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="8b4aa-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="8b4aa-128">Habilita a filtragem de spam em uma mensagem que está sendo salva.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="8b4aa-129">O suporte à filtragem de spam está disponível somente se o tipo de endereço de email do remetente for SMTP(Simple Mail Transfer Protocol) e a mensagem estiver sendo salva em um repositório de um arquivo de pastas particulares (PST).</span><span class="sxs-lookup"><span data-stu-id="8b4aa-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b4aa-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8b4aa-130">Return value</span></span>

<span data-ttu-id="8b4aa-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b4aa-131">S_OK</span></span> 
  
> <span data-ttu-id="8b4aa-132">O compromisso das alterações foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="8b4aa-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8b4aa-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8b4aa-134">**SaveChanges** não poderá manter o objeto aberto para permissão somente leitura se KEEP_OPEN_READONLY estiver definida ou permissão de leitura/gravação se KEEP_OPEN_READWRITE estiver definida.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="8b4aa-135">Nenhuma alteração foi comprometida.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-135">No changes are committed.</span></span> 
    
<span data-ttu-id="8b4aa-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="8b4aa-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="8b4aa-137">O objeto foi alterado desde que foi aberto.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="8b4aa-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="8b4aa-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="8b4aa-139">O objeto foi excluído desde que foi aberto.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b4aa-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b4aa-140">Remarks</span></span>

<span data-ttu-id="8b4aa-141">O **método IMAPIProp::SaveChanges** torna as alterações de propriedade permanentes para objetos que suportam o modelo de transação de processamento, como mensagens, anexos, contêineres de livro de endereços e objetos de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="8b4aa-142">Os objetos que não suportam transações, como pastas, armazenamentos de mensagens e seções de perfil, fazem alterações permanentemente imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="8b4aa-143">Nenhuma chamada **para SaveChanges** é necessária.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="8b4aa-144">Como os provedores de serviços não precisarão gerar um identificador de entrada para seus objetos até que todas as propriedades tenham sido salvas, a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de um objeto pode não estar disponível até que o método **SaveChanges** tenha sido chamado.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="8b4aa-145">Alguns provedores aguardam até que KEEP_OPEN_READONLY sinalizador seja definido na **chamada SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="8b4aa-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="8b4aa-146">KEEP_OPEN_READONLY indica que as alterações a serem salvas na chamada atual serão as últimas alterações que serão feitas no objeto.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="8b4aa-147">Algumas implementações de armazenamento de mensagens não mostram mensagens recém-criadas em uma pasta até que um cliente salve as alterações de mensagem usando **SaveChanges** e libere os objetos de mensagem usando o método [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b4aa-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="8b4aa-148">Além disso, algumas implementações de objeto não podem gerar uma propriedade PR_ENTRYID para um objeto recém-criado até que **SaveChanges** tenha sido chamado, e algumas podem fazer isso somente depois que **SaveChanges** tiver sido chamado usando um conjunto de **KEEP_OPEN_READONLY** em _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8b4aa-149">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="8b4aa-149">Notes to implementers</span></span>

<span data-ttu-id="8b4aa-150">Se você receber o KEEP_OPEN_READONLY sinalizador, terá a opção de deixar o acesso do objeto como leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="8b4aa-151">No entanto, um provedor nunca pode deixar um objeto em um estado somente leitura quando o sinalizador KEEP_OPEN_READWRITE é passado.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="8b4aa-152">Quando um cliente salva vários anexos em várias mensagens, ele chama o **método SaveChanges** para cada anexo e cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="8b4aa-153">Muitas vezes, os clientes MAPI_DEFERRED_ERRORS para cada uma dessas chamadas, exceto para a última.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="8b4aa-154">Você pode retornar erros com a última chamada ou chamadas anteriores.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="8b4aa-155">Você pode até ignorar o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="8b4aa-156">Se o KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY for definido junto com o MAPI_DEFERRED_ERRORS, você poderá ignorar a solicitação de adiamento de erro.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="8b4aa-157">Se MAPI_DEFERRED_ERRORS não estiver definido em _ulFlags_, um dos erros adiados anteriormente poderá ser retornado para a **chamada SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="8b4aa-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="8b4aa-158">Se um provedor de transporte remoto fornece uma implementação funcional desse método é opcional e depende de outras opções de design em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="8b4aa-159">Se você implementar esse método, faça isso de acordo com a documentação aqui.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="8b4aa-160">Como os objetos de pasta e os objetos de status não são transacionados, no mínimo a implementação do **SaveChanges** de um provedor de transporte remoto deve retornar S_OK sem realmente fazer qualquer trabalho.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8b4aa-161">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="8b4aa-161">Notes to callers</span></span>

<span data-ttu-id="8b4aa-162">Se um cliente passar KEEP_OPEN_READONLY, chamar o método [IMAPIProp::SetProps](imapiprop-setprops.md) e chamar **SaveChanges** novamente, a mesma implementação poderá falhar.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="8b4aa-163">Depois de MAPI_E_NO_ACCESS de uma chamada na qual você definiu KEEP_OPEN_READWRITE, você continuará a ter permissão de leitura/gravação para o objeto.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="8b4aa-164">Você pode chamar **SaveChanges** novamente, passando o sinalizador KEEP_OPEN_READONLY ou nenhum sinalizador com KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="8b4aa-165">Se um provedor oferece suporte KEEP_OPEN_READWRITE sinalizador depende da implementação do provedor.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="8b4aa-166">Para indicar que a única chamada a ser feita no objeto após **SaveChanges** é **IUnknown::Release**, não defina sinalizadores para o _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="8b4aa-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="8b4aa-167">Um erro de **SaveChanges** indica que não foi possível tornar permanentes as alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="8b4aa-168">Provedores diferentes lidam com a ausência de sinalizadores na chamada **SaveChanges** de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="8b4aa-169">Alguns provedores tratam esse estado da mesma forma que KEEP_OPEN_READONLY; outros provedores o interpretam da mesma forma que KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="8b4aa-170">Ainda outros provedores desligaram o objeto quando não recebem sinalizadores na **chamada SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="8b4aa-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="8b4aa-171">Algumas propriedades, normalmente computadas, não podem ser processadas até que você chame **SaveChanges** e, em alguns casos, **Release**.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="8b4aa-172">Ao fazer alterações em massa, como salvar anexos em várias mensagens, adia o processamento de erros definindo o sinalizador MAPI_DEFERRED_ERRORS em  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="8b4aa-173">Se você salvar vários anexos em várias mensagens, faça uma chamada **SaveChanges** para cada anexo e uma **chamada SaveChanges** para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="8b4aa-174">De definida a MAPI_DEFERRED_ERRORS sinalizador para cada chamada de anexo e para todas as mensagens, exceto a última.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="8b4aa-175">Se **SaveChanges** retornar MAPI_E_OBJECT_CHANGED, verifique se o objeto original foi modificado.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="8b4aa-176">Nesse caso, avise o usuário, que pode solicitar que as alterações sobrescrevem as alterações anteriores ou salve o objeto em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="8b4aa-177">Se o objeto original tiver sido excluído, avise o usuário para dar a ele a oportunidade de salvar o objeto em outro local.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="8b4aa-178">Você não pode **chamar SaveChanges** com o FORCE_SAVE sinalizador em um objeto aberto que foi excluído.</span><span class="sxs-lookup"><span data-stu-id="8b4aa-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="8b4aa-179">Se **SaveChanges** retornar um erro, o objeto cujas alterações devem ser salvas permanece aberto, independentemente dos sinalizadores definidos no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="8b4aa-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8b4aa-180">O  _ulFlags_ NON_EMS_XP_SAVE e SPAMFILTER_ONSAVE podem não ser definidos no arquivo de header baixável que você tem atualmente, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="8b4aa-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="8b4aa-181">Para obter mais informações, consulte [Salvar propriedades MAPI](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="8b4aa-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b4aa-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b4aa-182">See also</span></span>



[<span data-ttu-id="8b4aa-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="8b4aa-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="8b4aa-184">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="8b4aa-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="8b4aa-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b4aa-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="8b4aa-186">Salvando propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8b4aa-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

