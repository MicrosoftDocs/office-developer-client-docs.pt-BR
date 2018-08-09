---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bdb879a2412c817b7b314cd7bf6de1fa4c9f40d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770720"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="0ced7-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="0ced7-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="0ced7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ced7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ced7-105">Descompacta o corpo de uma mensagem de email que está no compactado Rich Text Format (RTF), indica o formato do fluxo descompactado, opcionalmente converte o fluxo descompactado em seu formato nativo e retorna o fluxo de descompactados ou o convertido stream nativo.</span><span class="sxs-lookup"><span data-stu-id="0ced7-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0ced7-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="0ced7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ced7-107">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="0ced7-107">Exported by:</span></span>  <br/> |<span data-ttu-id="0ced7-108">Msmapi32</span><span class="sxs-lookup"><span data-stu-id="0ced7-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="0ced7-109">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0ced7-109">Called by:</span></span>  <br/> |<span data-ttu-id="0ced7-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="0ced7-110">Client</span></span>  <br/> |
|<span data-ttu-id="0ced7-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0ced7-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="0ced7-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="0ced7-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="0ced7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ced7-113">Parameters</span></span>

<span data-ttu-id="0ced7-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="0ced7-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="0ced7-115">[in] Este é um ponteiro para um fluxo que é aberto na [Propriedade canônico de PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ced7-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="0ced7-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="0ced7-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="0ced7-117">[in] Este é um ponteiro para um</span><span class="sxs-lookup"><span data-stu-id="0ced7-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="0ced7-118">Estrutura [RTF_WCSINFO](rtf_wcsinfo.md) que contém opções para a função.</span><span class="sxs-lookup"><span data-stu-id="0ced7-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="0ced7-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="0ced7-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="0ced7-120">[out] Este é um ponteiro para o local onde um stream para o RTF descompactado é retornado.</span><span class="sxs-lookup"><span data-stu-id="0ced7-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="0ced7-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="0ced7-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="0ced7-122">[out] Este é um ponteiro para uma estrutura [RTF_WCSRETINFO](rtf_wcsretinfo.md) que contém informações sobre o formato do fluxo retornado descompactado.</span><span class="sxs-lookup"><span data-stu-id="0ced7-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="0ced7-123">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="0ced7-123">Return values</span></span>

<span data-ttu-id="0ced7-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ced7-124">S_OK</span></span> 
  
- <span data-ttu-id="0ced7-125">A chamada de função é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0ced7-125">The function call is successful.</span></span>
    
<span data-ttu-id="0ced7-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0ced7-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="0ced7-127">Isso será retornado se o sinalizador **MAPI_NATIVE_BODY** é combinado com o sinalizador **MAPI_MODIFY** no campo **ulFlags** da estrutura **RTF_WCSINFO** apontado por *pWCSInfo* .</span><span class="sxs-lookup"><span data-stu-id="0ced7-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0ced7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ced7-128">Remarks</span></span>

<span data-ttu-id="0ced7-129">**WrapCompressedRTFStreamEx** permite que você acesse o corpo de uma mensagem de email encapsulado em RTF compactado, descompactando o fluxo, retorna stream descompactado e seu formato e, opcionalmente, o fluxo de corpo nativo.</span><span class="sxs-lookup"><span data-stu-id="0ced7-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="0ced7-130">O fluxo de corpo nativo pode estar em RTF, HTML ou texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="0ced7-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="0ced7-131">O modelo de objeto do Microsoft Office Outlook fornece uma propriedade de **corpo** de uma [Propriedade MailItem BodyFormat (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) que indica o formato do corpo de texto e objetos de **MailItem** .</span><span class="sxs-lookup"><span data-stu-id="0ced7-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="0ced7-132">Por design, uma solução que não é confiável pelo Outlook invoca caixas de diálogo de segurança geradas pelo protetor de segurança do Outlook.</span><span class="sxs-lookup"><span data-stu-id="0ced7-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="0ced7-133">Usando a função MAPI exportada **WrapCompressedRTFStreamEx** permite que uma solução para usar MAPI em vez de modelo de objeto do Outlook e evitar essas caixas de diálogo de segurança.</span><span class="sxs-lookup"><span data-stu-id="0ced7-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="0ced7-134">Porque o **MAPI\_NATIVE_BODY** sinalizador não pode ser combinado com o **MAPI\_modificar** sinalizador no campo **ulFlags** do **RTF\_WCSINFO** estrutura apontado pela *pWCSInfo*, você só poderá acessar o nativo fluxo do corpo em modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0ced7-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="0ced7-135">Para acessar o fluxo de corpo nativos no modo leitura/gravação, você deve usar a função **WrapCompressedRTFStream** .</span><span class="sxs-lookup"><span data-stu-id="0ced7-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ced7-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ced7-136">See also</span></span>

- [<span data-ttu-id="0ced7-137">Recuperar o corpo de uma mensagem em RTF compactado e convertê-lo ao formato nativo</span><span class="sxs-lookup"><span data-stu-id="0ced7-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

