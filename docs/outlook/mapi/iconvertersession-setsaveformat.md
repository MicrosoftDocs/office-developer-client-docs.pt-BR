---
title: IConverterSessionSetSaveFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f24ad938fdb8c3ac234e1d78f2668139840c8b8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568214"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="cdf6d-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="cdf6d-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="cdf6d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdf6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdf6d-105">Define o formato no qual o conversor retornará um fluxo MIME em [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="cdf6d-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="cdf6d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdf6d-106">Parameters</span></span>

<span data-ttu-id="cdf6d-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="cdf6d-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="cdf6d-108">[in] Salvar formato a ser usado para um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="cdf6d-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="cdf6d-109">Para obter mais informações, consulte o tipo de enum [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cdf6d-109">For more information, see the enum type [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="cdf6d-110">**SAVE_RFC1521**: uso MIME, que é o padrão.</span><span class="sxs-lookup"><span data-stu-id="cdf6d-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="cdf6d-111">**SAVE_RFC822**: Use uuencode.</span><span class="sxs-lookup"><span data-stu-id="cdf6d-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="cdf6d-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="cdf6d-112">Return values</span></span>

<span data-ttu-id="cdf6d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="cdf6d-113">S_OK</span></span>
  
> <span data-ttu-id="cdf6d-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cdf6d-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="cdf6d-115">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cdf6d-115">MFCMAPI reference</span></span>

<span data-ttu-id="cdf6d-116">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cdf6d-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cdf6d-117">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="cdf6d-117">**File**</span></span>|<span data-ttu-id="cdf6d-118">**Function**</span><span class="sxs-lookup"><span data-stu-id="cdf6d-118">**Function**</span></span>|<span data-ttu-id="cdf6d-119">**Comment**</span><span class="sxs-lookup"><span data-stu-id="cdf6d-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cdf6d-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="cdf6d-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="cdf6d-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="cdf6d-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="cdf6d-122">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="cdf6d-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="cdf6d-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="cdf6d-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="cdf6d-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="cdf6d-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="cdf6d-125">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="cdf6d-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdf6d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdf6d-126">See also</span></span>

- [<span data-ttu-id="cdf6d-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cdf6d-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="cdf6d-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="cdf6d-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="cdf6d-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="cdf6d-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="cdf6d-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="cdf6d-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="cdf6d-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="cdf6d-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="cdf6d-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="cdf6d-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="cdf6d-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="cdf6d-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="cdf6d-134">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="cdf6d-134">MAPI Constants</span></span>](mapi-constants.md)

