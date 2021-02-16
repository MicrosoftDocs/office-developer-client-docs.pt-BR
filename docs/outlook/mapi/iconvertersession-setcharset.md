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
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336656"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="47cd7-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="47cd7-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="47cd7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47cd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47cd7-105">Especifica um conjunto de caracteres opcional que o conversor MAPI para MIME usa ao converter uma mensagem MAPI em um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="47cd7-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="47cd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47cd7-106">Parameters</span></span>

 <span data-ttu-id="47cd7-107">_fApply_</span><span class="sxs-lookup"><span data-stu-id="47cd7-107">_fApply_</span></span>
  
> <span data-ttu-id="47cd7-108">[in] Indica se um conjunto de caracteres específico deve ser usado para a conversão.</span><span class="sxs-lookup"><span data-stu-id="47cd7-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="47cd7-109">De definir esse parâmetro **como true** para aplicar o conjunto de caracteres em conversões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="47cd7-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="47cd7-110">De definida como **false se** você não quiser mais aplicar qualquer conjunto de caracteres específico e retornar aos padrões para mensagens subsequentes.</span><span class="sxs-lookup"><span data-stu-id="47cd7-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="47cd7-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="47cd7-111">_hcharset_</span></span>
  
> <span data-ttu-id="47cd7-112">[in] Um alça para um conjunto de caracteres, conforme definido em mimeole.h do Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="47cd7-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="47cd7-113">**Especifique** nulo para especificar que você não deseja aplicar qualquer conjunto de caracteres específico.</span><span class="sxs-lookup"><span data-stu-id="47cd7-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="47cd7-114">Para valores não **nulos,** use uma função como [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) para obter um alça para o conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="47cd7-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="47cd7-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="47cd7-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="47cd7-116">[in] Indica como aplicar um conjunto de caracteres para converter uma mensagem, conforme definido em mimeole.h do Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="47cd7-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47cd7-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="47cd7-117">Return value</span></span>

<span data-ttu-id="47cd7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="47cd7-118">S_OK</span></span>
  
> <span data-ttu-id="47cd7-119">A chamada de função é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="47cd7-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="47cd7-120">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="47cd7-120">MFCMAPI reference</span></span>

<span data-ttu-id="47cd7-121">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="47cd7-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="47cd7-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="47cd7-122">**File**</span></span>|<span data-ttu-id="47cd7-123">**Função**</span><span class="sxs-lookup"><span data-stu-id="47cd7-123">**Function**</span></span>|<span data-ttu-id="47cd7-124">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="47cd7-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="47cd7-125">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="47cd7-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="47cd7-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="47cd7-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="47cd7-127">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="47cd7-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="47cd7-128">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="47cd7-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="47cd7-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="47cd7-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="47cd7-130">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="47cd7-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47cd7-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="47cd7-131">See also</span></span>



[<span data-ttu-id="47cd7-132">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47cd7-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="47cd7-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="47cd7-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="47cd7-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="47cd7-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="47cd7-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="47cd7-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="47cd7-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="47cd7-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="47cd7-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="47cd7-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="47cd7-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="47cd7-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

