---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432314"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="61aed-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61aed-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="61aed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61aed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61aed-105">Permite conversões entre objetos MIME e mensagens MAPI.</span><span class="sxs-lookup"><span data-stu-id="61aed-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="61aed-106">Isso pode ser útil no transporte de mensagens pela Internet.</span><span class="sxs-lookup"><span data-stu-id="61aed-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61aed-107">Provided by:</span><span class="sxs-lookup"><span data-stu-id="61aed-107">Provided by:</span></span>  <br/> |<span data-ttu-id="61aed-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="61aed-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="61aed-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="61aed-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="61aed-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="61aed-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="61aed-111">Vtable order</span><span class="sxs-lookup"><span data-stu-id="61aed-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61aed-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="61aed-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="61aed-113">Especifica um Address Book MAPI opcional que o conversor MAPI para MIME usa para resolver endereços ambíguos ao converter uma mensagem MAPI em um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="61aed-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="61aed-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="61aed-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="61aed-115">Inicializa a codificação a ser usada durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="61aed-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="61aed-116">*Membro placeholder*</span><span class="sxs-lookup"><span data-stu-id="61aed-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="61aed-117">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="61aed-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="61aed-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="61aed-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="61aed-119">Converte um fluxo MIME em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="61aed-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="61aed-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="61aed-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="61aed-121">Converte uma mensagem MAPI em um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="61aed-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="61aed-122">*Membro placeholder*</span><span class="sxs-lookup"><span data-stu-id="61aed-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="61aed-123">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="61aed-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="61aed-124">*Membro placeholder*</span><span class="sxs-lookup"><span data-stu-id="61aed-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="61aed-125">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="61aed-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="61aed-126">*Membro placeholder*</span><span class="sxs-lookup"><span data-stu-id="61aed-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="61aed-127">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="61aed-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="61aed-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="61aed-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="61aed-129">Define a largura da quebra de texto para um fluxo MIME que o conversor retorna em **MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="61aed-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="61aed-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="61aed-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="61aed-131">Define o formato que o conversor retorna um fluxo MIME em **MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="61aed-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="61aed-132">*Membro placeholder*</span><span class="sxs-lookup"><span data-stu-id="61aed-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="61aed-133">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="61aed-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="61aed-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="61aed-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="61aed-135">Especifica um conjunto de caracteres opcional que o conversor MAPI para MIME usa ao converter uma mensagem MAPI em um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="61aed-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61aed-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="61aed-136">Remarks</span></span>

<span data-ttu-id="61aed-137">Chame **SetEncoding antes** de usar **MAPIToMIMEStm** para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="61aed-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61aed-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="61aed-138">See also</span></span>



[<span data-ttu-id="61aed-139">Sobre a API de conversão MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="61aed-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="61aed-140">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="61aed-140">MAPI Constants</span></span>](mapi-constants.md)

