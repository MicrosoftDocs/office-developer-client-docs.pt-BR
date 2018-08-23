---
title: IConverterSessionSetCharSet
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
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 69023d2c13037fb52a4d1dc4f7376efbd839aebc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581696"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="6b767-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="6b767-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="6b767-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b767-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b767-105">Especifica que um caractere opcional definir que a MAPI para MIME conversor usar ao converter uma mensagem MAPI para um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="6b767-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="6b767-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b767-106">Parameters</span></span>

 <span data-ttu-id="6b767-107">_fApply_</span><span class="sxs-lookup"><span data-stu-id="6b767-107">_fApply_</span></span>
  
> <span data-ttu-id="6b767-108">[in] Indica se deve usar um conjunto para a conversão de caracteres específica.</span><span class="sxs-lookup"><span data-stu-id="6b767-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="6b767-109">Defina esse parâmetro como **true** para aplicar o conjunto de caracteres no conversões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6b767-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="6b767-110">Defina esse parâmetro como **false** , se você não deseja mais aplicar qualquer conjunto de caracteres específico e retornar aos padrões para mensagens subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6b767-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="6b767-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="6b767-111">_hcharset_</span></span>
  
> <span data-ttu-id="6b767-112">[in] Um identificador para um caractere definido como definido no mimeole.h do Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="6b767-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="6b767-113">Especifique **Nulo** para especificar que você não deseja aplicar qualquer conjunto de caracteres específico.</span><span class="sxs-lookup"><span data-stu-id="6b767-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="6b767-114">Para valores não - **Nulo** , use uma função como [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) para obter um identificador para o conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b767-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="6b767-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="6b767-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="6b767-116">[in] Indica como aplicar um conjunto de caracteres para converter uma mensagem, conforme definido na mimeole.h do Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="6b767-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b767-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6b767-117">Return value</span></span>

<span data-ttu-id="6b767-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b767-118">S_OK</span></span>
  
> <span data-ttu-id="6b767-119">A chamada de função é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6b767-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="6b767-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6b767-120">MFCMAPI reference</span></span>

<span data-ttu-id="6b767-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6b767-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6b767-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="6b767-122">**File**</span></span>|<span data-ttu-id="6b767-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="6b767-123">**Function**</span></span>|<span data-ttu-id="6b767-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6b767-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b767-125">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="6b767-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="6b767-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="6b767-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="6b767-127">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="6b767-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="6b767-128">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="6b767-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="6b767-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="6b767-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="6b767-130">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="6b767-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b767-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b767-131">See also</span></span>



[<span data-ttu-id="6b767-132">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b767-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="6b767-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="6b767-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="6b767-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="6b767-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="6b767-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="6b767-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="6b767-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="6b767-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="6b767-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="6b767-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="6b767-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="6b767-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

