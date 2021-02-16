---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406518"
---
# <a name="openimsgonistg"></a><span data-ttu-id="eb263-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="eb263-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="eb263-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb263-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb263-105">Cria um novo [objeto IMessage](imessageimapiprop.md) sobre um objeto **IStorage** OLE existente, a ser usado em uma sessão de mensagem.</span><span class="sxs-lookup"><span data-stu-id="eb263-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb263-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="eb263-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb263-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="eb263-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="eb263-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="eb263-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eb263-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eb263-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eb263-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="eb263-110">Called by:</span></span>  <br/> |<span data-ttu-id="eb263-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="eb263-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a><span data-ttu-id="eb263-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb263-112">Parameters</span></span>

<span data-ttu-id="eb263-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="eb263-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="eb263-114">[in] Ponteiro para um objeto de sessão de mensagem dentro do qual o novo objeto **IMessage** **-on-IStorage** deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="eb263-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="eb263-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="eb263-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="eb263-116">[in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="eb263-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="eb263-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="eb263-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="eb263-118">[in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="eb263-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="eb263-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="eb263-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="eb263-120">[in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="eb263-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="eb263-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="eb263-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="eb263-122">[in] Ponteiro para um objeto alocador de memória expondo a interface **IMalloc OLE.**</span><span class="sxs-lookup"><span data-stu-id="eb263-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="eb263-123">A interface **IMessage** precisa usar esse método de alocação ao trabalhar com interfaces como **IStorage** e **IStream**.</span><span class="sxs-lookup"><span data-stu-id="eb263-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="eb263-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="eb263-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="eb263-125">[in] Ponteiro opcional para um objeto de suporte MAPI que um provedor de serviços pode usar para chamar os métodos da interface [IMAPISupport : IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="eb263-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="eb263-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="eb263-126">_lpStg_</span></span>
  
> <span data-ttu-id="eb263-127">[in, out] Ponteiro para um objeto **IStorage** OLE que está aberto e tem permissão somente leitura ou leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="eb263-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="eb263-128">Como **o IMessage** não dá suporte ao acesso somente gravação, **o OpenIMsgOnIStg** não aceita um objeto de armazenamento aberto no modo somente gravação.</span><span class="sxs-lookup"><span data-stu-id="eb263-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="eb263-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="eb263-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="eb263-130">[in] Ponteiro opcional para uma função de retorno de chamada com base no protótipo [MSGCALLRELEASE](msgcallrelease.md) que o MAPI deve chamar seguindo a última versão no objeto **IMessage**-on-IStorage. </span><span class="sxs-lookup"><span data-stu-id="eb263-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="eb263-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="eb263-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="eb263-132">[in] Dados do chamador salvos por MAPI com o objeto **IMessage** **-on-IStorage** e passados para a função de retorno de chamada baseada em **MSGCALLRELEASE.**</span><span class="sxs-lookup"><span data-stu-id="eb263-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="eb263-133">Os dados proporcionam contexto sobre o objeto **IMessage** que está sendo liberado e o objeto **IStorage** sobre o qual ele foi criado.</span><span class="sxs-lookup"><span data-stu-id="eb263-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="eb263-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eb263-134">_ulFlags_</span></span>
  
> <span data-ttu-id="eb263-135">[in] Bitmask de sinalizadores usados para controlar se o método **OLE IStorage::Commit** é chamado quando o aplicativo cliente ou provedor de serviços chama o método **IMessage::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="eb263-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="eb263-136">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="eb263-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="eb263-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="eb263-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="eb263-138">O método OLE **IStorage::Commit** não deve ser chamado quando o cliente ou provedor chamar [SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="eb263-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="eb263-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eb263-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="eb263-140">Habilita a criação de arquivos .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb263-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="eb263-141">O arquivo [IMessage](imessageimapiprop.md) resultante mostra STORE_UNICODE_OK em sua [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) e dá suporte a propriedades Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb263-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="eb263-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span><span class="sxs-lookup"><span data-stu-id="eb263-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="eb263-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="eb263-143">_lppMsg_</span></span>
  
> <span data-ttu-id="eb263-144">[out] Ponteiro para um ponteiro para o objeto **IMessage** aberto.</span><span class="sxs-lookup"><span data-stu-id="eb263-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eb263-145">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="eb263-145">Return value</span></span>

<span data-ttu-id="eb263-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb263-146">S_OK</span></span> 
  
> <span data-ttu-id="eb263-147">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="eb263-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb263-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb263-148">Remarks</span></span>

<span data-ttu-id="eb263-149">Atributos de propriedade só podem ser acessados em objetos de propriedade, ou seja, objetos que implementam o [IMAPIProp : interface IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="eb263-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="eb263-150">Para disponibilizar propriedades MAPI em um objeto de armazenamento estruturado OLE, **OpenIMsgOnIStg** cria um [IMessage : objeto IMAPIProp](imessageimapiprop.md) sobre o objeto **IStorage** OLE.</span><span class="sxs-lookup"><span data-stu-id="eb263-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="eb263-151">Os atributos de propriedade nesses objetos podem ser definidos ou alterados com [SetAttribIMsgOnIStg](setattribimsgonistg.md) e recuperados com [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="eb263-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eb263-152">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="eb263-152">Notes to callers</span></span>

<span data-ttu-id="eb263-153">Uma sessão de mensagem deve ser aberta com [OpenIMsgSession](openimsgsession.md) antes de **OpenIMsgOnIStg** ser chamado.</span><span class="sxs-lookup"><span data-stu-id="eb263-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="eb263-154">Fornecer um parâmetro  _lpMsgSess_ válido garante que a nova mensagem seja criada dentro de uma sessão de mensagem para que ela seja fechada quando a sessão for fechada.</span><span class="sxs-lookup"><span data-stu-id="eb263-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="eb263-155">Se  _lpMsgSess_ for NULL, a mensagem será criada independentemente de qualquer sessão de mensagem.</span><span class="sxs-lookup"><span data-stu-id="eb263-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="eb263-156">Se o aplicativo cliente ou provedor de serviços que criou a mensagem não a liberar, bem como todos os seus anexos e tabelas abertas, a memória será vazada e poderá fazer com que o aplicativo seja encerrado.</span><span class="sxs-lookup"><span data-stu-id="eb263-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="eb263-157">MAPI uses the functions pointed to  _by lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such [as IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="eb263-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="eb263-158">Os  _ponteiros lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ são opcionais quando a função **OpenIMsgOnIStg** é chamada com um parâmetro  _lpMapiSup_ válido.</span><span class="sxs-lookup"><span data-stu-id="eb263-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="eb263-159">Como ele está lidando com um objeto OLE subjacente, o MAPI também precisa usar a alocação de memória OLE.</span><span class="sxs-lookup"><span data-stu-id="eb263-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="eb263-160">Para obter mais informações sobre objetos de armazenamento estruturado OLE e alocação de memória OLE, consulte a _Referência do programador OLE._</span><span class="sxs-lookup"><span data-stu-id="eb263-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="eb263-161">Se um valor válido for fornecido para _lpMapiSup_, **IMessage** suportará os sinalizadores MAPI_DIALOG e ATTACH_DIALOG chamando o método [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para fornecer uma interface de usuário de progresso para os métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMessage::D eleteAttach.](imessage-deleteattach.md)</span><span class="sxs-lookup"><span data-stu-id="eb263-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="eb263-162">Além disso, o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) tenta converter identificadores de entrada de curto prazo em identificadores de entrada de longo prazo chamando o método [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) e fazendo chamadas no objeto de agendamento de endereço resultante.</span><span class="sxs-lookup"><span data-stu-id="eb263-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="eb263-163">Se NULL for passado para  _lpMapiSup_, **IMessage** ignorará MAPI_DIALOG e ATTACH_DIALOG e armazenará identificadores de entrada de curto prazo sem conversão.</span><span class="sxs-lookup"><span data-stu-id="eb263-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="eb263-164">O **objeto IStorage** apontado pelo parâmetro  _lpStg_ deve ser aberto no modo de STGM_READ ou STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="eb263-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="eb263-165">Se o STGM_READWRITE padrão for usado, o modo STGM_TRANSACTED também deverá ser definido.</span><span class="sxs-lookup"><span data-stu-id="eb263-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="eb263-166">A função de retorno de chamada apontada pelo _parâmetro lpfMsgCallRelease_ é opcional; se fornecido, ele deve ser baseado no protótipo [de função MSGCALLRELEASE.](msgcallrelease.md)</span><span class="sxs-lookup"><span data-stu-id="eb263-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="eb263-167">A interface **IMessage** a chama quando a contagem de referência do objeto **IMessage**-on-IStorage é definida como zero pela última chamada para seu **método Release.** </span><span class="sxs-lookup"><span data-stu-id="eb263-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="eb263-168">A função de retorno de chamada normalmente é usada para liberar a interface **IStorage** subjacente.</span><span class="sxs-lookup"><span data-stu-id="eb263-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="eb263-169">**IMessage** não tentará acessar o objeto **IStorage** apontado pelo parâmetro  _lpStg_ depois de fazer o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="eb263-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="eb263-170">Alguns clientes ou provedores podem gravar dados adicionais no objeto **IStorage** além do que o **próprio IMessage** grava quando seu [método SaveChanges](imapiprop-savechanges.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="eb263-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="eb263-171">O cliente ou provedor pode usar o sinalizador IMSG_NO_ISTG_COMMIT para impedir que **IMessage** chame o método **OLE IStorage::Commit** durante o processamento de uma **chamada SaveChanges;** nesse caso, o cliente ou provedor deve próprio comprometer o **objeto IStorage** quando os dados adicionais são gravados.</span><span class="sxs-lookup"><span data-stu-id="eb263-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="eb263-172">Para ajudar nisso, a implementação **IMessage** garante nomear todas as substorages que cria no objeto **IStorage** começando com a cadeia de caracteres "__", ou seja, com dois sublinhados.</span><span class="sxs-lookup"><span data-stu-id="eb263-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="eb263-173">O cliente ou provedor pode evitar colisões de nomes mantendo seus nomes de substoragem fora desse namespace.</span><span class="sxs-lookup"><span data-stu-id="eb263-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="eb263-174">O MAPI não define o comportamento de várias operações abertas executadas em um subobjeto de uma mensagem, como um anexo, um fluxo ou uma mensagem incorporada.</span><span class="sxs-lookup"><span data-stu-id="eb263-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="eb263-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span><span class="sxs-lookup"><span data-stu-id="eb263-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="eb263-176">Isso significa que o acesso solicitado para a primeira operação de abertura em um subobjeto é o acesso fornecido para todas as operações abertas subsequentes, independentemente do acesso solicitado pelas operações.</span><span class="sxs-lookup"><span data-stu-id="eb263-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="eb263-177">O procedimento correto para colocar uma mensagem em um anexo é chamar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com um identificador de interface de IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="eb263-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="eb263-178">**OpenProperty** atualmente também oferece suporte à criação de anexos de mensagem disponíveis diretamente na interface **IStorage** OLE, ou seja, usando o identificador IID_IStorage interface.</span><span class="sxs-lookup"><span data-stu-id="eb263-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="eb263-179">**O acesso a IStorage** é suportado para permitir uma maneira fácil de colocar um documento do Microsoft Word em um anexo sem convertê-lo para ou da interface **IStream** OLE.</span><span class="sxs-lookup"><span data-stu-id="eb263-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="eb263-180">No entanto, **IMessage** pode não se comportar de forma previsível se **OpenIMsgOnIStg** for passado um ponteiro **IStorage** para os dados do anexo e, em seguida, os objetos são liberados na ordem errada.</span><span class="sxs-lookup"><span data-stu-id="eb263-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eb263-181">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="eb263-181">MFCMAPI reference</span></span>

<span data-ttu-id="eb263-182">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb263-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eb263-183">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="eb263-183">**File**</span></span>|<span data-ttu-id="eb263-184">**Função**</span><span class="sxs-lookup"><span data-stu-id="eb263-184">**Function**</span></span>|<span data-ttu-id="eb263-185">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="eb263-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eb263-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="eb263-186">File.cpp</span></span>  <br/> |<span data-ttu-id="eb263-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="eb263-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="eb263-188">MFCMAPI usa **o método OpenIMsgOnIStg** para abrir uma interface IMessage sobre o . Arquivo MSG para que o arquivo possa ser manipulado com MAPI.</span><span class="sxs-lookup"><span data-stu-id="eb263-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb263-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb263-189">See also</span></span>

- [<span data-ttu-id="eb263-190">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="eb263-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

