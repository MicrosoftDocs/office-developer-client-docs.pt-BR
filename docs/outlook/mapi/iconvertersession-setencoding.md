---
title: IConverterSessionSetEncoding
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
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341297"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="8deb6-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="8deb6-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="8deb6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8deb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8deb6-105">Inicializa a codificação a ser usada durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="8deb6-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="8deb6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8deb6-106">Parameters</span></span>

<span data-ttu-id="8deb6-107">_et_</span><span class="sxs-lookup"><span data-stu-id="8deb6-107">_et_</span></span>
  
> <span data-ttu-id="8deb6-108">Um [](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) valor EncodingType.</span><span class="sxs-lookup"><span data-stu-id="8deb6-108">An [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="8deb6-109">Só há suporte para os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="8deb6-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="8deb6-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="8deb6-110">IET_BASE64</span></span>
   - <span data-ttu-id="8deb6-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="8deb6-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="8deb6-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="8deb6-112">IET_QP</span></span>
   - <span data-ttu-id="8deb6-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="8deb6-113">IET_7BIT</span></span>
   - <span data-ttu-id="8deb6-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="8deb6-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8deb6-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8deb6-115">Return value</span></span>

<span data-ttu-id="8deb6-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8deb6-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="8deb6-117">O tipo de codificação passado era inválido.</span><span class="sxs-lookup"><span data-stu-id="8deb6-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8deb6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8deb6-118">Remarks</span></span>

<span data-ttu-id="8deb6-119">Chame **setencoding** antes de usar [IConverterSession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="8deb6-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="8deb6-120">Use **setencoding** para definir a codificação somente para o corpo de mensagem mais externo de um item de email.</span><span class="sxs-lookup"><span data-stu-id="8deb6-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="8deb6-121">Microsoft Outlook 2010 e Microsoft Outlook 2013 escolha a codificação para qualquer anexo individual.</span><span class="sxs-lookup"><span data-stu-id="8deb6-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8deb6-122">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8deb6-122">MFCMAPI reference</span></span>

<span data-ttu-id="8deb6-123">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8deb6-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8deb6-124">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="8deb6-124">**File**</span></span>|<span data-ttu-id="8deb6-125">**Função**</span><span class="sxs-lookup"><span data-stu-id="8deb6-125">**Function**</span></span>|<span data-ttu-id="8deb6-126">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="8deb6-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8deb6-127">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="8deb6-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="8deb6-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="8deb6-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="8deb6-129">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="8deb6-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="8deb6-130">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="8deb6-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="8deb6-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="8deb6-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="8deb6-132">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="8deb6-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8deb6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8deb6-133">See also</span></span>

- [<span data-ttu-id="8deb6-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8deb6-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="8deb6-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="8deb6-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="8deb6-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="8deb6-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="8deb6-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="8deb6-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="8deb6-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="8deb6-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="8deb6-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="8deb6-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="8deb6-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="8deb6-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="8deb6-141">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="8deb6-141">MAPI Constants</span></span>](mapi-constants.md)

