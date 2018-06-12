---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770280"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="89e00-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="89e00-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="89e00-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89e00-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89e00-105">Essa estrutura fornece informações sobre um fluxo no formato nativo retornado da descompactando o corpo de uma mensagem que é encapsulado no compactado Rich Text Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="89e00-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="89e00-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="89e00-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="89e00-107">Membros</span><span class="sxs-lookup"><span data-stu-id="89e00-107">Members</span></span>

<span data-ttu-id="89e00-108">_tamanho_</span><span class="sxs-lookup"><span data-stu-id="89e00-108">_size_</span></span>
  
> <span data-ttu-id="89e00-109">O tamanho da estrutura **RTF_WCSRETINFO** em número de bytes.</span><span class="sxs-lookup"><span data-stu-id="89e00-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="89e00-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="89e00-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="89e00-111">Este é um valor que indica o formato do corpo da nativo.</span><span class="sxs-lookup"><span data-stu-id="89e00-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="89e00-112">Este valor só será válido se o sinalizador **MAPI_NATIVE_BODY** é passado no parâmetro _ulFlags_ da estrutura [RTF_WCSINFO](rtf_wcsinfo.md) que é passado para a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="89e00-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="89e00-113">Isso pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="89e00-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="89e00-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="89e00-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="89e00-115">Esse valor é usado apenas se _ulFlags_ inclui o sinalizador **MAPI_NATIVE_BODY** e corpo for RTF.</span><span class="sxs-lookup"><span data-stu-id="89e00-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="89e00-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="89e00-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="89e00-117">Esse valor é usado apenas se _ulFlags_ inclui o sinalizador **MAPI_NATIVE_BODY** e o corpo é o formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="89e00-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="89e00-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="89e00-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="89e00-119">Esse valor é usado apenas se _ulFlags_ inclui o sinalizador **MAPI_NATIVE_BODY** e o corpo é o formato de linguagem de marcação de hipertexto (HTML).</span><span class="sxs-lookup"><span data-stu-id="89e00-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89e00-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="89e00-120">See also</span></span>

- [<span data-ttu-id="89e00-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="89e00-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

