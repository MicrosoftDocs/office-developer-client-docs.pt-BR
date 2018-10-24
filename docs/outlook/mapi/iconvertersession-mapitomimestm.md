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
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400114"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="3b9c3-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="3b9c3-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="3b9c3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b9c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b9c3-105">Converte uma mensagem MAPI em um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="3b9c3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b9c3-106">Parameters</span></span>

 <span data-ttu-id="3b9c3-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="3b9c3-107">_pmsg_</span></span>
  
> <span data-ttu-id="3b9c3-108">[in] Ponteiro para a mensagem para converter.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="3b9c3-109">Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="3b9c3-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="3b9c3-110">_pstm_</span></span>
  
> <span data-ttu-id="3b9c3-111">[out] Interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para o fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-111">[out] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="3b9c3-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3b9c3-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="3b9c3-113">[in] Sinalizadores que indicam ações específicas para o conversor:</span><span class="sxs-lookup"><span data-stu-id="3b9c3-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="3b9c3-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="3b9c3-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="3b9c3-115">O conversor deve permitir que os cabeçalhos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="3b9c3-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3b9c3-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="3b9c3-117">Informações não enviados/enviadas é persistente no não enviadas X.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="3b9c3-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3b9c3-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="3b9c3-119">O conversor deve criar uma mensagem internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="3b9c3-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="3b9c3-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="3b9c3-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="3b9c3-121">Os destinatários Cco da mensagem MAPI devem ser incluídos no fluxo de MIME.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="3b9c3-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="3b9c3-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="3b9c3-123">Não inclua o campo de Id de mensagem em mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="3b9c3-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="3b9c3-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="3b9c3-125">O conversor deve ignorar os cabeçalhos da mensagem externo.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="3b9c3-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="3b9c3-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="3b9c3-127">O conversor apenas deve enviar texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="3b9c3-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="3b9c3-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="3b9c3-129">O conversor está sendo passado como uma mensagem SMTP.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="3b9c3-130">Esse sinalizador sempre deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-130">This flag must always be set.</span></span>
    
<span data-ttu-id="3b9c3-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="3b9c3-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="3b9c3-132">O conversor deve converter de HTML para o formato RTF na mensagem MIME.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="3b9c3-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="3b9c3-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="3b9c3-134">O conversor deve usar o formato TNEF Transport Neutral Encapsulation Format () na mensagem MIME.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="3b9c3-135">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3b9c3-135">Return values</span></span>

<span data-ttu-id="3b9c3-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3b9c3-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="3b9c3-137">Sinalizadores inválidos foram passados ou *pmsg* ou *pstm* é nulo.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3b9c3-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b9c3-138">Remarks</span></span>

<span data-ttu-id="3b9c3-139">Suporte apenas para os tipos de mensagem padrão do Outlook.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3b9c3-140">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3b9c3-140">MFCMAPI reference</span></span>

<span data-ttu-id="3b9c3-141">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3b9c3-142">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="3b9c3-142">**File**</span></span>|<span data-ttu-id="3b9c3-143">**Função**</span><span class="sxs-lookup"><span data-stu-id="3b9c3-143">**Function**</span></span>|<span data-ttu-id="3b9c3-144">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="3b9c3-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b9c3-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="3b9c3-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3b9c3-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="3b9c3-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="3b9c3-147">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="3b9c3-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="3b9c3-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3b9c3-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="3b9c3-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="3b9c3-150">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="3b9c3-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b9c3-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b9c3-151">See also</span></span>



[<span data-ttu-id="3b9c3-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b9c3-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="3b9c3-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="3b9c3-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="3b9c3-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="3b9c3-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="3b9c3-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="3b9c3-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="3b9c3-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="3b9c3-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="3b9c3-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="3b9c3-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="3b9c3-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="3b9c3-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="3b9c3-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="3b9c3-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="3b9c3-160">Propriedade canônico de PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="3b9c3-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="3b9c3-161">Propriedade canônica PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="3b9c3-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="3b9c3-162">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="3b9c3-162">MAPI Constants</span></span>](mapi-constants.md)

