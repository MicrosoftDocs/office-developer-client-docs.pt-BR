---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336628"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="f073a-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="f073a-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="f073a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f073a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f073a-105">Define a largura de disposição do texto para um fluxo MIME que o conversor retornará no [IConverterSession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="f073a-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="f073a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f073a-106">Parameters</span></span>

 <span data-ttu-id="f073a-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="f073a-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="f073a-108">no Se o texto deve ser quebrado ou não.</span><span class="sxs-lookup"><span data-stu-id="f073a-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="f073a-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="f073a-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="f073a-110">no A largura da disposição do texto a ser usada.</span><span class="sxs-lookup"><span data-stu-id="f073a-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f073a-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f073a-111">Return value</span></span>

<span data-ttu-id="f073a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f073a-112">S_OK</span></span>
  
> <span data-ttu-id="f073a-113">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f073a-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f073a-114">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f073a-114">MFCMAPI reference</span></span>

<span data-ttu-id="f073a-115">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f073a-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f073a-116">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f073a-116">**File**</span></span>|<span data-ttu-id="f073a-117">**Função**</span><span class="sxs-lookup"><span data-stu-id="f073a-117">**Function**</span></span>|<span data-ttu-id="f073a-118">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f073a-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f073a-119">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="f073a-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="f073a-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="f073a-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="f073a-121">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="f073a-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="f073a-122">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="f073a-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="f073a-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="f073a-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="f073a-124">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="f073a-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f073a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f073a-125">See also</span></span>



[<span data-ttu-id="f073a-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f073a-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="f073a-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="f073a-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="f073a-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="f073a-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="f073a-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="f073a-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="f073a-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="f073a-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="f073a-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="f073a-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="f073a-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="f073a-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="f073a-133">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="f073a-133">MAPI Constants</span></span>](mapi-constants.md)

