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
# <a name="rtf_wcsinfo"></a><span data-ttu-id="d3bcd-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="d3bcd-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="d3bcd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3bcd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3bcd-105">Essa estrutura permite especificar informações para descompactar o corpo de uma mensagem em RTF (Formato Rich Text) compactado e, opcionalmente, retornar o fluxo de corpo em seu formato nativo.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d3bcd-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d3bcd-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="d3bcd-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d3bcd-107">Members</span></span>

 <span data-ttu-id="d3bcd-108">_size_</span><span class="sxs-lookup"><span data-stu-id="d3bcd-108">_size_</span></span>
  
> <span data-ttu-id="d3bcd-109">O tamanho da estrutura **RTF_WCSINFO** em número de bytes.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="d3bcd-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3bcd-110">_ulFlags_</span></span>
  
> <span data-ttu-id="d3bcd-111">Esta é a máscara de bits dos sinalizadores de opção para [a função WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="d3bcd-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="d3bcd-112">Os sinalizadores de opção com suporte são:</span><span class="sxs-lookup"><span data-stu-id="d3bcd-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="d3bcd-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d3bcd-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="d3bcd-114">Isso indica se o cliente pretende gravar a interface de fluxo envolvida que é retornada.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="d3bcd-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="d3bcd-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="d3bcd-116">Isso indica se o RTF descompactado deve ser gravado no fluxo apontado pelo ponteiro _lpCompressedRTFStream_ da função [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="d3bcd-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="d3bcd-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="d3bcd-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="d3bcd-118">Isso indica se o fluxo descompactado também é convertido no corpo nativo antes de retornar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="d3bcd-119">Esse sinalizador não pode ser combinado com o **MAPI_MODIFY** sinalizador.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="d3bcd-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="d3bcd-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="d3bcd-121">Este é o valor da página de código da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-121">This is the code page value of the message.</span></span> <span data-ttu-id="d3bcd-122">Normalmente, esse valor é obtido da propriedade canônica [PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) na mensagem.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="d3bcd-123">Esse valor só é usado quando o **MAPI_NATIVE_BODY** sinalizador é passado  _em ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="d3bcd-124">Caso contrário, esse valor será ignorado.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="d3bcd-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="d3bcd-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="d3bcd-126">Esse é o valor de página de código do fluxo descompactado retornado que você deseja.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="d3bcd-127">Se isso for definido como um valor não zero, a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) converterá o fluxo na página de código especificada.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="d3bcd-128">Se isso for definido como um valor zero, o MAPI decidirá qual página de código usar.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="d3bcd-129">Esse valor é usado somente quando o **MAPI_NATIVE_BODY** sinalizador é passado  _em ulFlags_ e o formato do corpo não é RTF.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="d3bcd-130">Caso contrário, esse valor será ignorado.</span><span class="sxs-lookup"><span data-stu-id="d3bcd-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3bcd-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3bcd-131">See also</span></span>



[<span data-ttu-id="d3bcd-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="d3bcd-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

