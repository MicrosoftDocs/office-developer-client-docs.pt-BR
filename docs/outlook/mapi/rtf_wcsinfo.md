---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430529"
---
# <a name="rtfwcsinfo"></a><span data-ttu-id="fab58-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="fab58-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="fab58-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fab58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fab58-105">Essa estrutura permite que você especifique informações para descompactar o corpo de uma mensagem no formato Rich Text (RTF) compactado e, opcionalmente, retornar o fluxo do corpo em seu formato nativo.</span><span class="sxs-lookup"><span data-stu-id="fab58-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fab58-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="fab58-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="fab58-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fab58-107">Members</span></span>

 <span data-ttu-id="fab58-108">_size_</span><span class="sxs-lookup"><span data-stu-id="fab58-108">_size_</span></span>
  
> <span data-ttu-id="fab58-109">O tamanho da estrutura **RTF_WCSINFO** em número de bytes.</span><span class="sxs-lookup"><span data-stu-id="fab58-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="fab58-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fab58-110">_ulFlags_</span></span>
  
> <span data-ttu-id="fab58-111">Esta é a bitmask dos sinalizadores de opção para a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="fab58-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="fab58-112">Os sinalizadores de opção com suporte são:</span><span class="sxs-lookup"><span data-stu-id="fab58-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="fab58-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="fab58-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="fab58-114">Isso indica se o cliente pretende gravar a interface de fluxo encapsulada retornada.</span><span class="sxs-lookup"><span data-stu-id="fab58-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="fab58-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="fab58-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="fab58-116">Isso indica se o RTF descompactado deve ser gravado no fluxo que é apontado pelo ponteiro _lpCompressedRTFStream_ da função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="fab58-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="fab58-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="fab58-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="fab58-118">Isso indica se o fluxo descompactado também é convertido no corpo nativo antes de retornar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="fab58-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="fab58-119">Este sinalizador não pode ser combinado com o sinalizador **MAPI_MODIFY** .</span><span class="sxs-lookup"><span data-stu-id="fab58-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="fab58-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="fab58-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="fab58-121">Este é o valor da página de código da mensagem.</span><span class="sxs-lookup"><span data-stu-id="fab58-121">This is the code page value of the message.</span></span> <span data-ttu-id="fab58-122">Normalmente, esse valor é obtido da [Propriedade canônica PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) na mensagem.</span><span class="sxs-lookup"><span data-stu-id="fab58-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="fab58-123">Esse valor é usado apenas quando o sinalizador **MAPI_NATIVE_BODY** é passado em _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="fab58-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="fab58-124">Caso contrário, esse valor será ignorado.</span><span class="sxs-lookup"><span data-stu-id="fab58-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="fab58-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="fab58-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="fab58-126">Este é o valor da página de código do Stream descompactado retornado que você deseja.</span><span class="sxs-lookup"><span data-stu-id="fab58-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="fab58-127">Se for definido como um valor diferente de zero, a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) converte o Stream na página de código especificada.</span><span class="sxs-lookup"><span data-stu-id="fab58-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="fab58-128">Se for definido como um valor zero, MAPI decide qual página de código usar.</span><span class="sxs-lookup"><span data-stu-id="fab58-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="fab58-129">Esse valor é usado somente quando o sinalizador **MAPI_NATIVE_BODY** é passado em _parâmetroulflags_, e o formato do corpo não é RTF.</span><span class="sxs-lookup"><span data-stu-id="fab58-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="fab58-130">Caso contrário, esse valor será ignorado.</span><span class="sxs-lookup"><span data-stu-id="fab58-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fab58-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fab58-131">See also</span></span>



[<span data-ttu-id="fab58-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="fab58-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

