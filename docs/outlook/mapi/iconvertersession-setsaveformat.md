---
title: IConverterSessionSetSaveFormat
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
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f1a4834fc600cc93eeb7fc96563723326c7f2169
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766914"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="36504-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="36504-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="36504-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36504-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36504-105">Define o formato no qual o conversor retornará um fluxo MIME em [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="36504-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="36504-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36504-106">Parameters</span></span>

<span data-ttu-id="36504-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="36504-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="36504-108">[in] Salvar formato a ser usado para um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="36504-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="36504-109">Para obter mais informações, consulte o tipo de enum [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="36504-109">For more information, see the enum type [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="36504-110">**SAVE_RFC1521**: uso MIME, que é o padrão.</span><span class="sxs-lookup"><span data-stu-id="36504-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="36504-111">**SAVE_RFC822**: Use uuencode.</span><span class="sxs-lookup"><span data-stu-id="36504-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="36504-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="36504-112">Return values</span></span>

<span data-ttu-id="36504-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="36504-113">S_OK</span></span>
  
> <span data-ttu-id="36504-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="36504-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="36504-115">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="36504-115">MFCMAPI reference</span></span>

<span data-ttu-id="36504-116">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="36504-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36504-117">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="36504-117">**File**</span></span>|<span data-ttu-id="36504-118">**Function**</span><span class="sxs-lookup"><span data-stu-id="36504-118">**Function**</span></span>|<span data-ttu-id="36504-119">**Comment**</span><span class="sxs-lookup"><span data-stu-id="36504-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36504-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="36504-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="36504-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="36504-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="36504-122">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="36504-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="36504-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="36504-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="36504-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="36504-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="36504-125">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="36504-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36504-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="36504-126">See also</span></span>

- [<span data-ttu-id="36504-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36504-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="36504-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="36504-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="36504-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="36504-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="36504-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="36504-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="36504-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="36504-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="36504-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="36504-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="36504-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="36504-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="36504-134">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="36504-134">MAPI Constants</span></span>](mapi-constants.md)

