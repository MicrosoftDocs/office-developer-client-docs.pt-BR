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
# <a name="imapipropsavechanges"></a><span data-ttu-id="ce52b-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="ce52b-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="ce52b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce52b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce52b-105">Torna permanente quaisquer alterações feitas a um objeto desde a última operação de salvamento.</span><span class="sxs-lookup"><span data-stu-id="ce52b-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ce52b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce52b-106">Parameters</span></span>

 <span data-ttu-id="ce52b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce52b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ce52b-108">no Uma bitmask de sinalizadores que controlam o que acontece com o objeto quando o método **IMAPIProp:: SaveChanges** é chamado.</span><span class="sxs-lookup"><span data-stu-id="ce52b-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="ce52b-109">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ce52b-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="ce52b-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="ce52b-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="ce52b-111">Indica que a mensagem não foi entregue de um servidor do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="ce52b-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="ce52b-112">Esse sinalizador deve ser usado em combinação com o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) e o sinalizador ITEMPROC_FORCE para indicar a um repositório PST que a mensagem está qualificada para o processamento de regras antes que o repositório de arquivos de pastas particulares (PST) Notifique qualquer cliente de escuta que a mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="ce52b-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="ce52b-113">Este processamento de regras só se aplica a novas mensagens criadas com o [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) em um servidor que não é um servidor Exchange, caso em que o servidor Exchange já tenha processado as regras da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ce52b-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="ce52b-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="ce52b-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="ce52b-115">As alterações devem ser gravadas no objeto, substituindo todas as alterações anteriores que foram feitas no objeto e o objeto deve ser fechado.</span><span class="sxs-lookup"><span data-stu-id="ce52b-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="ce52b-116">A permissão de leitura/gravação deve ser definida para que a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ce52b-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="ce52b-117">O sinalizador FORCE_SAVE é usado depois que uma chamada anterior a **SaveChanges** retornou MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="ce52b-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="ce52b-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="ce52b-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="ce52b-119">As alterações devem ser confirmadas e o objeto deve ser mantido aberto para leitura.</span><span class="sxs-lookup"><span data-stu-id="ce52b-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="ce52b-120">Nenhuma alteração adicional será feita.</span><span class="sxs-lookup"><span data-stu-id="ce52b-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="ce52b-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="ce52b-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="ce52b-122">As alterações devem ser confirmadas e o objeto deve ser mantido aberto para permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ce52b-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="ce52b-123">Normalmente, esse sinalizador é definido quando o objeto foi aberto pela primeira vez para permissões de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ce52b-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="ce52b-124">Alterações subsequentes no objeto são permitidas.</span><span class="sxs-lookup"><span data-stu-id="ce52b-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="ce52b-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ce52b-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ce52b-126">Permite que **SaveChanges** seja retornado com êxito, possivelmente antes de as alterações terem sido totalmente confirmadas.</span><span class="sxs-lookup"><span data-stu-id="ce52b-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="ce52b-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="ce52b-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="ce52b-128">Habilita a filtragem de spam em uma mensagem que está sendo salva.</span><span class="sxs-lookup"><span data-stu-id="ce52b-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="ce52b-129">O suporte à filtragem de spam está disponível somente se o tipo de endereço de email do remetente for SMTP(Simple Mail Transfer Protocol) e a mensagem estiver sendo salva em um repositório de um arquivo de pastas particulares (PST).</span><span class="sxs-lookup"><span data-stu-id="ce52b-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce52b-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ce52b-130">Return value</span></span>

<span data-ttu-id="ce52b-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce52b-131">S_OK</span></span> 
  
> <span data-ttu-id="ce52b-132">O compromisso das alterações foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ce52b-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="ce52b-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ce52b-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ce52b-134">**SaveChanges** não pode manter o objeto aberto para permissão somente leitura se KEEP_OPEN_READONLY estiver definido, ou permissão de leitura/gravação se KEEP_OPEN_READWRITE estiver definido.</span><span class="sxs-lookup"><span data-stu-id="ce52b-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="ce52b-135">Nenhuma alteração é confirmada.</span><span class="sxs-lookup"><span data-stu-id="ce52b-135">No changes are committed.</span></span> 
    
<span data-ttu-id="ce52b-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="ce52b-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="ce52b-137">O objeto foi alterado desde que foi aberto.</span><span class="sxs-lookup"><span data-stu-id="ce52b-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="ce52b-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="ce52b-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="ce52b-139">O objeto foi excluído desde que foi aberto.</span><span class="sxs-lookup"><span data-stu-id="ce52b-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce52b-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce52b-140">Remarks</span></span>

<span data-ttu-id="ce52b-141">O método **IMAPIProp:: SaveChanges** torna as alterações de propriedade permanentes para objetos que dão suporte ao modelo de transação de processamento, como mensagens, anexos, contêineres de catálogo de endereços e objetos de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ce52b-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="ce52b-142">Objetos que não dão suporte a transações, como pastas, repositórios de mensagens e seções de perfil, tornam as alterações permanentes imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ce52b-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="ce52b-143">Nenhuma chamada para **SaveChanges** é necessária.</span><span class="sxs-lookup"><span data-stu-id="ce52b-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="ce52b-144">Como os provedores de serviços não precisam gerar um identificador de entrada para seus objetos até que todas as propriedades tenham sido salvas, a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de um objeto pode não estar disponível até que o método **SaveChanges** foi chamado.</span><span class="sxs-lookup"><span data-stu-id="ce52b-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="ce52b-145">Alguns provedores esperam até que o sinalizador KEEP_OPEN_READONLY seja definido na chamada **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="ce52b-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="ce52b-146">KEEP_OPEN_READONLY indica que as alterações a serem salvas na chamada atual serão as últimas alterações que serão feitas no objeto.</span><span class="sxs-lookup"><span data-stu-id="ce52b-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="ce52b-147">Algumas implementações de repositório de mensagens não mostram mensagens recém-criadas em uma pasta até que um cliente salve as alterações de mensagens usando **SaveChanges** e libere os objetos de mensagem usando o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ce52b-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="ce52b-148">Além disso, algumas implementações de objeto não podem gerar uma propriedade **PR_ENTRYID** para um objeto recém-criado até que **SaveChanges** tenha sido chamado, e alguns podem fazer isso somente depois que **SaveChanges** tiver sido chamado usando o KEEP_OPEN_READONLY definido no _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="ce52b-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ce52b-149">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ce52b-149">Notes to implementers</span></span>

<span data-ttu-id="ce52b-150">Se você receber o sinalizador KEEP_OPEN_READONLY, terá a opção de deixar o acesso do objeto como leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ce52b-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="ce52b-151">No enTanto, um provedor nunca pode deixar um objeto em um estado somente leitura quando o sinalizador KEEP_OPEN_READWRITE é passado.</span><span class="sxs-lookup"><span data-stu-id="ce52b-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="ce52b-152">Quando um cliente salva vários anexos em várias mensagens, ele chama o método **SaveChanges** para todos os anexos e todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="ce52b-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="ce52b-153">Geralmente, os clientes definirão MAPI_DEFERRED_ERRORS para cada uma dessas chamadas, exceto para o último.</span><span class="sxs-lookup"><span data-stu-id="ce52b-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="ce52b-154">Você pode retornar erros com a última chamada ou chamadas anteriores.</span><span class="sxs-lookup"><span data-stu-id="ce52b-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="ce52b-155">Você pode até mesmo ignorar o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="ce52b-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="ce52b-156">Se KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY estiver definido junto com o MAPI_DEFERRED_ERRORS, você poderá ignorar a solicitação de diferimento de erro.</span><span class="sxs-lookup"><span data-stu-id="ce52b-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="ce52b-157">Se MAPI_DEFERRED_ERRORS não estiver definido no _parâmetroulflags_, um dos erros adiados anteriormente poderá ser retornado para a chamada **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="ce52b-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="ce52b-158">Se um provedor de transporte remoto fornece uma implementação funcional desse método é opcional e depende de outras escolhas de design na sua implementação.</span><span class="sxs-lookup"><span data-stu-id="ce52b-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="ce52b-159">Se você implementar esse método, faça-o de acordo com a documentação aqui.</span><span class="sxs-lookup"><span data-stu-id="ce52b-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="ce52b-160">Como objetos Folder e status objetos não são transacionados, no mínimo uma implementação de **SaveChanges** do provedor de transporte remoto deve retornar S_OK sem realmente realizar qualquer trabalho.</span><span class="sxs-lookup"><span data-stu-id="ce52b-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ce52b-161">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ce52b-161">Notes to callers</span></span>

<span data-ttu-id="ce52b-162">Se um cliente passar KEEP_OPEN_READONLY, chama o método [IMAPIProp::](imapiprop-setprops.md) SetProps e, em seguida, chama **SaveChanges** novamente, a mesma implementação pode falhar.</span><span class="sxs-lookup"><span data-stu-id="ce52b-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="ce52b-163">Após receber MAPI_E_NO_ACCESS de uma chamada na qual você definiu KEEP_OPEN_READWRITE, você continuará com permissão de leitura/gravação para o objeto.</span><span class="sxs-lookup"><span data-stu-id="ce52b-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="ce52b-164">Você pode chamar o **SaveChanges** novamente, passando o sinalizador KEEP_OPEN_READONLY ou nenhum sinalizador com KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="ce52b-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="ce52b-165">Se um provedor oferece suporte ao sinalizador KEEP_OPEN_READWRITE depende da implementação do provedor.</span><span class="sxs-lookup"><span data-stu-id="ce52b-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="ce52b-166">Para indicar que a única chamada a ser feita no objeto após **SaveChanges** é **IUnknown:: Release**, configure nenhum sinalizador para o parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="ce52b-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="ce52b-167">Um erro de **SaveChanges** indica que não foi possível tornar as alterações pendentes permanentes.</span><span class="sxs-lookup"><span data-stu-id="ce52b-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="ce52b-168">Diferentes provedores manipulam a ausência de sinalizadores na chamada **SaveChanges** de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="ce52b-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="ce52b-169">Alguns provedores tratam esse estado da mesma forma que KEEP_OPEN_READONLY; outros provedores interpretam o mesmo que KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="ce52b-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="ce52b-170">Ainda outros provedores desligam o objeto quando não recebem sinalizadores na chamada **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="ce52b-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="ce52b-171">Algumas propriedades, normalmente, Propriedades computadas, não podem ser processadas até que você chame **SaveChanges** e, em alguns casos, o **lançamento**.</span><span class="sxs-lookup"><span data-stu-id="ce52b-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="ce52b-172">Ao fazer alterações em massa, como salvar anexos em várias mensagens, adie o processamento de erro definindo o sinalizador MAPI_DEFERRED_ERRORS no _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="ce52b-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="ce52b-173">Se você salvar vários anexos em várias mensagens, faça uma chamada **SaveChanges** para cada anexo e uma chamada **SaveChanges** para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="ce52b-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="ce52b-174">Defina o sinalizador MAPI_DEFERRED_ERRORS para cada chamada de anexo e para todas as mensagens, exceto a última.</span><span class="sxs-lookup"><span data-stu-id="ce52b-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="ce52b-175">Se **SaveChanges** retornar MAPI_E_OBJECT_CHANGED, verifique se o objeto original foi modificado.</span><span class="sxs-lookup"><span data-stu-id="ce52b-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="ce52b-176">Em caso afirmativo, avise ao usuário que pode solicitar que as alterações substituam as alterações anteriores ou salvem o objeto em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="ce52b-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="ce52b-177">Se o objeto original tiver sido excluído, avise o usuário para dar a eles a oportunidade de salvar o objeto em outro local.</span><span class="sxs-lookup"><span data-stu-id="ce52b-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="ce52b-178">Você não pode chamar **SaveChanges** com o sinalizador FORCE_SAVE em um objeto Open que tenha sido excluído.</span><span class="sxs-lookup"><span data-stu-id="ce52b-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="ce52b-179">Se **SaveChanges** retornar um erro, o objeto cujas alterações foram salvas permanecerá aberto, independentemente dos sinalizadores definidos no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="ce52b-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ce52b-180">O _parâmetroulflags_ NON_EMS_XP_SAVE e o SPAMFILTER_ONSAVE podem não ser definidos no arquivo de cabeçalho baixável que você tem atualmente e, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="ce52b-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="ce52b-181">Para obter mais informações, consulte [salvar propriedades MAPI](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ce52b-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce52b-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce52b-182">See also</span></span>



[<span data-ttu-id="ce52b-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="ce52b-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="ce52b-184">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="ce52b-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="ce52b-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce52b-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="ce52b-186">Salvar propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ce52b-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

