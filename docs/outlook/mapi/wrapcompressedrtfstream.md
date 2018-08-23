---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a7095907a1fb437e225922d0bef08b4ad79a4b6f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594590"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="af994-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="af994-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="af994-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af994-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af994-105">Cria um fluxo de texto em descompactado Rich Text Format (RTF) do formato compactado usado na propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="af994-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af994-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="af994-106">Header file:</span></span>  <br/> |<span data-ttu-id="af994-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af994-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="af994-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="af994-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="af994-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="af994-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="af994-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="af994-110">Called by:</span></span>  <br/> |<span data-ttu-id="af994-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="af994-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="af994-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af994-112">Parameters</span></span>

 <span data-ttu-id="af994-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="af994-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="af994-114">[in] Ponteiro para um fluxo aberto na propriedade PR_RTF_COMPRESSED de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="af994-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="af994-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af994-115">_ulFlags_</span></span>
  
> <span data-ttu-id="af994-116">[in] Bitmask dos sinalizadores de opção para a função.</span><span class="sxs-lookup"><span data-stu-id="af994-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="af994-117">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="af994-117">The following flags can be set:</span></span>
    
<span data-ttu-id="af994-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="af994-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="af994-119">Se o cliente pretende ler ou gravar a interface de fluxo ajustado que será retornada.</span><span class="sxs-lookup"><span data-stu-id="af994-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="af994-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="af994-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="af994-121">RTF descompactado deve ser gravada no fluxo apontado pela _lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="af994-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="af994-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="af994-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="af994-123">[out] Ponteiro para o local onde **WrapCompressedRTFStream** retorna um fluxo para o RTF descompactado.</span><span class="sxs-lookup"><span data-stu-id="af994-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="af994-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="af994-124">Return value</span></span>

<span data-ttu-id="af994-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="af994-125">S_OK</span></span> 
  
> <span data-ttu-id="af994-126">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="af994-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af994-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="af994-127">Remarks</span></span>

<span data-ttu-id="af994-128">Se o sinalizador MAPI_MODIFY é passado no parâmetro _ulFlags_ , o parâmetro _lpCompressedRTFStream_ já deve estar aberto para leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="af994-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="af994-129">Novo e descompactado RTF texto deve ser gravado na interface da stream retornado em _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="af994-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="af994-130">Porque não é possível acrescentar stream existente, o texto da mensagem inteira deve ser gravado.</span><span class="sxs-lookup"><span data-stu-id="af994-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="af994-131">Se o parâmetro _ulFlags_ é passado zero, então _lpCompressedRTFStream_ pode ser aberto somente leitura.</span><span class="sxs-lookup"><span data-stu-id="af994-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="af994-132">Somente o texto da mensagem inteira pode ser lido para fora da interface do stream retornada em _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="af994-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="af994-133">Não é possível pesquisar iniciando ao meio do fluxo.</span><span class="sxs-lookup"><span data-stu-id="af994-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="af994-134">**WrapCompressedRTFStream** pressupõe que o ponteiro do fluxo compactado está definido como o início do stream.</span><span class="sxs-lookup"><span data-stu-id="af994-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="af994-135">Determinados métodos OLE **IStream** não são suportados pelo fluxo descompactado retornado.</span><span class="sxs-lookup"><span data-stu-id="af994-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="af994-136">Eles incluem **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**e **IStream::UnlockRegion**.</span><span class="sxs-lookup"><span data-stu-id="af994-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="af994-137">Para copiar para o fluxo inteiro, será necessária a um loop de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="af994-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="af994-138">Porque o cliente grava novo RTF no formato descompactado, ele deve usar **WrapCompressedRTFStream**, em vez de escrever diretamente no fluxo.</span><span class="sxs-lookup"><span data-stu-id="af994-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="af994-139">Clientes RTF reconhecimento devem procurar o sinalizador STORE_UNCOMPRESSED_RTF na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) e passá-la para **WrapCompressed RTFStream** , se ela estiver definida.</span><span class="sxs-lookup"><span data-stu-id="af994-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af994-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="af994-140">See also</span></span>



[<span data-ttu-id="af994-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="af994-141">RTFSync</span></span>](rtfsync.md)

