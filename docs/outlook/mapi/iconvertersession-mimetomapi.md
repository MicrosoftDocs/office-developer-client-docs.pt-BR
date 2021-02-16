---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Última modificação: 06 de setembro de 2019'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160283"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="0cf75-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="0cf75-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="0cf75-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cf75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cf75-105">Converte um fluxo MIME em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="0cf75-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="0cf75-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cf75-106">Parameters</span></span>

 <span data-ttu-id="0cf75-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="0cf75-107">_pstm_</span></span>
  
> <span data-ttu-id="0cf75-108">[in] [Interface IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="0cf75-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="0cf75-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="0cf75-109">_pmsg_</span></span>
  
> <span data-ttu-id="0cf75-110">[in] Ponteiro para a mensagem a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="0cf75-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="0cf75-111">O chamador deve fornecer uma mensagem para que a API seja preenchida, portanto, o objeto deve ser usado [in].</span><span class="sxs-lookup"><span data-stu-id="0cf75-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="0cf75-112">Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="0cf75-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="0cf75-113">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="0cf75-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="0cf75-114">[in] Esse valor deve ser **nulo.**</span><span class="sxs-lookup"><span data-stu-id="0cf75-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="0cf75-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0cf75-115">_ulFlags_</span></span>
  
> <span data-ttu-id="0cf75-116">[in] Esse parâmetro identifica qualquer ação especial a ser tomada durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="0cf75-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="0cf75-117">Ele deve ser zero (0) se nenhuma ação específica for tomada ou uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="0cf75-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="0cf75-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="0cf75-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="0cf75-119">As informações enviadas/não enviadas são persistentes em X-Unsent.</span><span class="sxs-lookup"><span data-stu-id="0cf75-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="0cf75-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="0cf75-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="0cf75-121">O fluxo MIME é para uma mensagem SMTP.</span><span class="sxs-lookup"><span data-stu-id="0cf75-121">The MIME stream is for a Simple Mail Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="0cf75-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="0cf75-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="0cf75-123">Os destinatários Cc do fluxo MIME devem ser incluídos na mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="0cf75-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="0cf75-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="0cf75-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="0cf75-125">O corpo HTML do fluxo MIME deve ser convertido em RTF (Rich Text Format) na mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="0cf75-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="0cf75-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="0cf75-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="0cf75-127">O conversor deve manipular o fluxo MIME como uma mensagem internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="0cf75-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="0cf75-128">Sem suporte no Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="0cf75-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0cf75-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0cf75-129">Return value</span></span>

<span data-ttu-id="0cf75-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0cf75-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="0cf75-131">Indica que  _pstm_ é **nulo,**  _pmsg_ é **nulo** ou  _ulFlags_ é inválido.</span><span class="sxs-lookup"><span data-stu-id="0cf75-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0cf75-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cf75-132">Remarks</span></span>

<span data-ttu-id="0cf75-133">Se você especificou CCSF_USE_RTF como parte do _ulFlags_ e o armazenamento de mensagens de destino dá suporte a HTML e RTF, a mensagem MAPI será convertida em HTML ou RTF. </span><span class="sxs-lookup"><span data-stu-id="0cf75-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="0cf75-134">Se a mensagem for convertida em RTF, o formato convertido será compactado RTF, qualquer HTML será inserido na cadeia de caracteres RTF compactada e a cadeia de caracteres estará contida na propriedade canônica [PidTagRtfCompressed.](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0cf75-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0cf75-135">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0cf75-135">MFCMAPI reference</span></span>

<span data-ttu-id="0cf75-136">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0cf75-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0cf75-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0cf75-137">**File**</span></span>|<span data-ttu-id="0cf75-138">**Função**</span><span class="sxs-lookup"><span data-stu-id="0cf75-138">**Function**</span></span>|<span data-ttu-id="0cf75-139">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="0cf75-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0cf75-140">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="0cf75-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="0cf75-141">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="0cf75-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="0cf75-142">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="0cf75-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="0cf75-143">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="0cf75-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="0cf75-144">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="0cf75-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="0cf75-145">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="0cf75-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0cf75-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cf75-146">See also</span></span>



[<span data-ttu-id="0cf75-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0cf75-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="0cf75-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="0cf75-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="0cf75-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="0cf75-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="0cf75-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="0cf75-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="0cf75-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="0cf75-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="0cf75-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="0cf75-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="0cf75-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="0cf75-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="0cf75-154">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="0cf75-154">MAPI Constants</span></span>](mapi-constants.md)

