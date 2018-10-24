---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1526ed54fd3773856b009c7c3570064f5a66df28
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594940"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="ca7aa-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="ca7aa-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="ca7aa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca7aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca7aa-105">Cria um identificador de entrada para um endereço one-off.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-105">Creates an entry identifier for a one-off address.</span></span>
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="ca7aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca7aa-106">Parameters</span></span>

 <span data-ttu-id="ca7aa-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="ca7aa-107">_lpszName_</span></span>
  
> <span data-ttu-id="ca7aa-108">[in] Um ponteiro para o nome de exibição do destinatário a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ca7aa-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="ca7aa-109">O parâmetro _lpszName_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ca7aa-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="ca7aa-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="ca7aa-111">[in] Um ponteiro para o tipo de endereço (por exemplo, FAX, SMTP ou X500) do destinatário.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="ca7aa-112">O parâmetro _lpszAdrType_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="ca7aa-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="ca7aa-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="ca7aa-114">[in] Um ponteiro para o endereço de mensagens do destinatário.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="ca7aa-115">O parâmetro _lpszAddress_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="ca7aa-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca7aa-116">_ulFlags_</span></span>
  
> <span data-ttu-id="ca7aa-117">[in] Uma bitmask dos sinalizadores que afeta o destinatário único.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="ca7aa-118">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ca7aa-118">The following flags can be set:</span></span>
    
<span data-ttu-id="ca7aa-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="ca7aa-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="ca7aa-120">O destinatário não pode manipular o conteúdo da mensagem formatada.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="ca7aa-121">Se MAPI_SEND_NO_RICH_INFO for definido, o MAPI define a propriedade de **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como FALSE.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="ca7aa-122">Se MAPI_SEND_NO_RICH_INFO não estiver definida, o MAPI define essa propriedade como TRUE, a menos que o endereço do destinatário mensagens apontado pela _lpszAddress_ é interpretado como um endereço de Internet.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="ca7aa-123">Nesse caso, MAPI define **PR_SEND_RICH_INFO** como FALSE.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="ca7aa-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ca7aa-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ca7aa-125">O nome para exibição, tipo de endereço e endereço estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="ca7aa-126">Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ca7aa-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ca7aa-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="ca7aa-128">[out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="ca7aa-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ca7aa-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="ca7aa-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="ca7aa-130">[out] Um ponteiro para um ponteiro para o identificador de entrada para o destinatário único.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca7aa-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ca7aa-131">Return value</span></span>

<span data-ttu-id="ca7aa-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca7aa-132">S_OK</span></span> 
  
> <span data-ttu-id="ca7aa-133">O identificador de entrada únicos foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca7aa-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca7aa-134">Remarks</span></span>

<span data-ttu-id="ca7aa-135">O método **IMAPISupport::CreateOneOff** é implementado para todos os objetos de suporte de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="ca7aa-136">Provedores de serviços de chamarem **CreateOneOff** para criar um identificador de entrada para um destinatário único (um destinatário que não pertençam a qualquer um dos contêineres de qualquer um dos provedores de catálogo de endereços carregado no momento).</span><span class="sxs-lookup"><span data-stu-id="ca7aa-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ca7aa-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ca7aa-137">Notes to callers</span></span>

<span data-ttu-id="ca7aa-138">Quando tiver terminado, usando o identificador de entrada retornado por **CreateOneOff**, libere a memória alocada para o identificador de entrada usando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ca7aa-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="ca7aa-139">Observações para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="ca7aa-139">Notes to Transport Providers</span></span>

<span data-ttu-id="ca7aa-140">Suportar o TNEF Transport Neutral Encapsulation Format () e use o valor da propriedade **PR_SEND_RICH_INFO** para determinar quando usar o TNEF quando você uma mensagem de transporte.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="ca7aa-141">Não suporte TNEF ou não enviar uma mensagem neste formato, quando ele for solicitado pode ser um problema para clientes baseados no formulário ou clientes que requerem propriedades personalizadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="ca7aa-142">Isso ocorre porque o TNEF é geralmente usada para enviar propriedades personalizadas para classes de mensagem personalizada.</span><span class="sxs-lookup"><span data-stu-id="ca7aa-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca7aa-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca7aa-143">See also</span></span>



[<span data-ttu-id="ca7aa-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ca7aa-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ca7aa-145">Propriedade canônico de PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="ca7aa-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="ca7aa-146">Propriedade canônico de PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="ca7aa-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="ca7aa-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca7aa-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

