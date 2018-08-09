---
title: Transmitir e copiar propriedades nomeadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a5d2244270463fcc2fe0a9786112590e741a8a66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770617"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="4fd93-103">Transmitir e copiar propriedades nomeadas</span><span class="sxs-lookup"><span data-stu-id="4fd93-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="4fd93-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4fd93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4fd93-105">Sempre que uma propriedade nomeada é enviada, movido ou copiadas, o nome permanece constante, mas o identificador deve alterar para cumpram o mapeamento de objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="4fd93-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="4fd93-106">A única exceção a essa regra é quando a origem e destino têm a mesma assinatura de mapeamento, tornando o novo mapeamento desnecessária.</span><span class="sxs-lookup"><span data-stu-id="4fd93-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="4fd93-107">É responsabilidade do provedor de transporte para remapear os nomes das propriedades nomeadas transmitidos aos identificadores apropriados que funcionam no destino.</span><span class="sxs-lookup"><span data-stu-id="4fd93-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="4fd93-108">O provedor de transporte de envio não é possível saber qual é o mapeamento correto no destino; ela deve transmita os nomes e contam com o provedor de transporte de recebimento para mapeá-los aos identificadores que funcionam.</span><span class="sxs-lookup"><span data-stu-id="4fd93-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="4fd93-109">A implementação de MAPI do TNEF lida com o novo mapeamento de propriedades nomeadas para provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="4fd93-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="4fd93-110">Provedores de transporte podem lidar com o novo mapeamento manualmente ou usar a implementação de TNEF.</span><span class="sxs-lookup"><span data-stu-id="4fd93-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="4fd93-111">Um novo semelhante mapeamento de propriedades nomeadas deve ocorrer quando essas propriedades são copiadas entre as lojas de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4fd93-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="4fd93-112">No entanto, porque os provedores de armazenamento de mensagem podem recuperar o nome para o mapeamento de identificador do destino, podem remapear as propriedades imediatamente e não precisará contam com o armazenamento de mensagens de destino.</span><span class="sxs-lookup"><span data-stu-id="4fd93-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4fd93-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fd93-113">See also</span></span>



[<span data-ttu-id="4fd93-114">MAPI denominada propriedades</span><span class="sxs-lookup"><span data-stu-id="4fd93-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

