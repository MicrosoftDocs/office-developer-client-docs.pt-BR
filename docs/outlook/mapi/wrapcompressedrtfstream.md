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
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325624"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="f51f0-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="f51f0-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="f51f0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f51f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f51f0-105">Cria um fluxo de texto no formato Rich Text (RTF) descompactado a partir do formato compactado usado na propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f51f0-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f51f0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f51f0-106">Header file:</span></span>  <br/> |<span data-ttu-id="f51f0-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f51f0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f51f0-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f51f0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f51f0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f51f0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f51f0-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f51f0-110">Called by:</span></span>  <br/> |<span data-ttu-id="f51f0-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="f51f0-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="f51f0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f51f0-112">Parameters</span></span>

 <span data-ttu-id="f51f0-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f51f0-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="f51f0-114">no Ponteiro para um Stream aberto na propriedade PR_RTF_COMPRESSED de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f51f0-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="f51f0-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f51f0-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f51f0-116">no Bitmask dos sinalizadores de opções para a função.</span><span class="sxs-lookup"><span data-stu-id="f51f0-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="f51f0-117">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f51f0-117">The following flags can be set:</span></span>
    
<span data-ttu-id="f51f0-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f51f0-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f51f0-119">Se o cliente pretende ler ou gravar a interface de fluxo encapsulada retornada.</span><span class="sxs-lookup"><span data-stu-id="f51f0-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="f51f0-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="f51f0-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="f51f0-121">O RTF descompactado deve ser gravado no fluxo apontado pelo _lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f51f0-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="f51f0-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f51f0-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="f51f0-123">bota Ponteiro para o local onde **WrapCompressedRTFStream** retorna um Stream para o RTF descompactado.</span><span class="sxs-lookup"><span data-stu-id="f51f0-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f51f0-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f51f0-124">Return value</span></span>

<span data-ttu-id="f51f0-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="f51f0-125">S_OK</span></span> 
  
> <span data-ttu-id="f51f0-126">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="f51f0-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f51f0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f51f0-127">Remarks</span></span>

<span data-ttu-id="f51f0-128">Se o sinalizador MAPI_MODIFY for passado no parâmetro _parâmetroulflags_ , o parâmetro _lpCompressedRTFStream_ já deverá estar aberto para leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="f51f0-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="f51f0-129">O texto RTF novo e descompactado deve ser gravado na interface de fluxo retornada no _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="f51f0-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="f51f0-130">Como não é possível acrescentar o fluxo existente, o texto da mensagem inteira deve ser gravado.</span><span class="sxs-lookup"><span data-stu-id="f51f0-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="f51f0-131">Se zero é passado no parâmetro _parâmetroulflags_ , _lpCompressedRTFStream_ pode ser aberto somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f51f0-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="f51f0-132">Somente todo o texto da mensagem pode ser lido da interface de fluxo retornada no _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="f51f0-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="f51f0-133">Não é possível pesquisar iniciando o meio do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f51f0-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="f51f0-134">**WrapCompressedRTFStream** assume que o ponteiro do fluxo compactado está definido para o início do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f51f0-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="f51f0-135">Determinados métodos OLE **IStream** não são suportados pelo Stream não compactado retornado.</span><span class="sxs-lookup"><span data-stu-id="f51f0-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="f51f0-136">Entre eles estão **IStream:: clone**, **IStream:: LockRegion**, **IStream:: reVert**, IStream:: **Seek**, IStream:: SetSize, **IStream:: stat**e **IStream:: UnlockRegion**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f51f0-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="f51f0-137">Para copiar para o fluxo inteiro, é necessário um loop de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f51f0-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="f51f0-138">Como o cliente grava novo RTF no formato descompactado, ele deve usar o **WrapCompressedRTFStream**, em vez de gravar diretamente no Stream.</span><span class="sxs-lookup"><span data-stu-id="f51f0-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="f51f0-139">Os clientes com reconhecimento de RTF devem procurar o sinalizador STORE_UNCOMPRESSED_RTF na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) e passá-lo para **WrapCompressed RTFStream** se ele estiver definido.</span><span class="sxs-lookup"><span data-stu-id="f51f0-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f51f0-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="f51f0-140">See also</span></span>



[<span data-ttu-id="f51f0-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="f51f0-141">RTFSync</span></span>](rtfsync.md)

