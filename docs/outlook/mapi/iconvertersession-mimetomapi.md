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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326926"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="fdc9b-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="fdc9b-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="fdc9b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdc9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdc9b-105">Converte um fluxo MIME em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="fdc9b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdc9b-106">Parameters</span></span>

 <span data-ttu-id="fdc9b-107">_pStm_</span><span class="sxs-lookup"><span data-stu-id="fdc9b-107">_pstm_</span></span>
  
> <span data-ttu-id="fdc9b-108">no Interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="fdc9b-109">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="fdc9b-109">_pmsg_</span></span>
  
> <span data-ttu-id="fdc9b-110">bota Ponteiro para a mensagem a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="fdc9b-111">Consulte mapidefs. h para a definição de tipo de **lpMessage**.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="fdc9b-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="fdc9b-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="fdc9b-113">no Este valor deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="fdc9b-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fdc9b-114">_ulFlags_</span></span>
  
> <span data-ttu-id="fdc9b-115">no Esse parâmetro identifica qualquer ação especial a ser tomada durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="fdc9b-116">Ele deve ser zero (0) se nenhuma ação específica for executada ou uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fdc9b-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="fdc9b-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="fdc9b-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="fdc9b-118">As informações enviadas/não enviadas são mantidas em X-não enviadas.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="fdc9b-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="fdc9b-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="fdc9b-120">O fluxo MIME é para uma mensagem Simple MAPI Transfer Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="fdc9b-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="fdc9b-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="fdc9b-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="fdc9b-122">Os destinatários Cco do fluxo MIME devem ser incluídos na mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="fdc9b-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="fdc9b-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="fdc9b-124">O corpo HTML do fluxo MIME deve ser convertido em Rich Text Format (RTF) na mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="fdc9b-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="fdc9b-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="fdc9b-126">O conversor deve lidar com o fluxo MIME como uma mensagem internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="fdc9b-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="fdc9b-127">Sem suporte no Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fdc9b-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fdc9b-128">Return value</span></span>

<span data-ttu-id="fdc9b-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fdc9b-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="fdc9b-130">Indica que _pStm_ é **nulo**, _pMsg_ é **nulo**ou _parâmetroulflags_ é inválido.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fdc9b-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdc9b-131">Remarks</span></span>

<span data-ttu-id="fdc9b-132">Se você tiver especificado o **CCSF_USE_RTF** como parte do _parâmetroulflags_ e o repositório de mensagens de destino oferecer suporte a HTML e RTF, a mensagem MAPI será convertida em HTML ou RTF.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="fdc9b-133">Se a mensagem for convertida para RTF, o formato convertido será compactado RTF, qualquer HTML será incorporado na cadeia de caracteres RTF compactada, e a cadeia de caracteres será contida na [Propriedade canônica PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="fdc9b-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fdc9b-134">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fdc9b-134">MFCMAPI reference</span></span>

<span data-ttu-id="fdc9b-135">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fdc9b-136">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fdc9b-136">**File**</span></span>|<span data-ttu-id="fdc9b-137">**Função**</span><span class="sxs-lookup"><span data-stu-id="fdc9b-137">**Function**</span></span>|<span data-ttu-id="fdc9b-138">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="fdc9b-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fdc9b-139">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="fdc9b-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="fdc9b-140">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="fdc9b-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="fdc9b-141">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="fdc9b-142">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="fdc9b-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="fdc9b-143">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="fdc9b-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="fdc9b-144">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="fdc9b-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fdc9b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdc9b-145">See also</span></span>



[<span data-ttu-id="fdc9b-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fdc9b-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="fdc9b-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="fdc9b-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="fdc9b-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="fdc9b-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="fdc9b-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="fdc9b-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="fdc9b-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="fdc9b-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="fdc9b-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="fdc9b-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="fdc9b-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="fdc9b-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="fdc9b-153">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="fdc9b-153">MAPI Constants</span></span>](mapi-constants.md)

