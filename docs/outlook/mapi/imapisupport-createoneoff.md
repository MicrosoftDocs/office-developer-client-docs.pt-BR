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
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411992"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="a665b-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="a665b-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="a665b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a665b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a665b-105">Cria um identificador de entrada para um endereço one-off.</span><span class="sxs-lookup"><span data-stu-id="a665b-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a665b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a665b-106">Parameters</span></span>

 <span data-ttu-id="a665b-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="a665b-107">_lpszName_</span></span>
  
> <span data-ttu-id="a665b-108">no Um ponteiro para o nome de exibição do destinatário da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a665b-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="a665b-109">O parâmetro _lpszName_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a665b-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a665b-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="a665b-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="a665b-111">no Um ponteiro para o tipo de endereço (como FAX, SMTP ou X500) do destinatário.</span><span class="sxs-lookup"><span data-stu-id="a665b-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="a665b-112">O parâmetro _lpszAdrType_ não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="a665b-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="a665b-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="a665b-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="a665b-114">no Um ponteiro para o endereço de mensagens do destinatário.</span><span class="sxs-lookup"><span data-stu-id="a665b-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="a665b-115">O parâmetro _lpszAddress_ não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="a665b-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="a665b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a665b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="a665b-117">no Uma máscara de bits de sinalizadores que afeta o destinatário one-off.</span><span class="sxs-lookup"><span data-stu-id="a665b-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="a665b-118">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a665b-118">The following flags can be set:</span></span>
    
<span data-ttu-id="a665b-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="a665b-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="a665b-120">O destinatário não pode lidar com o conteúdo de mensagens formatados.</span><span class="sxs-lookup"><span data-stu-id="a665b-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="a665b-121">Se MAPI_SEND_NO_RICH_INFO for definido, MAPI definirá a propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como false.</span><span class="sxs-lookup"><span data-stu-id="a665b-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="a665b-122">Se MAPI_SEND_NO_RICH_INFO não for definido, MAPI definirá essa propriedade como TRUE, a menos que o endereço de email do destinatário apontado por _lpszAddress_ seja interpretado como um endereço de Internet.</span><span class="sxs-lookup"><span data-stu-id="a665b-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="a665b-123">Nesse caso, o MAPI define **PR_SEND_RICH_INFO** como false.</span><span class="sxs-lookup"><span data-stu-id="a665b-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="a665b-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a665b-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a665b-125">O nome de exibição, o tipo de endereço e o endereço estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a665b-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="a665b-126">Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a665b-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a665b-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a665b-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="a665b-128">bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="a665b-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a665b-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="a665b-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="a665b-130">bota Um ponteiro para um ponteiro para o identificador de entrada para o destinatário one-off.</span><span class="sxs-lookup"><span data-stu-id="a665b-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a665b-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a665b-131">Return value</span></span>

<span data-ttu-id="a665b-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="a665b-132">S_OK</span></span> 
  
> <span data-ttu-id="a665b-133">O identificador de entrada one-off foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="a665b-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a665b-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="a665b-134">Remarks</span></span>

<span data-ttu-id="a665b-135">O método **IMAPISupport:: CreateOneOff** é implementado para todos os objetos de suporte do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="a665b-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="a665b-136">Os provedores de serviços chamam o **CreateOneOff** para criar um identificador de entrada para um destinatário individual (um destinatário que não pertence a nenhum contêiner de qualquer um dos provedores de catálogos de endereços carregados no momento).</span><span class="sxs-lookup"><span data-stu-id="a665b-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a665b-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a665b-137">Notes to callers</span></span>

<span data-ttu-id="a665b-138">Quando você terminar de usar o identificador de entrada retornado por **CreateOneOff**, libere a memória alocada para o identificador de entrada usando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a665b-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="a665b-139">Observações para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="a665b-139">Notes to Transport Providers</span></span>

<span data-ttu-id="a665b-140">Dê suporte ao TNEF (Transport neutral Encapsulation Format) e use o valor da propriedade **PR_SEND_RICH_INFO** para determinar se usará TNEF quando você transportar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a665b-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="a665b-141">Não oferecer suporte a TNEF ou não enviar uma mensagem neste formato quando solicitado pode ser um problema para clientes baseados em formulário ou clientes que exigem propriedades MAPI personalizadas.</span><span class="sxs-lookup"><span data-stu-id="a665b-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="a665b-142">Isso ocorre porque o TNEF geralmente é usado para enviar propriedades personalizadas para classes de mensagens personalizadas.</span><span class="sxs-lookup"><span data-stu-id="a665b-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a665b-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="a665b-143">See also</span></span>



[<span data-ttu-id="a665b-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a665b-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a665b-145">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="a665b-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="a665b-146">Propriedade canônica PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="a665b-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="a665b-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a665b-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

