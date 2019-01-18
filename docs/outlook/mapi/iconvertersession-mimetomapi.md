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
ms.openlocfilehash: 356f4470be26ae3803a53af1cec34b3ac6eb0cc9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723030"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="10a04-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="10a04-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="10a04-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10a04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10a04-105">Converte um fluxo MIME em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="10a04-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="10a04-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10a04-106">Parameters</span></span>

 <span data-ttu-id="10a04-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="10a04-107">_pstm_</span></span>
  
> <span data-ttu-id="10a04-108">[in] Interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="10a04-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="10a04-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="10a04-109">_pmsg_</span></span>
  
> <span data-ttu-id="10a04-110">[out] Ponteiro para a mensagem para carregar.</span><span class="sxs-lookup"><span data-stu-id="10a04-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="10a04-111">Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="10a04-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="10a04-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="10a04-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="10a04-113">[in] Este valor deve ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="10a04-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="10a04-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="10a04-114">_ulFlags_</span></span>
  
> <span data-ttu-id="10a04-115">[in] Este parâmetro identificará nenhuma ação especial a ser executada durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="10a04-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="10a04-116">Ele deve ser zero (0) se nenhuma ação específica deve ser tomada, ou uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="10a04-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="10a04-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="10a04-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="10a04-118">Informações não enviados/enviadas é persistente no não enviadas X.</span><span class="sxs-lookup"><span data-stu-id="10a04-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="10a04-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="10a04-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="10a04-120">O fluxo MIME é uma mensagem do Simple MAPI Transfer Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="10a04-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="10a04-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="10a04-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="10a04-122">Os destinatários Cco do fluxo de MIME devem ser incluídos na mensagem de MAPI.</span><span class="sxs-lookup"><span data-stu-id="10a04-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="10a04-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="10a04-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="10a04-124">O corpo de HTML do fluxo de MIME deve ser convertido para formato Rich Text (RTF) na mensagem de MAPI.</span><span class="sxs-lookup"><span data-stu-id="10a04-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="10a04-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="10a04-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="10a04-126">O conversor deve manipular o fluxo MIME como uma mensagem internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="10a04-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="10a04-127">Não suportado no Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="10a04-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10a04-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="10a04-128">Return value</span></span>

<span data-ttu-id="10a04-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="10a04-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="10a04-130">Indica que _pstm_ for **nula**, _pmsg_ é **Nulo**ou _ulFlags_ é inválido.</span><span class="sxs-lookup"><span data-stu-id="10a04-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="10a04-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="10a04-131">Remarks</span></span>

<span data-ttu-id="10a04-132">Se você especificou **CCSF_USE_RTF** como parte do _ulFlags_ e o armazenamento de mensagens de destino oferece suporte a HTML e RTF, a mensagem MAPI será convertida em HTML ou RTF.</span><span class="sxs-lookup"><span data-stu-id="10a04-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="10a04-133">Se a mensagem é convertida em RTF, será compactado convertido no novo formato RTF, qualquer HTML será incorporada na sequência de RTF compactada e a cadeia de caracteres será contida a [Propriedade canônico de PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="10a04-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="10a04-134">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="10a04-134">MFCMAPI reference</span></span>

<span data-ttu-id="10a04-135">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="10a04-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="10a04-136">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="10a04-136">**File**</span></span>|<span data-ttu-id="10a04-137">**Função**</span><span class="sxs-lookup"><span data-stu-id="10a04-137">**Function**</span></span>|<span data-ttu-id="10a04-138">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="10a04-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="10a04-139">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="10a04-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="10a04-140">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="10a04-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="10a04-141">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="10a04-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="10a04-142">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="10a04-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="10a04-143">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="10a04-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="10a04-144">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="10a04-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10a04-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="10a04-145">See also</span></span>



[<span data-ttu-id="10a04-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10a04-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="10a04-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="10a04-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="10a04-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="10a04-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="10a04-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="10a04-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="10a04-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="10a04-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="10a04-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="10a04-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="10a04-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="10a04-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="10a04-153">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="10a04-153">MAPI Constants</span></span>](mapi-constants.md)

