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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 81771a263a7496042d4950b465c0d5b03290399b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766910"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="b83f1-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="b83f1-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="b83f1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b83f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b83f1-105">Define o largura de um fluxo MIME que o conversor vai retornar em [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)de quebra de texto.</span><span class="sxs-lookup"><span data-stu-id="b83f1-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="b83f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b83f1-106">Parameters</span></span>

 <span data-ttu-id="b83f1-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="b83f1-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="b83f1-108">[in] Se deseja quebrar texto automaticamente ou não.</span><span class="sxs-lookup"><span data-stu-id="b83f1-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="b83f1-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="b83f1-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="b83f1-110">[in] O texto quebra largura usar.</span><span class="sxs-lookup"><span data-stu-id="b83f1-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b83f1-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b83f1-111">Return value</span></span>

<span data-ttu-id="b83f1-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b83f1-112">S_OK</span></span>
  
> <span data-ttu-id="b83f1-113">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b83f1-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="b83f1-114">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b83f1-114">MFCMAPI reference</span></span>

<span data-ttu-id="b83f1-115">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b83f1-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b83f1-116">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b83f1-116">**File**</span></span>|<span data-ttu-id="b83f1-117">**Function**</span><span class="sxs-lookup"><span data-stu-id="b83f1-117">**Function**</span></span>|<span data-ttu-id="b83f1-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b83f1-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b83f1-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="b83f1-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="b83f1-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="b83f1-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="b83f1-121">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="b83f1-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="b83f1-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="b83f1-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="b83f1-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="b83f1-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="b83f1-124">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="b83f1-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b83f1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b83f1-125">See also</span></span>



[<span data-ttu-id="b83f1-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b83f1-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="b83f1-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="b83f1-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="b83f1-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="b83f1-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="b83f1-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="b83f1-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="b83f1-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="b83f1-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="b83f1-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="b83f1-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="b83f1-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="b83f1-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="b83f1-133">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b83f1-133">MAPI Constants</span></span>](mapi-constants.md)

