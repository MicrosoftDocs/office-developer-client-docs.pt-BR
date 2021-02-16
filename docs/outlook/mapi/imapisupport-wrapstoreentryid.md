---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430445"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="e3195-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="e3195-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="e3195-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3195-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3195-105">Converte o identificador de entrada interno de um armazenamento de mensagens em um identificador de entrada no formato padrão MAPI.</span><span class="sxs-lookup"><span data-stu-id="e3195-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="e3195-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3195-106">Parameters</span></span>

 <span data-ttu-id="e3195-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="e3195-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="e3195-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpOrigEntry._</span><span class="sxs-lookup"><span data-stu-id="e3195-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="e3195-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="e3195-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="e3195-110">[in] Um ponteiro para o identificador de entrada privada para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e3195-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="e3195-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="e3195-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="e3195-112">[out] Um ponteiro para a contagem de byte no identificador de entrada apontado pelo parâmetro _lppWrappedEntry._</span><span class="sxs-lookup"><span data-stu-id="e3195-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="e3195-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="e3195-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="e3195-114">[out] Um ponteiro para um ponteiro para o identificador de entrada com fim.</span><span class="sxs-lookup"><span data-stu-id="e3195-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e3195-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3195-115">Return value</span></span>

<span data-ttu-id="e3195-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3195-116">S_OK</span></span> 
  
> <span data-ttu-id="e3195-117">O identificador de entrada foi empacotado com êxito.</span><span class="sxs-lookup"><span data-stu-id="e3195-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3195-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3195-118">Remarks</span></span>

<span data-ttu-id="e3195-119">O **método IMAPISupport::WrapStoreEntryID** é implementado para todos os objetos de suporte do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e3195-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="e3195-120">Os provedores de serviços usam **WrapStoreEntryID** para que o MAPI gere um identificador de entrada para um repositório de mensagens que quebra o identificador de entrada interno do repositório.</span><span class="sxs-lookup"><span data-stu-id="e3195-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e3195-121">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e3195-121">Notes to callers</span></span>

<span data-ttu-id="e3195-122">Quando um cliente chama o método [IMAPIProp::GetProps](imapiprop-getprops.md) do repositório de mensagens para recuperar sua propriedade **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)), e seu repositório de mensagens usa um identificador de entrada em um formato privado, chame **WrapStoreEntryID** e retorne o identificador de entrada apontado pelo parâmetro _lppWrappedEntry._</span><span class="sxs-lookup"><span data-stu-id="e3195-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="e3195-123">Chamadas para os métodos [IMSProvider::Logon](imsprovider-logon.md) e [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) sempre obtém o identificador de entrada privada do armazenamento; a versão empacotada é usada somente entre aplicativos cliente e MAPI.</span><span class="sxs-lookup"><span data-stu-id="e3195-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="e3195-124">Liberar a memória para o identificador de entrada apontado pelo parâmetro  _lppWrappedEntry_ usando a função [MAPIFreeBuffer](mapifreebuffer.md) quando terminar de usar o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e3195-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e3195-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3195-125">See also</span></span>



[<span data-ttu-id="e3195-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e3195-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="e3195-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e3195-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="e3195-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e3195-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="e3195-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="e3195-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="e3195-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e3195-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e3195-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3195-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

