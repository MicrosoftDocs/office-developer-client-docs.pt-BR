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
ms.openlocfilehash: ae00fd0711b8fcae01db6a89da7607d79d8757c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584356"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="02727-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="02727-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="02727-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02727-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02727-105">Especifica um catálogo de endereços MAPI opcional que usa de MAPI conversor de MIME para resolver endereços ambíguos ao converter uma mensagem MAPI para um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="02727-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="02727-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02727-106">Parameters</span></span>

 <span data-ttu-id="02727-107">_PAB_</span><span class="sxs-lookup"><span data-stu-id="02727-107">_pab_</span></span>
  
> <span data-ttu-id="02727-108">[in] Ponteiro para uma [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interface a ser usado na MAPI para conversão de MIME.</span><span class="sxs-lookup"><span data-stu-id="02727-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="02727-109">Defina esse parâmetro como **null** quando não precisar mais o catálogo de endereços; Isso libera a interface e redefine o conversor para não usar qualquer catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="02727-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="02727-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="02727-110">Return value</span></span>

<span data-ttu-id="02727-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="02727-111">S_OK</span></span>
  
> <span data-ttu-id="02727-112">A chamada de função é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="02727-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="02727-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="02727-113">Remarks</span></span>

<span data-ttu-id="02727-114">Convertendo um MAPI mensagem para o fluxo de MIME geralmente não exige o registro em log em um perfil MAPI.</span><span class="sxs-lookup"><span data-stu-id="02727-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="02727-115">Entretanto, a especificação de um catálogo de endereços MAPI para conversão requer logon a um perfil para obter o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="02727-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="02727-116">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="02727-116">MFCMAPI reference</span></span>

<span data-ttu-id="02727-117">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="02727-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="02727-118">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="02727-118">**File**</span></span>|<span data-ttu-id="02727-119">**Function**</span><span class="sxs-lookup"><span data-stu-id="02727-119">**Function**</span></span>|<span data-ttu-id="02727-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="02727-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02727-121">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="02727-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="02727-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="02727-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="02727-123">MFCMAPI usa MimeToMAPI para converter um arquivo EML em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="02727-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="02727-124">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="02727-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="02727-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="02727-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="02727-126">MFCMAPI usa MAPIToMIMEStm para converter uma mensagem MAPI em um arquivo EML.</span><span class="sxs-lookup"><span data-stu-id="02727-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02727-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="02727-127">See also</span></span>



[<span data-ttu-id="02727-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02727-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="02727-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="02727-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="02727-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="02727-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="02727-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="02727-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="02727-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="02727-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="02727-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="02727-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="02727-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="02727-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

