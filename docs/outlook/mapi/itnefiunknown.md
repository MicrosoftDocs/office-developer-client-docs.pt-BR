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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315033"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="31bb0-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="31bb0-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="31bb0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31bb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31bb0-105">Fornece métodos para o encapsulamento de propriedades MAPI que não são compatíveis com um sistema de mensagens em fluxos binários que podem ser anexados a mensagens.</span><span class="sxs-lookup"><span data-stu-id="31bb0-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="31bb0-106">O formato usado para esse encapsulamento é o formato de encapsulamento de transporte neutro (TNEF).</span><span class="sxs-lookup"><span data-stu-id="31bb0-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="31bb0-107">O provedor de transporte de destino ou aplicativo cliente baseado em MAPI pode então, ao receber uma mensagem que inclui um anexo TNEF, recupera as propriedades do anexo.</span><span class="sxs-lookup"><span data-stu-id="31bb0-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31bb0-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="31bb0-108">Header file:</span></span>  <br/> |<span data-ttu-id="31bb0-109">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="31bb0-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="31bb0-110">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="31bb0-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="31bb0-111">Objetos TNEF</span><span class="sxs-lookup"><span data-stu-id="31bb0-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="31bb0-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="31bb0-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="31bb0-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="31bb0-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="31bb0-114">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="31bb0-114">Called by:</span></span>  <br/> |<span data-ttu-id="31bb0-115">Provedores de transporte, provedores de repositórios de mensagens e gateways</span><span class="sxs-lookup"><span data-stu-id="31bb0-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="31bb0-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="31bb0-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="31bb0-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="31bb0-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="31bb0-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="31bb0-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="31bb0-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="31bb0-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="31bb0-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="31bb0-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="31bb0-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="31bb0-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="31bb0-122">Permite que o provedor de serviços de chamada ou o gateway adicione Propriedades ao encapsulamento de uma mensagem ou de um anexo.</span><span class="sxs-lookup"><span data-stu-id="31bb0-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="31bb0-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="31bb0-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="31bb0-124">Extrai as propriedades de um encapsulamento TNEF.</span><span class="sxs-lookup"><span data-stu-id="31bb0-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="31bb0-125">Finish</span><span class="sxs-lookup"><span data-stu-id="31bb0-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="31bb0-126">Conclui o processamento de todas as operações TNEF que estão na fila e aguardando.</span><span class="sxs-lookup"><span data-stu-id="31bb0-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="31bb0-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="31bb0-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="31bb0-128">Abre uma interface de fluxo no texto de uma mensagem encapsulada.</span><span class="sxs-lookup"><span data-stu-id="31bb0-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="31bb0-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="31bb0-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="31bb0-130">Define o valor de uma ou mais propriedades de uma mensagem encapsulada ou anexo sem modificar a mensagem original ou o anexo.</span><span class="sxs-lookup"><span data-stu-id="31bb0-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="31bb0-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="31bb0-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="31bb0-132">Codifica um modo de exibição para a tabela de destinatários de uma mensagem no fluxo de dados TNEF para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="31bb0-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="31bb0-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="31bb0-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="31bb0-134">Processa componentes individuais de uma mensagem de cada vez em um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="31bb0-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31bb0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="31bb0-135">See also</span></span>



[<span data-ttu-id="31bb0-136">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="31bb0-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

