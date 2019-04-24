---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315782"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="88b61-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="88b61-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="88b61-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88b61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88b61-105">Essa estrutura fornece informações sobre um fluxo no formato nativo retornado da descompactação do corpo de uma mensagem encapsulada em formato Rich Text (RTF) compactado.</span><span class="sxs-lookup"><span data-stu-id="88b61-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="88b61-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="88b61-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="88b61-107">Membros</span><span class="sxs-lookup"><span data-stu-id="88b61-107">Members</span></span>

<span data-ttu-id="88b61-108">_size_</span><span class="sxs-lookup"><span data-stu-id="88b61-108">_size_</span></span>
  
> <span data-ttu-id="88b61-109">O tamanho da estrutura **RTF_WCSRETINFO** em número de bytes.</span><span class="sxs-lookup"><span data-stu-id="88b61-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="88b61-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="88b61-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="88b61-111">Este é um valor que indica o formato do corpo nativo.</span><span class="sxs-lookup"><span data-stu-id="88b61-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="88b61-112">Esse valor só será válido se o sinalizador **MAPI_NATIVE_BODY** for passado no parâmetro _Parâmetroulflags_ da estrutura [RTF_WCSINFO](rtf_wcsinfo.md) que é passada para a função [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="88b61-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="88b61-113">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="88b61-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="88b61-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="88b61-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="88b61-115">Esse valor só será usado se _parâmetroulflags_ incluir o sinalizador **MAPI_NATIVE_BODY** e o corpo for RTF.</span><span class="sxs-lookup"><span data-stu-id="88b61-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="88b61-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="88b61-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="88b61-117">Esse valor é usado somente se _parâmetroulflags_ inclui o sinalizador **MAPI_NATIVE_BODY** e o corpo é o formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="88b61-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="88b61-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="88b61-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="88b61-119">Esse valor é usado somente se _parâmetroulflags_ inclui o sinalizador **MAPI_NATIVE_BODY** e o corpo é o formato HTML (Hypertext Markup Language).</span><span class="sxs-lookup"><span data-stu-id="88b61-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88b61-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="88b61-120">See also</span></span>

- [<span data-ttu-id="88b61-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="88b61-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

