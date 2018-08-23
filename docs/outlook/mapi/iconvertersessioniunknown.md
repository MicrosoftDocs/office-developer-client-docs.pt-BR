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
ms.openlocfilehash: 316e17e7804e754eed4ee4fef27211fb5173d4bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589641"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="bb47e-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb47e-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="bb47e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb47e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb47e-105">Permite conversões entre os objetos MIME e mensagens MAPI.</span><span class="sxs-lookup"><span data-stu-id="bb47e-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="bb47e-106">Isso pode ser útil em transporte de mensagens pela Internet.</span><span class="sxs-lookup"><span data-stu-id="bb47e-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb47e-107">Provided by:</span><span class="sxs-lookup"><span data-stu-id="bb47e-107">Provided by:</span></span>  <br/> |<span data-ttu-id="bb47e-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="bb47e-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="bb47e-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="bb47e-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bb47e-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="bb47e-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bb47e-111">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="bb47e-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb47e-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="bb47e-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="bb47e-113">Especifica um catálogo de endereços MAPI opcional que usa de MAPI conversor de MIME para resolver endereços ambíguos ao converter uma mensagem MAPI para um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="bb47e-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="bb47e-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="bb47e-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="bb47e-115">Inicializa a codificação a ser usada durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="bb47e-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="bb47e-116">*Membro do espaço reservado*</span><span class="sxs-lookup"><span data-stu-id="bb47e-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb47e-117">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="bb47e-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="bb47e-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="bb47e-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="bb47e-119">Converte um fluxo MIME em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="bb47e-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="bb47e-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="bb47e-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="bb47e-121">Converte uma mensagem MAPI em um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="bb47e-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="bb47e-122">*Membro do espaço reservado*</span><span class="sxs-lookup"><span data-stu-id="bb47e-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb47e-123">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="bb47e-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bb47e-124">*Membro do espaço reservado*</span><span class="sxs-lookup"><span data-stu-id="bb47e-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb47e-125">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="bb47e-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bb47e-126">*Membro do espaço reservado*</span><span class="sxs-lookup"><span data-stu-id="bb47e-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb47e-127">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="bb47e-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="bb47e-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="bb47e-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="bb47e-129">Define o largura de um fluxo MIME que o conversor retorna em **MAPIToMIMEStm**de quebra de texto.</span><span class="sxs-lookup"><span data-stu-id="bb47e-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="bb47e-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="bb47e-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="bb47e-131">Define o formato que o conversor retorna um fluxo MIME em **MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="bb47e-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="bb47e-132">*Membro do espaço reservado*</span><span class="sxs-lookup"><span data-stu-id="bb47e-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb47e-133">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="bb47e-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="bb47e-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="bb47e-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="bb47e-135">Especifica o que conjunto de um caractere opcional que MAPI conversor de MIME usa ao converter uma mensagem MAPI para um fluxo MIME.</span><span class="sxs-lookup"><span data-stu-id="bb47e-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb47e-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb47e-136">Remarks</span></span>

<span data-ttu-id="bb47e-137">Chame **SetEncoding** antes de usar **MAPIToMIMEStm** para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="bb47e-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb47e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb47e-138">See also</span></span>



[<span data-ttu-id="bb47e-139">Sobre a API de conversão MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="bb47e-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="bb47e-140">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="bb47e-140">MAPI Constants</span></span>](mapi-constants.md)

