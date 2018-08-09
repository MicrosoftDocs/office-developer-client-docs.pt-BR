---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Modificado pela última vez: 20 de setembro de 2017'
ms.openlocfilehash: b59114926d44ba613efbbde1c8dd5d17c26756c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766899"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="45cec-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="45cec-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="45cec-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45cec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45cec-105">Converte uma mensagem MAPI em um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="45cec-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="45cec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45cec-106">Parameters</span></span>

 <span data-ttu-id="45cec-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="45cec-107">_pmsg_</span></span>
  
> <span data-ttu-id="45cec-108">[in] Ponteiro para a mensagem para converter.</span><span class="sxs-lookup"><span data-stu-id="45cec-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="45cec-109">Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="45cec-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="45cec-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="45cec-110">_pstm_</span></span>
  
> <span data-ttu-id="45cec-111">[out] Interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) para o fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="45cec-111">[out] [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="45cec-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45cec-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="45cec-113">[in] Sinalizadores que indicam ações específicas para o conversor:</span><span class="sxs-lookup"><span data-stu-id="45cec-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="45cec-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="45cec-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="45cec-115">O conversor deve permitir que os cabeçalhos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="45cec-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="45cec-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="45cec-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="45cec-117">Informações não enviados/enviadas é persistente no não enviadas X.</span><span class="sxs-lookup"><span data-stu-id="45cec-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="45cec-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="45cec-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="45cec-119">O conversor deve criar uma mensagem internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="45cec-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="45cec-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="45cec-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="45cec-121">Os destinatários Cco da mensagem MAPI devem ser incluídos no fluxo de MIME.</span><span class="sxs-lookup"><span data-stu-id="45cec-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="45cec-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="45cec-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="45cec-123">Não inclua o campo de Id de mensagem em mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="45cec-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="45cec-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="45cec-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="45cec-125">O conversor deve ignorar os cabeçalhos da mensagem externo.</span><span class="sxs-lookup"><span data-stu-id="45cec-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="45cec-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="45cec-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="45cec-127">O conversor apenas deve enviar texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="45cec-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="45cec-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="45cec-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="45cec-129">O conversor está sendo passado como uma mensagem SMTP.</span><span class="sxs-lookup"><span data-stu-id="45cec-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="45cec-130">Esse sinalizador sempre deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="45cec-130">This flag must always be set.</span></span>
    
<span data-ttu-id="45cec-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="45cec-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="45cec-132">O conversor deve converter de HTML para o formato RTF na mensagem MIME.</span><span class="sxs-lookup"><span data-stu-id="45cec-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="45cec-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="45cec-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="45cec-134">O conversor deve usar o formato TNEF Transport Neutral Encapsulation Format () na mensagem MIME.</span><span class="sxs-lookup"><span data-stu-id="45cec-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="45cec-135">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="45cec-135">Return values</span></span>

<span data-ttu-id="45cec-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="45cec-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="45cec-137">Sinalizadores inválidos foram passados ou *pmsg* ou *pstm* é nulo.</span><span class="sxs-lookup"><span data-stu-id="45cec-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="45cec-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="45cec-138">Remarks</span></span>

<span data-ttu-id="45cec-139">Suporte apenas para os tipos de mensagem padrão do Outlook.</span><span class="sxs-lookup"><span data-stu-id="45cec-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="45cec-140">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="45cec-140">MFCMAPI reference</span></span>

<span data-ttu-id="45cec-141">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="45cec-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="45cec-142">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="45cec-142">**File**</span></span>|<span data-ttu-id="45cec-143">**Function**</span><span class="sxs-lookup"><span data-stu-id="45cec-143">**Function**</span></span>|<span data-ttu-id="45cec-144">**Comment**</span><span class="sxs-lookup"><span data-stu-id="45cec-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45cec-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="45cec-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="45cec-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="45cec-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="45cec-147">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="45cec-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="45cec-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="45cec-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="45cec-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="45cec-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="45cec-150">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="45cec-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45cec-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="45cec-151">See also</span></span>



[<span data-ttu-id="45cec-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45cec-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="45cec-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="45cec-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="45cec-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="45cec-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="45cec-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="45cec-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="45cec-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="45cec-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="45cec-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="45cec-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="45cec-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="45cec-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="45cec-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="45cec-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="45cec-160">Propriedade canônica PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="45cec-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="45cec-161">Propriedade can�nico de PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="45cec-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="45cec-162">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="45cec-162">MAPI Constants</span></span>](mapi-constants.md)

