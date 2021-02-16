---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428512"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="06f7e-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="06f7e-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="06f7e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06f7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06f7e-105">Fornece métodos para encapsular propriedades MAPI que não são suportadas por um sistema de mensagens em fluxos binários que podem ser anexados a mensagens.</span><span class="sxs-lookup"><span data-stu-id="06f7e-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="06f7e-106">O formato usado para esse encapsulamento é o Transport-Neutral encapsulamento (TNEF).</span><span class="sxs-lookup"><span data-stu-id="06f7e-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="06f7e-107">O provedor de transporte de destino ou o aplicativo cliente baseado em MAPI podem, ao receber uma mensagem que inclui um anexo TNEF, recuperar as propriedades do anexo.</span><span class="sxs-lookup"><span data-stu-id="06f7e-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06f7e-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="06f7e-108">Header file:</span></span>  <br/> |<span data-ttu-id="06f7e-109">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="06f7e-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="06f7e-110">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="06f7e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="06f7e-111">Objetos TNEF</span><span class="sxs-lookup"><span data-stu-id="06f7e-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="06f7e-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="06f7e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="06f7e-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="06f7e-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="06f7e-114">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="06f7e-114">Called by:</span></span>  <br/> |<span data-ttu-id="06f7e-115">Provedores de transporte, provedores de armazenamento de mensagens e gateways</span><span class="sxs-lookup"><span data-stu-id="06f7e-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="06f7e-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="06f7e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="06f7e-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="06f7e-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="06f7e-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="06f7e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="06f7e-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="06f7e-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="06f7e-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="06f7e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="06f7e-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="06f7e-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="06f7e-122">Permite que o provedor de serviços de chamada ou gateway adicione propriedades ao encapsulamento de uma mensagem ou anexo.</span><span class="sxs-lookup"><span data-stu-id="06f7e-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="06f7e-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="06f7e-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="06f7e-124">Extrai as propriedades de um encapsulamento TNEF.</span><span class="sxs-lookup"><span data-stu-id="06f7e-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="06f7e-125">Finish</span><span class="sxs-lookup"><span data-stu-id="06f7e-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="06f7e-126">Finaliza o processamento de todas as operações TNEF que estão em fila e aguardando.</span><span class="sxs-lookup"><span data-stu-id="06f7e-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="06f7e-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="06f7e-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="06f7e-128">Abre uma interface de fluxo no texto de uma mensagem encapsulada.</span><span class="sxs-lookup"><span data-stu-id="06f7e-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="06f7e-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="06f7e-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="06f7e-130">Define o valor de uma ou mais propriedades para uma mensagem ou anexo encapsulado sem modificar a mensagem ou o anexo original.</span><span class="sxs-lookup"><span data-stu-id="06f7e-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="06f7e-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="06f7e-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="06f7e-132">Codifica uma exibição para a tabela de destinatários de uma mensagem no fluxo de dados TNEF da mensagem.</span><span class="sxs-lookup"><span data-stu-id="06f7e-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="06f7e-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="06f7e-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="06f7e-134">Processa componentes individuais de uma mensagem, um de cada vez, em um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="06f7e-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06f7e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="06f7e-135">See also</span></span>



[<span data-ttu-id="06f7e-136">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="06f7e-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

