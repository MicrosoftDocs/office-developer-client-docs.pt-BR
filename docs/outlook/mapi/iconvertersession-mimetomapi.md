---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 03a67371c67d5f0ac346470ec7ab38bb67d5ce2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766900"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="489c8-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="489c8-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="489c8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="489c8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="489c8-105">Converte um fluxo MIME em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="489c8-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="489c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="489c8-106">Parameters</span></span>

 <span data-ttu-id="489c8-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="489c8-107">_pstm_</span></span>
  
> <span data-ttu-id="489c8-108">[in] Interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) a um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="489c8-108">[in] [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="489c8-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="489c8-109">_pmsg_</span></span>
  
> <span data-ttu-id="489c8-110">[out] Ponteiro para a mensagem para carregar.</span><span class="sxs-lookup"><span data-stu-id="489c8-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="489c8-111">Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="489c8-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="489c8-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="489c8-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="489c8-113">[in] Este valor deve ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="489c8-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="489c8-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="489c8-114">_ulFlags_</span></span>
  
> <span data-ttu-id="489c8-115">[in] Este parâmetro identificará nenhuma ação especial a ser executada durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="489c8-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="489c8-116">Ele deve ser zero (0) se nenhuma ação específica deve ser tomada, ou uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="489c8-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="489c8-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="489c8-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="489c8-118">Informações não enviados/enviadas é persistente no não enviadas X.</span><span class="sxs-lookup"><span data-stu-id="489c8-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="489c8-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="489c8-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="489c8-120">O fluxo MIME é uma mensagem do Simple MAPI Transfer Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="489c8-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="489c8-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="489c8-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="489c8-122">Os destinatários Cco do fluxo de MIME devem ser incluídos na mensagem de MAPI.</span><span class="sxs-lookup"><span data-stu-id="489c8-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="489c8-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="489c8-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="489c8-124">O corpo de HTML do fluxo de MIME deve ser convertido para formato Rich Text (RTF) na mensagem de MAPI.</span><span class="sxs-lookup"><span data-stu-id="489c8-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="489c8-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="489c8-125">Return value</span></span>

<span data-ttu-id="489c8-126">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="489c8-126">E_INVALIDARG</span></span>
  
> <span data-ttu-id="489c8-127">Indica que _pstm_ for **nula**, _pmsg_ é **Nulo**ou _ulFlags_ é inválido.</span><span class="sxs-lookup"><span data-stu-id="489c8-127">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="489c8-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="489c8-128">Remarks</span></span>

<span data-ttu-id="489c8-129">Se você especificou **CCSF_USE_RTF** como parte do _ulFlags_ e o armazenamento de mensagens de destino oferece suporte a HTML e RTF, a mensagem MAPI será convertida em HTML ou RTF.</span><span class="sxs-lookup"><span data-stu-id="489c8-129">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="489c8-130">Se a mensagem é convertida em RTF, será compactado convertido no novo formato RTF, qualquer HTML será incorporada na sequência de RTF compactada e a cadeia de caracteres será contida a [Propriedade canônico de PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="489c8-130">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="489c8-131">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="489c8-131">MFCMAPI reference</span></span>

<span data-ttu-id="489c8-132">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="489c8-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="489c8-133">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="489c8-133">**File**</span></span>|<span data-ttu-id="489c8-134">**Function**</span><span class="sxs-lookup"><span data-stu-id="489c8-134">**Function**</span></span>|<span data-ttu-id="489c8-135">**Comment**</span><span class="sxs-lookup"><span data-stu-id="489c8-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="489c8-136">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="489c8-136">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="489c8-137">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="489c8-137">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="489c8-138">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="489c8-138">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="489c8-139">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="489c8-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="489c8-140">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="489c8-140">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="489c8-141">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="489c8-141">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="489c8-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="489c8-142">See also</span></span>



[<span data-ttu-id="489c8-143">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="489c8-143">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="489c8-144">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="489c8-144">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="489c8-145">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="489c8-145">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="489c8-146">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="489c8-146">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="489c8-147">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="489c8-147">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="489c8-148">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="489c8-148">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="489c8-149">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="489c8-149">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="489c8-150">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="489c8-150">MAPI Constants</span></span>](mapi-constants.md)

