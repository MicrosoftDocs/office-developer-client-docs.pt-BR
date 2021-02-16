---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416297"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="df97e-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="df97e-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="df97e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df97e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df97e-105">Abre uma pasta ou objeto message e retorna um ponteiro para o objeto para fornecer mais acesso.</span><span class="sxs-lookup"><span data-stu-id="df97e-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="df97e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df97e-106">Parameters</span></span>

 <span data-ttu-id="df97e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="df97e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="df97e-108">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="df97e-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="df97e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="df97e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="df97e-110">[in] Um ponteiro para o endereço do identificador de entrada do objeto de pasta ou mensagem a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="df97e-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="df97e-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="df97e-111">_lpInterface_</span></span>
  
> <span data-ttu-id="df97e-112">[in] Um ponteiro para o identificador de interface (IID) do objeto.</span><span class="sxs-lookup"><span data-stu-id="df97e-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="df97e-113">Passar NULL indica que o objeto é lançado para a interface padrão para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="df97e-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="df97e-114">O  _parâmetro lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto.</span><span class="sxs-lookup"><span data-stu-id="df97e-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="df97e-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="df97e-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="df97e-116">[in] Uma máscara de bits de sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="df97e-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="df97e-117">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="df97e-117">The following flags can be set:</span></span>
    
<span data-ttu-id="df97e-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="df97e-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="df97e-119">O objeto deve ser aberto com as permissões máximas permitidas para o usuário e o máximo de permissões do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="df97e-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="df97e-120">Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto será aberto com permissão de leitura/gravação; se o cliente tiver permissão somente leitura, o objeto será aberto com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="df97e-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="df97e-121">O cliente pode recuperar o nível de permissão, PR_ACCESS_LEVEL **propriedade** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="df97e-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="df97e-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="df97e-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="df97e-123">A chamada tem permissão para ser bem-sucedida, mesmo se o objeto subjacente não estiver disponível para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="df97e-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="df97e-124">Se o objeto não estiver disponível, uma chamada subsequente para o objeto poderá retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="df97e-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="df97e-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="df97e-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="df97e-126">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="df97e-126">Requests read/write permission.</span></span> <span data-ttu-id="df97e-127">Por padrão, os objetos são criados com permissão somente leitura e os clientes não devem trabalhar com a suposição de que a permissão de leitura/gravação foi concedida.</span><span class="sxs-lookup"><span data-stu-id="df97e-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="df97e-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="df97e-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="df97e-129">[out] Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="df97e-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="df97e-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="df97e-130">_lppUnk_</span></span>
  
> <span data-ttu-id="df97e-131">[out] Um ponteiro para o ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="df97e-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="df97e-132">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="df97e-132">Return value</span></span>

<span data-ttu-id="df97e-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="df97e-133">S_OK</span></span> 
  
> <span data-ttu-id="df97e-134">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="df97e-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df97e-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="df97e-135">Remarks</span></span>

<span data-ttu-id="df97e-136">O MAPI chama **o método IMSLogon::OpenEntry** para abrir uma pasta ou uma mensagem em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="df97e-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="df97e-137">O MAPI passa o identificador de entrada do objeto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="df97e-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="df97e-138">O provedor de armazenamento de mensagens deve retornar um ponteiro que permita mais acesso ao objeto especificado no _parâmetro lppUnk._</span><span class="sxs-lookup"><span data-stu-id="df97e-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="df97e-139">Antes de o MAPI chamar **IMSLogon::OpenEntry**, ele primeiro determina que o identificador de entrada de pasta ou mensagem determinado corresponde a um registrado por esse provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="df97e-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="df97e-140">Para obter mais informações sobre como os provedores de armazenamento registram identificadores de entrada, consulte [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="df97e-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="df97e-141">**IMSLogon::OpenEntry** é idêntico ao método [IMsgStore::OpenEntry](imsgstore-openentry.md) do objeto de repositório de mensagens, exceto que o cliente não chama **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span><span class="sxs-lookup"><span data-stu-id="df97e-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="df97e-142">Os objetos abertos usando **IMSLogon::OpenEntry** devem ser tratados exatamente como objetos abertos usando o objeto de armazenamento de mensagens; em particular, os objetos abertos usando essa chamada devem ser invalidados quando o objeto do armazenamento de mensagens é liberado.</span><span class="sxs-lookup"><span data-stu-id="df97e-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df97e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="df97e-143">See also</span></span>



[<span data-ttu-id="df97e-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="df97e-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="df97e-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="df97e-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="df97e-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="df97e-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

