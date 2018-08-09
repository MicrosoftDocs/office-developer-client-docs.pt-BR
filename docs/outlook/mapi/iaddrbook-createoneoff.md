---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fefd81a7d6cdfda24df93ec928cd3305cb8ef8be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766867"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="d9b0e-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="d9b0e-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="d9b0e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9b0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9b0e-105">Cria um identificador de entrada para um endereço one-off.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d9b0e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9b0e-106">Parameters</span></span>

 <span data-ttu-id="d9b0e-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="d9b0e-107">_lpszName_</span></span>
  
> <span data-ttu-id="d9b0e-108">[in] Um ponteiro para o valor da propriedade de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do destinatário.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="d9b0e-109">O parâmetro _lpszName_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d9b0e-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="d9b0e-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="d9b0e-111">[in] Um ponteiro para o tipo de endereço do destinatário, como FAX ou SMTP.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="d9b0e-112">O parâmetro _lpszAdrType_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="d9b0e-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="d9b0e-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="d9b0e-114">[in] Um ponteiro para o endereço do destinatário.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="d9b0e-115">O parâmetro _lpszAddress_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="d9b0e-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9b0e-116">_ulFlags_</span></span>
  
> <span data-ttu-id="d9b0e-117">[in] Uma bitmask dos sinalizadores que afeta o destinatário único.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="d9b0e-118">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="d9b0e-118">The following flags can be set:</span></span>
    
<span data-ttu-id="d9b0e-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="d9b0e-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="d9b0e-120">O destinatário não pode manipular o conteúdo da mensagem formatada.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="d9b0e-121">Se MAPI_SEND_NO_RICH_INFO for definido, o MAPI define a propriedade de **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como FALSE.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="d9b0e-122">Se MAPI_SEND_NO_RICH_INFO não estiver definida, o MAPI define essa propriedade como TRUE, a menos que o endereço do destinatário mensagens apontado pela _lpszAddress_ é interpretado como um endereço de Internet.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="d9b0e-123">Nesse caso, MAPI define **PR_SEND_RICH_INFO** como FALSE.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="d9b0e-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9b0e-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d9b0e-125">O nome para exibição, tipo de endereço e endereço estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="d9b0e-126">Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d9b0e-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9b0e-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="d9b0e-128">[out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d9b0e-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d9b0e-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9b0e-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="d9b0e-130">[out] Um ponteiro para um ponteiro para o identificador de entrada para o destinatário único.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9b0e-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d9b0e-131">Return value</span></span>

<span data-ttu-id="d9b0e-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9b0e-132">S_OK</span></span> 
  
> <span data-ttu-id="d9b0e-133">O identificador de entrada únicos foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9b0e-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9b0e-134">Remarks</span></span>

<span data-ttu-id="d9b0e-135">Clientes chamar o método **CreateOneOff** para criar um identificador de entrada para um destinatário único — um destinatário que não pertençam a qualquer um dos contêineres de qualquer um dos provedores de catálogo de endereços atualmente carregado.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="d9b0e-136">Destinatários únicos podem ter qualquer tipo de endereço que é suportado por um dos provedores de catálogo de endereços ativo para a sessão.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="d9b0e-137">Destinatários únicos normalmente são criados com um modelo para seus tipos de endereço específica.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="d9b0e-138">O provedor de catálogo de endereços que suporta o tipo de endereço fornece o modelo.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="d9b0e-139">Um usuário de um aplicativo cliente inserir as informações relevantes para o modelo.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="d9b0e-140">MAPI suporta as sequências de caracteres Unicode para o nome para exibição, tipo de endereço e os parâmetros de endereço de **CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="d9b0e-141">O sinalizador MAPI_SEND_NO_RICH_INFO controla se o texto formatado no formato Rich Text (RTF) é enviado junto com cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="d9b0e-142">O TNEF Transport Neutral Encapsulation Format () — é usado para transmitir um formato de texto formatado — é enviada pelo maioria dos provedores de transporte, independentemente de como o destinatário define sua propriedade **PR_SEND_RICH_INFO** .</span><span class="sxs-lookup"><span data-stu-id="d9b0e-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="d9b0e-143">Isso não é um problema para clientes que funcionam com interpessoais emails de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="d9b0e-144">No entanto, porque o TNEF geralmente é utilizado para enviar propriedades personalizadas para classes de mensagem personalizada, não oferece suporte à pode ser um problema para clientes baseados no formulário ou clientes que requerem propriedades personalizadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="d9b0e-145">Para obter mais informações, consulte [Envio de mensagens com TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="d9b0e-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d9b0e-146">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d9b0e-146">MFCMAPI reference</span></span>

<span data-ttu-id="d9b0e-147">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d9b0e-148">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d9b0e-148">**File**</span></span>|<span data-ttu-id="d9b0e-149">**Function**</span><span class="sxs-lookup"><span data-stu-id="d9b0e-149">**Function**</span></span>|<span data-ttu-id="d9b0e-150">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d9b0e-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9b0e-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d9b0e-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="d9b0e-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="d9b0e-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="d9b0e-153">MFCMAPI usa o método **CreateOneOff** para criar uma identificação de entrada para um endereço que não for encontrado em qualquer catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d9b0e-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9b0e-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9b0e-154">See also</span></span>



[<span data-ttu-id="d9b0e-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="d9b0e-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="d9b0e-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d9b0e-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="d9b0e-157">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d9b0e-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

