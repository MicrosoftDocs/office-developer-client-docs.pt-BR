---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429191"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="3724d-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="3724d-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="3724d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3724d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3724d-105">Especifica um Address Book MAPI opcional que o conversor MAPI para MIME usa para resolver endereços ambíguos ao converter uma mensagem MAPI em um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="3724d-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="3724d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3724d-106">Parameters</span></span>

 <span data-ttu-id="3724d-107">_pab_</span><span class="sxs-lookup"><span data-stu-id="3724d-107">_pab_</span></span>
  
> <span data-ttu-id="3724d-108">[in] Ponteiro para um [IAddrBook : interface IMAPIProp](iaddrbookimapiprop.md) a ser usada na conversão MAPI para MIME.</span><span class="sxs-lookup"><span data-stu-id="3724d-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="3724d-109">De definir esse parâmetro como **nulo** quando você não precisar mais do Address Book; isso libera a interface e redefine o conversor para não usar o Address Book.</span><span class="sxs-lookup"><span data-stu-id="3724d-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3724d-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3724d-110">Return value</span></span>

<span data-ttu-id="3724d-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3724d-111">S_OK</span></span>
  
> <span data-ttu-id="3724d-112">A chamada de função é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3724d-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3724d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3724d-113">Remarks</span></span>

<span data-ttu-id="3724d-114">A conversão de uma mensagem MAPI em fluxo MIME geralmente não requer logor em um perfil MAPI.</span><span class="sxs-lookup"><span data-stu-id="3724d-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="3724d-115">No entanto, a especificação de um Address Book MAPI para conversão requer o registro em um perfil para obter o Address Book.</span><span class="sxs-lookup"><span data-stu-id="3724d-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3724d-116">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3724d-116">MFCMAPI reference</span></span>

<span data-ttu-id="3724d-117">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3724d-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3724d-118">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="3724d-118">**File**</span></span>|<span data-ttu-id="3724d-119">**Função**</span><span class="sxs-lookup"><span data-stu-id="3724d-119">**Function**</span></span>|<span data-ttu-id="3724d-120">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="3724d-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3724d-121">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="3724d-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3724d-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="3724d-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="3724d-123">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="3724d-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="3724d-124">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="3724d-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3724d-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="3724d-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="3724d-126">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="3724d-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3724d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3724d-127">See also</span></span>



[<span data-ttu-id="3724d-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3724d-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="3724d-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="3724d-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="3724d-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="3724d-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="3724d-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="3724d-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="3724d-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="3724d-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="3724d-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="3724d-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="3724d-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="3724d-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

