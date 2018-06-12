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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e9d9ca56a877c0106c76242fe97ce43321e62e08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767542"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="c9787-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c9787-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="c9787-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9787-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9787-105">Abre uma pasta ou um objeto de mensagem e retorna um ponteiro para o objeto para fornecer mais acesso.</span><span class="sxs-lookup"><span data-stu-id="c9787-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="c9787-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="c9787-106">Parameters</span></span>

 <span data-ttu-id="c9787-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c9787-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c9787-108">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="c9787-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c9787-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c9787-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c9787-110">[in] Um ponteiro para o endereço do identificador de entrada do objeto folder ou a mensagem para abrir.</span><span class="sxs-lookup"><span data-stu-id="c9787-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="c9787-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c9787-111">_lpInterface_</span></span>
  
> <span data-ttu-id="c9787-112">[in] Um ponteiro para o identificador de interface (IID) para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c9787-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="c9787-113">Passar NULL indica que o objeto é convertido para a interface padrão para um objeto desse tipo.</span><span class="sxs-lookup"><span data-stu-id="c9787-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="c9787-114">O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c9787-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="c9787-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="c9787-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="c9787-116">[in] Uma bitmask dos sinalizadores que controla como o objeto é aberto.</span><span class="sxs-lookup"><span data-stu-id="c9787-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="c9787-117">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c9787-117">The following flags can be set:</span></span>
    
<span data-ttu-id="c9787-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c9787-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="c9787-119">O objeto deve ser aberto com as permissões máxima permitidas para o usuário e as permissões do aplicativo cliente máximo.</span><span class="sxs-lookup"><span data-stu-id="c9787-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="c9787-120">Por exemplo, se o cliente tem a permissão de leitura/gravação, o objeto é aberto com permissão de leitura/gravação; Se o cliente tem a permissão somente leitura, o objeto é aberto com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c9787-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="c9787-121">O cliente pode recuperar o nível de permissão, fazendo com que a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c9787-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="c9787-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c9787-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c9787-123">A chamada será autorizada de sucesso, mesmo se o objeto subjacente não está disponível para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="c9787-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="c9787-124">Se o objeto não estiver disponível, uma chamada subsequente ao objeto pode retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="c9787-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="c9787-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c9787-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="c9787-126">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="c9787-126">Requests read/write permission.</span></span> <span data-ttu-id="c9787-127">Por padrão, são criados objetos com permissão somente leitura e os clientes não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c9787-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="c9787-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="c9787-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="c9787-129">[out] Um ponteiro para o tipo de objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="c9787-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="c9787-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="c9787-130">_lppUnk_</span></span>
  
> <span data-ttu-id="c9787-131">[out] Um ponteiro para o ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="c9787-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c9787-132">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c9787-132">Return value</span></span>

<span data-ttu-id="c9787-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9787-133">S_OK</span></span> 
  
> <span data-ttu-id="c9787-134">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="c9787-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9787-135">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c9787-135">Remarks</span></span>

<span data-ttu-id="c9787-136">MAPI chama o método **IMSLogon::OpenEntry** para abrir uma pasta ou uma mensagem em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c9787-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="c9787-137">MAPI passa o identificador de entrada do objeto a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="c9787-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="c9787-138">O provedor de armazenamento de mensagem deve retornar um ponteiro que permite o acesso ao objeto especificado no parâmetro _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="c9787-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="c9787-139">Antes de chamadas de MAPI **IMSLogon::OpenEntry**, primeiro determina que o identificador de entrada da pasta ou determinada mensagem corresponde a um registrado por esse provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c9787-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="c9787-140">Para obter mais informações sobre como registrar os provedores de armazenamento de identificadores de entrada, consulte [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="c9787-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="c9787-141">**IMSLogon::OpenEntry** é idêntico ao método [IMsgStore::OpenEntry](imsgstore-openentry.md) do objeto de repositório de mensagem, exceto que o cliente não chamar **IMSLogon::OpenEntry**; As chamadas de MAPI **IMSLogon::OpenEntry** quando ele processa um método **IMAPISession::OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="c9787-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="c9787-142">Objetos abertos usando **IMSLogon::OpenEntry** devem ser tratados exatamente como objetos abertos usando a mensagem armazenam objeto; em particular, objetos abertos usando essa chamada devem ser invalidados quando o objeto de repositório da mensagem for lançado.</span><span class="sxs-lookup"><span data-stu-id="c9787-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9787-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9787-143">See also</span></span>



[<span data-ttu-id="c9787-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="c9787-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="c9787-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c9787-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="c9787-146">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9787-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

