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
ms.openlocfilehash: 27a5978d85cf06a31f583b82cd39d0001852876b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768177"
---
# <a name="openimsgonistg"></a><span data-ttu-id="43a27-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="43a27-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="43a27-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43a27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43a27-105">Cria um novo objeto [IMessage](imessageimapiprop.md) na parte superior de um objeto OLE **IStorage** existente, a ser usado em uma sessão de mensagem.</span><span class="sxs-lookup"><span data-stu-id="43a27-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="43a27-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="43a27-106">Header file:</span></span>  <br/> |<span data-ttu-id="43a27-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="43a27-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="43a27-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="43a27-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="43a27-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="43a27-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="43a27-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="43a27-110">Called by:</span></span>  <br/> |<span data-ttu-id="43a27-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="43a27-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="43a27-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43a27-112">Parameters</span></span>

<span data-ttu-id="43a27-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="43a27-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="43a27-114">[in] Ponteiro para um objeto de sessão de mensagem dentro do qual o novo **IMessage**objeto **|** - on - deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="43a27-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="43a27-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="43a27-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="43a27-116">[in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="43a27-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="43a27-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="43a27-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="43a27-118">[in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="43a27-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="43a27-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="43a27-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="43a27-120">[in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="43a27-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="43a27-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="43a27-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="43a27-122">[in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="43a27-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="43a27-123">A interface **IMessage** deve usar esse método de alocação ao trabalhar com interfaces como **IStorage** e **IStream**.</span><span class="sxs-lookup"><span data-stu-id="43a27-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="43a27-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="43a27-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="43a27-125">[in] Opcional ponteiro para um objeto de suporte MAPI que um provedor de serviços pode usar para chamar os métodos para o [IMAPISupport: IUnknown](imapisupportiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="43a27-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="43a27-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="43a27-126">_lpStg_</span></span>
  
> <span data-ttu-id="43a27-127">[além, out] Ponteiro para um objeto OLE **IStorage** que está aberta e somente leitura ou permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="43a27-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="43a27-128">Porque **IMessage** não oferece suporte para acesso somente gravação, **OpenIMsgOnIStg** não aceita um objeto de armazenamento aberto no modo somente gravação.</span><span class="sxs-lookup"><span data-stu-id="43a27-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="43a27-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="43a27-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="43a27-130">[in] Ponteiro opcional para uma função de retorno de chamada com base em protótipo [MSGCALLRELEASE](msgcallrelease.md) que MAPI deve chamar após a última versão em **IMessage**o objeto **|** - on.</span><span class="sxs-lookup"><span data-stu-id="43a27-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="43a27-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="43a27-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="43a27-132">[in] Dados do chamador salvo pelo MAPI com o objeto **|** **IMessage**- on - e passado para o **MSGCALLRELEASE** com base em função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="43a27-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="43a27-133">Os dados fornecem contexto sobre o objeto **IMessage** está sendo liberado e o objeto **|** na parte superior de qual ele foi criado.</span><span class="sxs-lookup"><span data-stu-id="43a27-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="43a27-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="43a27-134">_ulFlags_</span></span>
  
> <span data-ttu-id="43a27-135">[in] Bitmask dos sinalizadores utilizada para controlar se o método OLE **IStorage::Commit** é chamado quando o aplicativo cliente ou o provedor de serviço chama o método **IMessage::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="43a27-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="43a27-136">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="43a27-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="43a27-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="43a27-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="43a27-138">O método OLE **IStorage::Commit** não deve ser chamado quando o cliente ou o provedor chama [SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="43a27-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="43a27-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="43a27-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="43a27-140">Permite a criação de arquivos do. msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="43a27-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="43a27-141">O arquivo resultante de [IMessage](imessageimapiprop.md) mostra STORE_UNICODE_OK no seu [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) e oferece suporte a Unicode propriedades.</span><span class="sxs-lookup"><span data-stu-id="43a27-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="43a27-142">O sinalizador MAPI_UNICODE somente há suporte para essa função no Outlook 2003 ou superior.</span><span class="sxs-lookup"><span data-stu-id="43a27-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="43a27-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="43a27-143">_lppMsg_</span></span>
  
> <span data-ttu-id="43a27-144">[out] Ponteiro para um ponteiro para o objeto **IMessage** aberto.</span><span class="sxs-lookup"><span data-stu-id="43a27-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="43a27-145">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="43a27-145">Return value</span></span>

<span data-ttu-id="43a27-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="43a27-146">S_OK</span></span> 
  
> <span data-ttu-id="43a27-147">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="43a27-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43a27-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="43a27-148">Remarks</span></span>

<span data-ttu-id="43a27-149">Atributos de propriedade só podem ser acessados na propriedade objetos, ou seja, objetos Implementando o [IMAPIProp: IUnknown](imapipropiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="43a27-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="43a27-150">Para disponibilizar propriedades MAPI em um objeto de armazenamento estruturado OLE, **OpenIMsgOnIStg** cria um [IMessage: IMAPIProp](imessageimapiprop.md) objeto na parte superior do objeto OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="43a27-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="43a27-151">Os atributos de propriedade nesses objetos podem ser definidos ou alterados com [SetAttribIMsgOnIStg](setattribimsgonistg.md) e recuperados com [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="43a27-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="43a27-152">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="43a27-152">Notes to callers</span></span>

<span data-ttu-id="43a27-153">Uma sessão de mensagem deve ser aberta com [OpenIMsgSession](openimsgsession.md) antes de **OpenIMsgOnIStg** é chamado.</span><span class="sxs-lookup"><span data-stu-id="43a27-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="43a27-154">Fornecendo um parâmetro válido _lpMsgSess_ fazer sures a nova mensagem é criada dentro de uma sessão de mensagem, de modo que ela é fechada quando a sessão é fechada.</span><span class="sxs-lookup"><span data-stu-id="43a27-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="43a27-155">Se _lpMsgSess_ for NULL, a mensagem é criada, independentemente de qualquer sessão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="43a27-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="43a27-156">Se o aplicativo cliente ou o provedor de serviço que criou a mensagem não liberar a ele, bem como todos os seus respectivos anexos e abrir tabelas, memória tenha vazada e pode causar o aplicativo seja finalizado.</span><span class="sxs-lookup"><span data-stu-id="43a27-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="43a27-157">O MAPI usa as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação, especificamente para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="43a27-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="43a27-158">Os ponteiros _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ são opcionais quando a função **OpenIMsgOnIStg** é chamada com um parâmetro válido _lpMapiSup_ .</span><span class="sxs-lookup"><span data-stu-id="43a27-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="43a27-159">Porque ele está lidando com um objeto OLE subjacente, MAPI também precisa usar a alocação de memória do OLE.</span><span class="sxs-lookup"><span data-stu-id="43a27-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="43a27-160">Para obter mais informações sobre objetos de armazenamento estruturado OLE e alocação de memória do OLE, consulte a _referência do programador do OLE_.</span><span class="sxs-lookup"><span data-stu-id="43a27-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="43a27-161">Se um valor válido é fornecido para _lpMapiSup_, **IMessage** suporta os sinalizadores MAPI_DIALOG e ATTACH_DIALOG chamando o método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para fornecer uma interface do usuário de andamento para o [IMAPIProp::CopyTo](imapiprop-copyto.md) e os métodos [IMessage::DeleteAttach](imessage-deleteattach.md) .</span><span class="sxs-lookup"><span data-stu-id="43a27-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="43a27-162">Além disso, o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) tenta converter a curto prazo identificadores de entrada aos identificadores de entrada de longo prazo chamando o método [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) e fazendo chamadas sobre o objeto resultante de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="43a27-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="43a27-163">Se NULL é passado para _lpMapiSup_, **IMessage** ignora MAPI_DIALOG e ATTACH_DIALOG e armazena os identificadores de entrada de curto prazo sem a conversão.</span><span class="sxs-lookup"><span data-stu-id="43a27-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="43a27-164">O objeto **|** apontado pelo parâmetro _lpStg_ deve ser aberto no modo de STGM_READ ou STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="43a27-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="43a27-165">Se o modo STGM_READWRITE for usado, o modo STGM_TRANSACTED também deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="43a27-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="43a27-166">A função de retorno de chamada apontada pelo parâmetro _lpfMsgCallRelease_ é opcional. Se for fornecido, ele deve se basear o protótipo de função [MSGCALLRELEASE](msgcallrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="43a27-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="43a27-167">A interface **IMessage** chame quando a contagem de referência do objeto **IMessage**- on - **IStorage** está definida como zero pela última chamada para seu método de **lançamento** .</span><span class="sxs-lookup"><span data-stu-id="43a27-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="43a27-168">A função de retorno de chamada geralmente é usada para liberar a interface **IStorage** subjacente.</span><span class="sxs-lookup"><span data-stu-id="43a27-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="43a27-169">**IMessage** não tentará acessar o objeto **|** apontado pelo parâmetro _lpStg_ depois de fazer o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="43a27-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="43a27-170">Alguns clientes ou provedores podem gravar dados adicionais para o objeto **|** além quais **IMessage** próprio grava quando seu método [SaveChanges](imapiprop-savechanges.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="43a27-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="43a27-171">O cliente ou o provedor pode usar o sinalizador IMSG_NO_ISTG_COMMIT para impedir que **IMessage** chamar o método OLE **IStorage::Commit** durante o processamento de uma chamada **SaveChanges** ; Neste caso o cliente ou o provedor deve próprio confirmar o objeto **|** quando os dados adicionais serão gravados.</span><span class="sxs-lookup"><span data-stu-id="43a27-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="43a27-172">Para ajudar nisso, a implementação de **IMessage** garante nomear substorages todos, que ele cria o objeto **|** começando com a cadeia de caracteres _", ou seja, com dois sublinhados.</span><span class="sxs-lookup"><span data-stu-id="43a27-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="43a27-173">O cliente ou o provedor pode evitar conflitos de nome, mantendo os nomes de suas subarmazenamento sem esse namespace.</span><span class="sxs-lookup"><span data-stu-id="43a27-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="43a27-174">MAPI não define o comportamento das operações de abrir vários realizadas em um Subobjeto de uma mensagem, como um anexo, um fluxo ou uma mensagem incorporada.</span><span class="sxs-lookup"><span data-stu-id="43a27-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="43a27-175">MAPI atualmente permite um Subobjeto que já está aberto para ser aberto mais uma vez, mas MAPI executa a operação aberta com incrementar a contagem de referência para o objeto aberto existente e retorná-lo para o cliente ou o provedor que chamou o [IMessage::OpenAttach ](imessage-openattach.md)ou método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="43a27-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="43a27-176">Isso significa que o acesso solicitado para a operação de abertura primeira em um Subobjeto é o acesso fornecido para todas as operações de abrir subsequentes, independentemente do acesso solicitado pelas operações.</span><span class="sxs-lookup"><span data-stu-id="43a27-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="43a27-177">O procedimento correto para a inserção de uma mensagem em um anexo é chamar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com um identificador de interface de IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="43a27-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="43a27-178">**OpenProperty** atualmente também dá suporte à criação de anexos de mensagens disponíveis diretamente na interface OLE **IStorage** , ou seja, usando o identificador de interface IID_IStorage.</span><span class="sxs-lookup"><span data-stu-id="43a27-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="43a27-179">Acesso de **IStorage** é suportado para permitir uma maneira fácil de colocar um documento do Microsoft Word em um anexo sem convertê-lo ou para a interface **IStream** do OLE.</span><span class="sxs-lookup"><span data-stu-id="43a27-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="43a27-180">No entanto, **IMessage** podem não se comportar previsibilidade se **OpenIMsgOnIStg** é passado um ponteiro **IStorage** para os dados do anexo e, em seguida, os objetos são lançados na ordem errada.</span><span class="sxs-lookup"><span data-stu-id="43a27-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="43a27-181">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="43a27-181">MFCMAPI reference</span></span>

<span data-ttu-id="43a27-182">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="43a27-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="43a27-183">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="43a27-183">**File**</span></span>|<span data-ttu-id="43a27-184">**Function**</span><span class="sxs-lookup"><span data-stu-id="43a27-184">**Function**</span></span>|<span data-ttu-id="43a27-185">**Comment**</span><span class="sxs-lookup"><span data-stu-id="43a27-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43a27-186">CPP</span><span class="sxs-lookup"><span data-stu-id="43a27-186">File.cpp</span></span>  <br/> |<span data-ttu-id="43a27-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="43a27-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="43a27-188">MFCMAPI usa o método **OpenIMsgOnIStg** para abrir uma interface IMessage na parte superior do. MSG de arquivo para que o arquivo pode ser manipulado com MAPI.</span><span class="sxs-lookup"><span data-stu-id="43a27-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43a27-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="43a27-189">See also</span></span>

- [<span data-ttu-id="43a27-190">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="43a27-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

