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
ms.openlocfilehash: 1803707b46b9b58e7372e7e58cc36241d0ebdb4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571721"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="9d672-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d672-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="9d672-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d672-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d672-105">Fornece métodos para encapsular propriedades MAPI que não são suportadas por um sistema de mensagens em binários fluxos que podem ser anexados às mensagens.</span><span class="sxs-lookup"><span data-stu-id="9d672-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="9d672-106">O formato usado para este encapsulamento é o transporte-TNEF Neutral Encapsulation Format ().</span><span class="sxs-lookup"><span data-stu-id="9d672-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="9d672-107">O provedor de transporte de destino ou de um aplicativo cliente baseado em MAPI, ao receber uma mensagem que inclui um anexo TNEF, recuperem as propriedades do anexo.</span><span class="sxs-lookup"><span data-stu-id="9d672-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d672-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9d672-108">Header file:</span></span>  <br/> |<span data-ttu-id="9d672-109">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="9d672-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="9d672-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="9d672-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="9d672-111">Objetos TNEF</span><span class="sxs-lookup"><span data-stu-id="9d672-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="9d672-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="9d672-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d672-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="9d672-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="9d672-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="9d672-114">Called by:</span></span>  <br/> |<span data-ttu-id="9d672-115">Provedores de transporte, provedores de armazenamento de mensagem e gateways</span><span class="sxs-lookup"><span data-stu-id="9d672-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="9d672-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="9d672-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9d672-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="9d672-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="9d672-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="9d672-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="9d672-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="9d672-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9d672-120">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="9d672-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9d672-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="9d672-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="9d672-122">Permite que o provedor de serviços de chamada ou gateway adicionar propriedades ao encapsulamento de uma mensagem ou um anexo.</span><span class="sxs-lookup"><span data-stu-id="9d672-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="9d672-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="9d672-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="9d672-124">Extrai as propriedades de um encapsulamento TNEF.</span><span class="sxs-lookup"><span data-stu-id="9d672-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="9d672-125">Finish</span><span class="sxs-lookup"><span data-stu-id="9d672-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="9d672-126">Tiver terminado de processamento de todas as operações de TNEF que estão enfileiradas e em espera.</span><span class="sxs-lookup"><span data-stu-id="9d672-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="9d672-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="9d672-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="9d672-128">Abre uma interface de fluxo no texto de uma mensagem encapsulado.</span><span class="sxs-lookup"><span data-stu-id="9d672-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="9d672-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="9d672-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="9d672-130">Define o valor de uma ou mais propriedades para uma mensagem encapsulada ou um anexo sem modificar a mensagem original ou um anexo.</span><span class="sxs-lookup"><span data-stu-id="9d672-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="9d672-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="9d672-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="9d672-132">Codifica um modo de exibição da tabela do destinatário da mensagem o fluxo de dados TNEF da mensagem.</span><span class="sxs-lookup"><span data-stu-id="9d672-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="9d672-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="9d672-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="9d672-134">Processa os componentes individuais de uma mensagem de um por vez em um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="9d672-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d672-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d672-135">See also</span></span>



[<span data-ttu-id="9d672-136">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9d672-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

