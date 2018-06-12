---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 81771a263a7496042d4950b465c0d5b03290399b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766910"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="13b9f-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="13b9f-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="13b9f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13b9f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13b9f-105">Define o largura de um fluxo MIME que o conversor vai retornar em [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)de quebra de texto.</span><span class="sxs-lookup"><span data-stu-id="13b9f-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="13b9f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="13b9f-106">Parameters</span></span>

 <span data-ttu-id="13b9f-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="13b9f-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="13b9f-108">[in] Se deseja quebrar texto automaticamente ou não.</span><span class="sxs-lookup"><span data-stu-id="13b9f-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="13b9f-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="13b9f-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="13b9f-110">[in] O texto quebra largura usar.</span><span class="sxs-lookup"><span data-stu-id="13b9f-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13b9f-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="13b9f-111">Return value</span></span>

<span data-ttu-id="13b9f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="13b9f-112">S_OK</span></span>
  
> <span data-ttu-id="13b9f-113">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13b9f-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="13b9f-114">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="13b9f-114">MFCMAPI reference</span></span>

<span data-ttu-id="13b9f-115">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="13b9f-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="13b9f-116">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="13b9f-116">**File**</span></span>|<span data-ttu-id="13b9f-117">**Function**</span><span class="sxs-lookup"><span data-stu-id="13b9f-117">**Function**</span></span>|<span data-ttu-id="13b9f-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="13b9f-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13b9f-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="13b9f-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="13b9f-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="13b9f-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="13b9f-121">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="13b9f-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="13b9f-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="13b9f-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="13b9f-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="13b9f-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="13b9f-124">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="13b9f-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13b9f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="13b9f-125">See also</span></span>



[<span data-ttu-id="13b9f-126">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="13b9f-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="13b9f-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="13b9f-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="13b9f-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="13b9f-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="13b9f-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="13b9f-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="13b9f-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="13b9f-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="13b9f-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="13b9f-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="13b9f-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="13b9f-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="13b9f-133">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="13b9f-133">MAPI Constants</span></span>](mapi-constants.md)

