---
title: IConverterSessionSetEncoding
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
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a13d4e54900989c692add85add6853a1b511f448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766912"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="9eb85-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="9eb85-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="9eb85-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9eb85-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9eb85-105">Inicializa a codificação a ser usada durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="9eb85-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="9eb85-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eb85-106">Parameters</span></span>

<span data-ttu-id="9eb85-107">_et_</span><span class="sxs-lookup"><span data-stu-id="9eb85-107">_et_</span></span>
  
> <span data-ttu-id="9eb85-108">Um valor [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9eb85-108">An [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="9eb85-109">Apenas os valores a seguir são suportados:</span><span class="sxs-lookup"><span data-stu-id="9eb85-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="9eb85-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="9eb85-110">IET_BASE64</span></span>
   - <span data-ttu-id="9eb85-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="9eb85-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="9eb85-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="9eb85-112">IET_QP</span></span>
   - <span data-ttu-id="9eb85-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="9eb85-113">IET_7BIT</span></span>
   - <span data-ttu-id="9eb85-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="9eb85-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9eb85-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9eb85-115">Return value</span></span>

<span data-ttu-id="9eb85-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9eb85-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="9eb85-117">O tipo de codificação passado era inválido.</span><span class="sxs-lookup"><span data-stu-id="9eb85-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9eb85-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9eb85-118">Remarks</span></span>

<span data-ttu-id="9eb85-119">Chame **SetEncoding** antes de usar [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="9eb85-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="9eb85-120">Use **SetEncoding** para definir a codificação para apenas o corpo da mensagem mais externo de um item de email.</span><span class="sxs-lookup"><span data-stu-id="9eb85-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="9eb85-121">Microsoft Outlook 2010 e o Microsoft Outlook 2013 escolha a codificação para todos os anexos individuais.</span><span class="sxs-lookup"><span data-stu-id="9eb85-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9eb85-122">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9eb85-122">MFCMAPI reference</span></span>

<span data-ttu-id="9eb85-123">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9eb85-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9eb85-124">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9eb85-124">**File**</span></span>|<span data-ttu-id="9eb85-125">**Function**</span><span class="sxs-lookup"><span data-stu-id="9eb85-125">**Function**</span></span>|<span data-ttu-id="9eb85-126">**Comment**</span><span class="sxs-lookup"><span data-stu-id="9eb85-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9eb85-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="9eb85-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="9eb85-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="9eb85-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="9eb85-129">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="9eb85-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="9eb85-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="9eb85-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="9eb85-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="9eb85-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="9eb85-132">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="9eb85-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9eb85-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9eb85-133">See also</span></span>

- [<span data-ttu-id="9eb85-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9eb85-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="9eb85-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="9eb85-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="9eb85-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="9eb85-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="9eb85-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="9eb85-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="9eb85-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="9eb85-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="9eb85-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="9eb85-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="9eb85-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="9eb85-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="9eb85-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9eb85-141">MAPI Constants</span></span>](mapi-constants.md)

