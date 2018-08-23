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
ms.openlocfilehash: a89f6dd14e8bbea9d0d4145dc05bf332af95234a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573626"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="dea08-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="dea08-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="dea08-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dea08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dea08-105">Define o largura de um fluxo MIME que o conversor vai retornar em [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)de quebra de texto.</span><span class="sxs-lookup"><span data-stu-id="dea08-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="dea08-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dea08-106">Parameters</span></span>

 <span data-ttu-id="dea08-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="dea08-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="dea08-108">[in] Se deseja quebrar texto automaticamente ou não.</span><span class="sxs-lookup"><span data-stu-id="dea08-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="dea08-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="dea08-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="dea08-110">[in] O texto quebra largura usar.</span><span class="sxs-lookup"><span data-stu-id="dea08-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dea08-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dea08-111">Return value</span></span>

<span data-ttu-id="dea08-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="dea08-112">S_OK</span></span>
  
> <span data-ttu-id="dea08-113">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dea08-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="dea08-114">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dea08-114">MFCMAPI reference</span></span>

<span data-ttu-id="dea08-115">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dea08-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dea08-116">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="dea08-116">**File**</span></span>|<span data-ttu-id="dea08-117">**Function**</span><span class="sxs-lookup"><span data-stu-id="dea08-117">**Function**</span></span>|<span data-ttu-id="dea08-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="dea08-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dea08-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="dea08-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="dea08-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="dea08-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="dea08-121">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="dea08-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="dea08-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="dea08-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="dea08-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="dea08-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="dea08-124">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="dea08-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dea08-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dea08-125">See also</span></span>



[<span data-ttu-id="dea08-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dea08-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="dea08-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="dea08-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="dea08-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="dea08-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="dea08-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="dea08-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="dea08-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="dea08-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="dea08-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="dea08-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="dea08-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="dea08-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="dea08-133">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="dea08-133">MAPI Constants</span></span>](mapi-constants.md)

