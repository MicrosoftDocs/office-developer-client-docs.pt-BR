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
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427378"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="f6e2a-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="f6e2a-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="f6e2a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6e2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6e2a-105">Cria um identificador de entrada para um endereço one-off.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f6e2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6e2a-106">Parameters</span></span>

 <span data-ttu-id="f6e2a-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="f6e2a-107">_lpszName_</span></span>
  
> <span data-ttu-id="f6e2a-108">no Um ponteiro para o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do destinatário.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="f6e2a-109">O parâmetro _lpszName_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f6e2a-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="f6e2a-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="f6e2a-111">no Um ponteiro para o tipo de endereço do destinatário, como FAX ou SMTP.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="f6e2a-112">O parâmetro _lpszAdrType_ não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="f6e2a-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="f6e2a-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="f6e2a-114">no Um ponteiro para o endereço do destinatário.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="f6e2a-115">O parâmetro _lpszAddress_ não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="f6e2a-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f6e2a-116">_ulFlags_</span></span>
  
> <span data-ttu-id="f6e2a-117">no Uma máscara de bits de sinalizadores que afeta o destinatário one-off.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="f6e2a-118">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f6e2a-118">The following flags can be set:</span></span>
    
<span data-ttu-id="f6e2a-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="f6e2a-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="f6e2a-120">O destinatário não pode lidar com o conteúdo de mensagens formatados.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="f6e2a-121">Se MAPI_SEND_NO_RICH_INFO for definido, MAPI definirá a propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como false.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="f6e2a-122">Se MAPI_SEND_NO_RICH_INFO não for definido, MAPI definirá essa propriedade como TRUE, a menos que o endereço de email do destinatário apontado por _lpszAddress_ seja interpretado como um endereço de Internet.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="f6e2a-123">Nesse caso, o MAPI define **PR_SEND_RICH_INFO** como false.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="f6e2a-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f6e2a-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f6e2a-125">O nome de exibição, o tipo de endereço e o endereço estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="f6e2a-126">Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f6e2a-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f6e2a-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="f6e2a-128">bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f6e2a-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f6e2a-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="f6e2a-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="f6e2a-130">bota Um ponteiro para um ponteiro para o identificador de entrada para o destinatário one-off.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f6e2a-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f6e2a-131">Return value</span></span>

<span data-ttu-id="f6e2a-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6e2a-132">S_OK</span></span> 
  
> <span data-ttu-id="f6e2a-133">O identificador de entrada one-off foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6e2a-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6e2a-134">Remarks</span></span>

<span data-ttu-id="f6e2a-135">Os clientes chamam o método **CreateOneOff** para criar um identificador de entrada para um destinatário one-off, que não pertence a nenhum contêiner de qualquer um dos provedores de catálogo de endereços carregados no momento.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="f6e2a-136">Os destinatários únicos podem ter qualquer tipo de endereço que seja suportado por um dos provedores de catálogos de endereços ativos da sessão.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="f6e2a-137">Os destinatários únicos são normalmente criados com um modelo para o seu tipo de endereço específico.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="f6e2a-138">O provedor de catálogo de endereços que oferece suporte ao tipo de endereço fornece o modelo.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="f6e2a-139">Um usuário de um aplicativo cliente insere as informações relevantes no modelo.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="f6e2a-140">O MAPI oferece suporte a cadeias de caracteres Unicode para o nome de exibição, tipo de endereço e parâmetros de endereço de **CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="f6e2a-141">O sinalizador MAPI_SEND_NO_RICH_INFO controla se o texto formatado no formato Rich Text (RTF) é enviado junto com cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="f6e2a-142">O formato de encapsulamento neutro de transporte (TNEF) — um formato que é usado para transmitir texto formatado — é enviado pela maioria dos provedores de transporte, independentemente de como o destinatário define sua propriedade **PR_SEND_RICH_INFO** .</span><span class="sxs-lookup"><span data-stu-id="f6e2a-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="f6e2a-143">Isso não é um problema para clientes de mensagens que trabalham com mensagens interpessoais.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="f6e2a-144">No enTanto, como o TNEF geralmente é usado para enviar propriedades personalizadas para classes de mensagens personalizadas, não o suporte para ela pode ser um problema para clientes baseados em formulário ou clientes que exigem propriedades MAPI personalizadas.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="f6e2a-145">Para obter mais informações, consulte [enviando mensagens com TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="f6e2a-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f6e2a-146">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f6e2a-146">MFCMAPI reference</span></span>

<span data-ttu-id="f6e2a-147">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f6e2a-148">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f6e2a-148">**File**</span></span>|<span data-ttu-id="f6e2a-149">**Função**</span><span class="sxs-lookup"><span data-stu-id="f6e2a-149">**Function**</span></span>|<span data-ttu-id="f6e2a-150">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f6e2a-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6e2a-151">Mapiabfunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="f6e2a-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="f6e2a-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="f6e2a-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="f6e2a-153">MFCMAPI usa o método **CreateOneOff** para criar uma ID de entrada para um endereço que não é encontrado em nenhum catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="f6e2a-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6e2a-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6e2a-154">See also</span></span>



[<span data-ttu-id="f6e2a-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="f6e2a-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="f6e2a-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f6e2a-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="f6e2a-157">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f6e2a-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

